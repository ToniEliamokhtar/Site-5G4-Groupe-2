+++
title = "Infos"
weight = 1
+++

> [!info]
>   J'utilise le site [Hugo](https://gohugo.io/documentation/) et
    [Hugo Relearn Theme](https://mcshelby.github.io/hugo-theme-relearn/index.html)
    pour référence sur comment faire certaines choses. <br>
> <br>
> - L'une des choses les plus importantes est que j'ai constaté qu'on peut utiliser du html et ça
    fonctionne, ce qui facilite énormément les choses!<br>
> <br>
> - Pour l'atelier, c'est la même application que je vous avais montré lors de la démo. J'ai réglé la petite erreur de Frontend et j'y ai ajouté du css!
> <br>
> - Pour finir, je vais refaire une nouvelle application, avec probablement open web ui, dont vous m'avais parlé lors de la démo. Je n'ai pas encore eu le temps de voir
    ce que c'est exactement, alors je vais voir ce que c'est et soit faire une application en intégrant Whisper avec, ou sinon je vais faire une nouvelle application qui intègre des spectogrammes log-mel. <br>
> <br>
> - Voici le lien du repo git qui contiendra ce projet.  <br>
> https://github.com/ToniEliamokhtar/WhisperAIAmeliore <br>
> <br>  
> - Je vais essayer de le finir d'ici mardi le 16, car il me reste encore le projet App mobiles à finir et l'examen de
    Soutien Technique à faire.  <br>
> <br>
> - J'aimerai vous remercier pour votre aide, votre temps et votre compréhension avec moi, j'espère que mon travail vous plaira :) !


## PLAN NOTES DE COURS

### C'est quoi Whisper? 
- Système de Reconnaissance Automatique de la parole
- Modèle Deep Learning
- Par OpenAI, Open Source, 21 Septembre 2022
- Entraîné 680 000 heures
- Supervisé vs Non Supervisé
- Fichiers issues du Web, tâches diverses
- Réseau de neurones
- basé sur des patterns


### Utilisation
- Il reçoit audio (wav, mp3, aiff, etc.)
- Il **prédit** le résultat
- Découpe 30 secondes
- Fréquences, variations sonores, rythme, patterns audios
- Tiny, Base, Small, Medium, Large

### Forces
- Robuste au bruit
- Multilingue
- Pas complexe
- Modèle très général

### Features
- Transformer
- Encoder(numérique) / Decoder(texte)
- FP16 et FP32
- Log-mel spectogram (représentation visuelle)

<br>

![alt text](whisperTransformer.png)