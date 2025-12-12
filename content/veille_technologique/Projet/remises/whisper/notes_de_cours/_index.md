+++
title = "Notes de cours"
weight = 3
+++

### C'est quoi au juste, WhisperAI?

WhisperAI est un système de reconnaissance automatique de la parole, développé par OpenAI. <br>
Il a été mis en ligne sous licence *open-source* le 21 septembre 2022. 

![alt text](whisperAI.png)

Il faut savoir que WhisperAI a trois principales fonctionnalités :
- Transcription
- Traduction vers l'anglais
- Identification de la langue

### Entraînement

Whisper a été entraîné sur **680 000 heures** de données audio, ce qui est un volume extrêmement élevé comparé aux datasets ASR (Automatic Speech Recognition) classiques. <br>

Ce volume de données permet à WhisperAI d'avoir une approche généraliste pour comprendre les fichiers audio, pas spécialiste ! Je vais revenir sur ça plus bas dans le cours. <br>

En fait, normalement, les ASR classique sont très souvent entraînés sur quelques *centaines* à quelques *milliers* d'heures. Ils sont normalement entraînés sur des corpus propres et contrôlés.

> Un Corpus est un ensemble de données utilisé pour entraîner un modèle !

***Données et provenance***

Whisper a été entraîné majoritairement sur des donées qui proviennent du Web. Cela peut inclure des enregistrements audio très variées, comme :
- Des entrevues
- Des conférences
- Des vidéos (que ce soit de Youtube ou de n'importe quelle platforme)
- Des podcasts 
- Et pleins de discussions enregistrées dans de plusieurs contextes réels et variés. 

Ces enregistrements regroupent *plusieurs langues et accents* et portent sur des *tâches diverses*. 

Contrairement à des données enregistrées spécifiquement pour l'entraînement d'un modèle de reconnaissance vocale, ces fichiers audio ne sont pas produits dans des conditions idéales et contrôlées!

***Avantages***

Cette diversité des contextes audio donne à WhisperAI un très grand avantage. En fait, en étant exposé à des accents, des bruits de fond et tant d'environnements variés dès son entraînement, Whisper apprend à traiter des situations proches de celles rencontrés en pratique. 

Cette approche favorise une compréhension plus générale de la parole, plutôt qu'une spécialisation dans un seul type d'enregistrement. 

Whisper, grâce à ces données variés, est devenu un modèle robuste aux bruits de fond, c'est un modèle multilingue, c'est un modèle très général capable de s'adapter à beaucoup de situations et de contextes !

***Désavantages***

Ces mêmes avantages peuvent devenir des désavantages, dépendant du contexte du fichier audio qu'on veut que Whisper analyse. 

> `Exemple :` <br>
Quand on veut utiliser Whisper pour transcrire une chanson, Whisper aura plus de mal à bien transcrire les mots qu'un modèle spécialisé dans la transcription des audios accompagnés d'instruments, de bruits de fonds diverses mais toujours en rapport avec la musique, ainsi que plusieurs personnent qui chantent en même temps. 

En fait:

`Chanter ≠ parler`

Il y a une grande différence dans l'analyse des fichiers audios de musique et de conversations normales. Même si les mots sont les mêmes, il y a plusieurs éléments qui ne sont pas les mêmes !

- Rythme différent
- Voyelles étirés
- Mélodie qui déforme les phonèmes
- Instruments qui couvrent la voix
- Ad-libs, répétiions, l'autotune aussi peut affecter

Résultat: Whisper peut se tromper, halluciner ou simplifier les paroles d'une chanson :(


> [!info]
> J'ai fait une petite recherche personnelle ! <br>
> Lyrics Transcription / Singing voice recognition (SVR) : <br>
> - Ces modèles sont entraînés sur des chansons. Il apprennent à gérer la mélodie, le tempo et la répétition de refrains. <br>
> 
> `Whisper n'est PAS conçu pour ça à la base` <br>


<br> <br> <br> <br>

Issues du Web, ces données regroupent plusieurs langues et portent sur des tâches diverses.

Avec ce modèle (WhisperAI), OpenAI démontre que l'utilisation d'un jeu de données aussi étendu et diversifié améliore la fiabilité de la reconnaissance des accents, des bruits de fond et des termes techniques. 

De plus, ce modèle permet la transcription audio dans plusieurs langues, ainsi que la traduction depuis ces langues vers l'anglais. 

Il faut savoir que OpenAI a publié le modèle et le code d'inférence sous licence open source, ce qui permet la création d'applications utiles et de nouvelles recherches sur la fiabilisation du traitement de la parole!

### Architecture

![alt text](whisperArchitecture.png)

***ARCHITECTURE TRANSFORMER***

Whisper utilise une architecture encoder-decoder Transformer de bout en bout. 

Pour mieux comprendre comment il fonctionne, je vais en parler en plusieurs points: