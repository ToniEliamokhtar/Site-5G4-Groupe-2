+++
title = "Atelier"
weight = 4
+++

## Objectif

**L'objectif de cet atelier est d'installer Whisper et de l'utiliser librement dans une application Web.**

### La première étape : Préparation de l'environnement

> Tout d'abord, il faut savoir que pour faire fonctionner Whisper sur notre ordi, il faut installer 5 items différents.

### 1. Construire l'image Docker

> Le premier item à installer est Python. Python est le language de programmation que WhisperAI utilise!

Selon ce qui est écrit dans le répertoire [Github](https://github.com/openai/whisper) de Whisper par OpenAI, Python 3.9.9 a été utilisé pour entraîner leur modèles, mais leur code devrait fonctionner avec Python de 3.8 à 3.11. POUR ÊTRE SÛR d'éviter les bugs, on utilisera la `version 3.10`, une version un peu plus à jour que 3.9, mais toujours supportée par Whisper.

> [!info]
> `ATTENTION !!`<br>
> - Linux utilise Python pour son fonctionnement interne, donc on ne doit jamais modifier la
    version système. Pour pouvoir travailler avec Whisper, on va installer Python 3.9 séparément et on l'utilisera via un environnement isolé, et ce en utilisant Docker.

Tout d'abord, il faut vérifier la verison de Python qu'on a sur notre système Linux. Si vous avez déjà la bonne version d'installée, vous pouvez passer à la prochaine étape, Installer Whisper. <br>
Dans mon cas personnel, sur mon Linux Mint, j'ai la version 3.12.3. Pour vous, cela peut-être différent, mais ça n'affectera pas notre travail.

![alt text](pythonVersion.png)

La prochaine étape est de vérifier que nous avons docker. Je ne vais pas expliquer comment installer docker, on a eu un atelier dessus au début de la session et je l'ai déjà fait au début de la session.

``` bash
toni@toni-Horizon-T12750:~$ docker --version
Docker version 28.2.2, build 28.2.2-0ubuntu1~24.04.1
```

Maintenant que les vérifications faites, la première chose à faire est de créer un dossier qui va contenir tous les fichiers nécessaires (Dockerfile, le code Python, etc.). Vous pouvez nommer le dossier comme vous voulez, mais pour cet atelier, je vais le nommer whisper-atelier

``` bash
$ mkdir whisper-atelier

$ cd whisper-atelier
```

On va préparer ensuite un Dockerfile avec Python 3.10.

Le but est d'utiliser Docker pour créer un environnement isolé, ainsi, on ne touchera pas au Python de l'environnement interne de notre système Linux.

Une fois qu'on est dans le répertoire (c'est mieux de l'ouvrir dans vscode), on crée un fichier et on le nomme `Dockerfile` (sans extension). On va installer la version slim, qui est plus légère et donc son téléchargement sera plus rapide. On fait juste ce qui est nécessaire pour partir Whisper sur un système minime. Dans le Dockerfile, vous pouvez copier coller les lignes ci bas:

``` bash
FROM python:3.10-slim

# 1. Dépendances système (ffmpeg = obligatoire pour Whisper)
RUN apt-get update && apt-get install -y \
    ffmpeg \
    git \
 && rm -rf /var/lib/apt/lists/*

# 2. Dossier de travail
WORKDIR /app

# 3. Installation des dépendances Python
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 4. On laisse le container démarrer dans /app avec un shell
CMD ["bash"]
```
***À propos de ffmpeg :***
- Il est super important, car c'est lui qui lit (sert à décoder) les fichiers audio (mp3, wav, m4a, etc.)
- Whisper s'appuie dessus pour convertir l'audio en format utilisable par le modèle.

<br>

Un deuxième fichier doit être créé, et on le nomme `requirements.txt`.<br>
Requirements contient tout ce qui est requis/obligatoire en fait.

> torch : PyTorch est la grosse librairie de deep learning dont Whisper a besoin. <br>
> openai-whisper : la librairie Whisper elle même. <br>
> tiktoken : l'outil de tokenization utilisé en interne par Whisper.

Vous pouvez copier coller les lignes ci bas dedans:

``` bash
torch
openai-whisper
tiktoken
```

Maintenant qu'on a ces deux fichiers prêts, la prochaine étape est de faire le build!
Dans le bash, on peut faire cette commande pour construire l'image Docker avec toutes les conditions qu'on a donné dans le Dockerfile et le fichier requirements.txt

``` bash
docker build -t whisper-atelier .
```

- `docker build` : construit l'image
- `-t whisper-atelier` : donne un nome à l'image
- `.` : le contexte de build, en d'autres mot on choisit de faire le build dans le dossier courant

<br>
Le build va prendre beaucoup de temps, mais c'est normal. Ce qu'on installe est vraiment loud et cela peut prendre du temps pour tout installer. Une fois que c'est finit, vous devrez voir ces deux lignes:

``` bash
Successfully built <id>
Successfully tagged whisper-atelier:latest
```

Maintenant que l'image est construite, on va entrer dans le conteneur.

``` bash
docker run -it --rm -v "$(pwd)":/app whisper-atelier
```
On démarre un conteneur à partir de l'image :
- `-it` : mode interactif, pour avoir un shell dedans.
- `--rm` : le conteneur est supprimé quand on quitte, ce qui évite d'en accumuler (gestion de mémoir)
- `-v "$(pwd)":/app` : on monte notre dossier courant dans /app dans le conteneur (de cette façon, on a des fichiers partagés entre notre PC et Docker)
- `whisper-atelier` : le nom de l'image qu'on vient de construire

Une fois cela fait, notre prompt va changer vers un truc du genre : 
``` bash
root@<id_du_conteneur>:/app#
```

Dans mon cas, c'est ça que c'est devenu : 
![alt text](dockerContainer.png)

Normalement, l'environnement devrait être prêt!
![alt text](dockerTest.png)

## Tester Whisper

On se prépare maintenant à tester Whisper. 

Allez dans le dossier whisper-atelier, notre **dossier local**, pas dans Docker.
On cré dedans un dossier `audio`, dans lequel on va mettre des fichiers audio .mp3 ou .wav.

![alt text](dossierAudio.png)

J'ai utilisé le site [Sample Focus](https://samplefocus.com/categories/spoken?min_tempo=0&max_tempo=200&min_duration=0&max_duration=30.8)
pour trouver des échantillons de voix ou de personnes qui parlent. Sur ce site, on peut créer notre compte et avoir le droit de télécharger 5 échantillons gratuitement.

Une fois que vous avez choisi vos échantillons, vous devez les mettre dans le dossier audio qu'on a créé tantôt.

![alt text](samplesAudio.png)
<br>
Pour pouvoir transcrire les fichiers audio, nous avons besoin de créer un nouveau fichier qu'on va appeler `transcribe.py`.

Dedans, on va mettre ce code là :

``` bash
import whisper

# 1. Charger le modèle Whisper
model = whisper.load_model("base")

# 2. Transcrire le fichier audio
result = model.transcribe("audio/normalEnglish.wav")

# 3. Afficher le texte transcrit
print(result["text"])
```

- `import whisper` : on importe la librairie Whisper installée dans le conteneur
- `load_model("base")` : ce modèle offre un compromis entre vitesse et précision, alors parfait pour un atelier!
- `transcribe(...)` : C'est cette commande qui nous permet de tout transcrire. Elle charge l'audio, le découpe, extrait des features (Mel spectogram), passe tout ça dans un Transformer et génère du texte.
- `result["text"]` : Finalement, on dit que le résultat est un dictionnaire (texte, langue, segments, timestamps...)

<br>

**Maintenant que tout est prêt, on peut FINALEMENT exécuter le script!**

Pour ce faire, il suffit d'ouvrir le terminal et d'écrire : 

``` bash
python transcribe.py
```

![alt text](resultatNormalEnglish.png)

> Le warning qu'on voit ici est lié au fait que Whisper utilise le CPU plutôt que le GPU. Normalement, Whisper préfère utiliser le GPU, car le CPU ne supporte pas efficacement le FP16.<br>
> Normalement, Whisper détecte automatiquement le matériel disponible. Dans notre conteneur, il n'y a pas de GPU, uniquement le CPU. <br>
> <br>
> **Message (résumé) :** <br>
>   FP16 is not supported on CPU, using FP32 instead <br>
> <br>
> **La différence entre FP16 et FP32 :**
> - FP16 (float16): calculs en demi-précisions 
>   - plus rapide,
>   - moins de mémoire
>   - surtout utilisé sur GPU
> - FP32 (float32): calculs en précision normale
>   - plus lents
>   - plus précis
>   - standard sur CPU


Whisper est conçu pour fonctionner aussi bien sur GPU que sur CPU. Quand il n'y a pas de GPU ou qu'il n'est pas disponible, le modèle bascule automatiquement en calculs FP32 (float32) plutôt que FP16, puisque les calculs FP16 sont optimisés pour les GPU.

Cette façon de s'adapter permet à Whisper d'être compatible sur tous les systèmes, au prix d'un temps de calcul un peu plus élevé.

> [!info]
> Il faut savoir qu'on peut forcer le modèle à utiliser le CPU si on 
> veut. Pour ce faire, il suffit de lancer cette commande : <br>
> `model = whisper.load_model("base", device="cpu")`
