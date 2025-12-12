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

Ce volume de données permet à WhisperAI d'avoir une approche généraliste pour comprendre les fichiers audio, pas spécialiste ! Je vais revenir sur ça plus bas dans les notes de cours. <br>

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
