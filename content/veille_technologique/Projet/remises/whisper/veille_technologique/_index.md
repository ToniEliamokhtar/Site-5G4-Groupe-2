+++
title = "Veille technologique"
weight = 2
+++

> [!info]
> J'ai choisi de poser mon prompt à ­`Claude`. La raison est parce que vous nous l'aviez 
> conseillé au début de la session. <br>
> <br>
> Au début, je vais mettre le Prompt que j'ai envoyé à Claude et la réponse qu'il m'a envoyé. 
> Tout cela sera suivi par des explications. <br>
> <br>
> Le modèle de Claude utilisé ici est `Sonnet 4.5` comme on peut le voir à la fin de la dernière 
> image.

## Prompt envoyé à Claude

![alt text](PromptClaude_1.png)
![alt text](PromptClaude_2.png)
![alt text](PromptClaude_3.png)
![alt text](PromptClaude_4.png)
![alt text](PromptClaude_5.png)

## Retour sur la réponse du LLM

> **Je vais répondre à plusieurs questions ici :**
> **Est ce que la réponse est**
> - complète?
> - comparable à un moteur de recherche?
> - comparable à un autre LLM?
> - comparable à ce que je connais déjà? <br>
> <br>
> **Et finalement :**
> - Est ce que j'ai trouvé une page web qui contient déjà toutes les informations fournis par le llm?

### 1. Est ce que la réponse est complète?
Je pense que la réponse de Claude est vraiment complète, comparée avec le prompt que je lui ai donné. Elle est pertinente, et elle couvre bien les éléments que j'ai demandées. Cependant, elle reste générale et ne permet pas, à elle seule, de contruire des notes de cours approfondies. Il faudra faire des recherches supplémentaires, que ce soit avec des blogs, des sites officiels de OpenAI et de WhisperAI, sur youtube et les réseaux sociaux ou sur d'autres sources. Je tiens à dire qu'on peut poser des questions ou des prompts plus précis au llm, et de cette façon il nous donnera des réponses plus précises et mieux construites.

> Je vais mettre le lien du chat avec Claude à la fin, avec les sources. Je vais faire ma recherche personnelle et je vais aussi utiliser Claude. De cette façon, je pense que ça ne fera pas de mal, au contraire, ça maximisera ma chance d'avoir des informations importantes que je n'aurais peut-être pas pu avoir en fesant une recherche seulement ou en utilisant un llm seulement.

### 2. Est ce que la réponse est comparable à un moteur de recherche?
Le truc avec les moteurs de recherche est qu'on peut trouver facilement beaucoup de sources, mais il faudra aller chercher les informations nous même. Ça prend de l'effort, car on peut passer beaucoup de temps parfois sans avoir récolté beaucoup d'informations valables. 

D'un autre point de vue, un moteur de recherche offre, comme j'ai déjà dis dans la première partie de ma réponse, beaucoup de sources. Cela me permet de faire une recherche beaucoup plus approffondie, de récolter beaucoup plus d'informations et d'avoir des preuves de mes sources.

Les llm, bien qu'ils ne fournissent pas autant d'informations, ils facilitent la recherche générales et nous donnent leurs sources (les sites qu'ils ont utilisé). Voici les sources que Claude a utilisé pour répondre à mon prompt:

- Whisper OpenAI voice to text 2024
    - https://github.com/openai/whisper
    - https://www.freecodecamp.org/news/how-to-turn-audio-to-text-using-openai-whisper/
    - https://openai.com/index/whisper/
    - https://learn.microsoft.com/en-us/azure/ai-services/speech-service/whisper-overview
    - https://platform.openai.com/docs/guides/speech-to-text
    - https://whisperui.com/
    - https://medium.com/@aleksej.gudkov/whisper-example-how-to-use-openais-whisper-for-speech-recognition-6196c758d47d
    - https://learn.microsoft.com/en-us/azure/ai-foundry/openai/whisper-quickstart?-view=foundry-classic
    - https://community.openai.com/t/voice-to-text-via-whisper-integration-in-chatgpt-web-app/685231
    - https://whisperai.com/

![alt text](liensClaude1.png)
<br>
- Whisper machine learning architecture transformer
    - https://en.wikipedia.org/wiki/Whisper_(speech_recognition_system)
    - https://openai.com/index/whisper/
    - https://huggingface.co/docs/transformers/en/model_doc/whisper
    - https://huggingface.co/openai/whisper-large-v3
    - https://www.louisbouchard.ai/whisper/
    - https://github.com/huggingface/transformers/blob/main/src/transformers/models/whisper/modeling_whisper.py
    - https://github.com/huggingface/transformers/blob/main/docs/source/en/model_doc/whisper.md
    - https://github.com/huggingface/transformers/blob/main/src/transformers/models/whisper/configuration_whisper.py
    - https://github.com/openai/whisper/discussions/654
    - https://www.gladia.io/blog/what-is-openai-whisper

![alt text](liensClaude2.png)
<br>
- Whisper limitations disadvantages 2024
    - https://learn.microsoft.com/en-us/answers/questions/1638419/whisper-model-limitation
    - https://www.transcribetube.com/blog/openai-whisper-api-limits
    - https://deepgram.com/learn/whisper-issues-smart-formatting
    - https://www.voicegain.ai/post/practical-considerations-for-voice-developers-considering-openais-whisper-asr
    - https://www.baldurbjarnason.com/2024/openai-whisper-risks/
    - https://www.gladia.io/blog/thinking-of-using-open-source-whisper-asr-here-are-the-main-factors-to-consider
    - https://www.gladia.io/blog/what-is-openai-whisper
    - https://aimpower.org/2024/11/07/disparities-in-whispers-automatic-speech-recognition-performance-on-disfluent-speech/
    - https://link.springer.com/article/10.1186/s13636-024-00349-3
    - https://alphacephei.com/nsh/2024/04/20/status-of-whisper.html

![alt text](liensClaude3.png)
<br>
Pour faire un petit récapitulatif, en terme de temps, un llm peut-être plus rapide, mais en conséquences, les informations ne seront pas aussi normbreuses ou précises que si on utilisait un moteur de recherche. Je dis cela parce que les llm synthétise, il résument beaucoup et choisissent quelles informations elles veulent nous montrer selon notre demande (prompt).<br>
<br>
`INFOS SUPPLÉMENTAIRES`<br>
En terme de structure, les informations qu'un llm nous donne sont très variables. Le llm prend des informations de plusieurs sites et nous les donne d'un coup, donc on aura que peu d'informations de chaque point du sujet. En utilisant Google par exemple, chaque site est bien construit, obtient beaucoup plus d'informations en lien avec un même point et peut nous être beaucoup plus valable. Cependant, il ne faut pas oublier que beaucoup les informations sont éparpillés. Il faudra les trier selon ce qui nous est important ou utile et reconstruire l'explication dans notre tête. <br>
<br>
Finalement, en terme de fiabilité, Claude, ou les llm, ont tendance à beaucoup synthétiser, donner une vue cohérente et ils nous sont très utiles pour comprendre un certain sujet. L'inconvénient avec les llm est qu'ils ne montrent pas toujours et clairement chaque informations provient d'où exactement. Ils peuvent se tromper, simplifier ou même halluciner et donner de fausses informations parfois. Si on compare cela avec Google, ou n'importe quel moteur de recherche, on a toujours accès aux sources originales. Cela veut dire qu'on peut toujours vérifier qui a écrit, quand il l'a écrit et dans quel contexte ça a été écrit. Bien sûr, ça reste long et exigeant de vérifier les informations et parfois il y a des sites qui donnent de fausses informations, mais au final on ne peut pas tout contrôler. <br>
<br>
Si on regarde si bas par exemple, Claude nous donne la source de la première et de la troisième information, mais il ne donne pas de source pour la deuxième!

![alt text](exempleClaude1.png)


### 3. Est ce que la réponse est comparable à un autre llm?

J'ai posé le même prompt à `Gemini`. Je vous montre sa réponse tout d'abord, et je vais faire un retour dessus après.

![alt text](promptGemini_1.png)
![alt text](promptGemini_2.png)
![alt text](promptGemini_3.png)
<br>
Comme on peut voir dans la réponse de Gemini, sa rééponse est mieux structurée, plus facile à comprendre et plus claire même. Gemini nous donne même une image pour qu'on comprenne mieux, et j'aime beaucoup cela personnellement. Claude, de l'autre côté, va plus loin dans les détails et les limites. Il explique et parle des problèmes fréquents par exemple pour nous faire comprendre des détails que Gemini n'en parle pas. On peut dire que la réponse de Gemini est beaucoup plus neutre que celle de Claude qui est un peu plus nuancée. <br>
<br>
Selon le llm qu'on utilise, l'approche ne sera pas la même, et cela est parce qu'ils ont chacun un algorithme propre à eux qu'ils utilisent pour savoir comment nous répondre.<br>
<br>
Pour apprendre, Gemini est plus simple, mais pour analyser, je pense que Claude est clairement plus utile.<br>
<br>
Personnellement, je vais continuer à utiliser Claude. La raison principale qui m'a poussé à prendre cette décision est que Claude donne plus d'informations, il est plus nuancé, il explique plus et c'est de ça que j'ai besoin pour un grand projet. Je trouve que c'est un meilleur llm pour une Veille Technologique aussi. 


### 4. Est ce que la réponse est comparable à ce que je connais déjà?
Honnêtement, je ne connaissais rien sur Whisper ou sur le Voice to Texte. Grâce à Claude, j'ai appris beaucoup de choses. Bien sûr, je connaissais le nom Whisper et qu'il est un programme de Voice to Texte fait par OpenAI, je connaissais aussi qu'il est open source, mais c'est tout.<br>
<br>
Ce que j'ai appris est que Whisper a été publié en septembre 2022, ce qui veut dire qu'il est très récent. Il a été formé sur ÉNORMÉMENT D'HEURES de données multilingues, précisément 680 000 heures. <br> 
<br>
J'ai une idée générale de ce que l'architecture Transformer est et je connais maintenant les étapes de comment Whisper analyse les fichiers d'audio (Preprocessing, Encodeur, Décodeur). J'ai appris comment Whisper a été entraîné et ce qui le différencie des autres modèles plus spécialisés. <br> 
<br>
J'ai une idée générale de ce que ses avantages et désavantages sont par rapport aux autres modèles de transcription de voix. Je connais certaines informations précises sur ses limitations, comme le fait qu'il prend des fichiers audio de taille 25MB maximum. Bien sûr, cette information a été publiée en 2024, donc je vais devoir vérifier si elle est toujours à jour. <br>
<br>
Claude me parle du rapport de Whisper avec l'actualité (2024, ce qui est quand même récent), donc je suis informé sur où Whisper est utilisé, ce que les gens en pensent et ce que les grandes compagnies en pensent aussi. Je ne veux pas donner beaucoup d'informations ici, car je vais parler de tout cela dans la section Notes de Cours.

### 5. Est ce que j'ai trouvé une page web qui contient déjà toutes les informations fournis par le llm?

Non, je n'ai pas trouvé une seule page qui contient déjà toutes les informations fournis par le llm. En fait, j'ai dû chercher beaucoup de sites, d'articles et de vidéos youtube pour récolter toutes les informations dont j'ai eu besoin pour faire mes notes de cours, et l'atelier aussi bien sûr. La page la plus proche, je dirais c'était la page officielle de openAI, mais même là, elle ne contenait qu'une fraction des informations. <br>

En fait, j'aimerai faire un retour sur un point, parce que je pense qu'il est bien important. Je n'avais pas vraiment une seule page, mais plutôt un trio de pages qui se complétaient. C'est la page officielle de [OpenAI](https://openai.com/fr-FR/index/whisper/), la page officielle de [WhisperAI](https://whisperai.com/) et le repos [Github de WhisperAI](https://github.com/openai/whisper?tab=readme-ov-file) qui contenait pas mal d'informations aussi. <br>

Bien sûr, encore là, j'ai dû utiliser d'autres sources, mais ça, je vais en parler dans la prochaine section.


## Sources choisies pour les notes de cours

Pour cette section, je vais la diviser en plusieurs parties dépendant du type de source.


### Youtube

J'ai regardé vraiment beaucoup de vidéos youtube, mais je n'ai pas trouvé beaucoup de bonnes vidéos qui donnaient des informations importantes et cruciales. Cependant, j'ai fini par trouver quand même trois bonnes vidéos faites par différentes personnes. D'ailleurs, l'une d'entre elles a tout simplement une voix IA qui parle, mais il y a de bonnes informations quand même.

Voici les trois vidéos:
- https://youtu.be/ABFqbY_rmEk?si=5cgywGGt3kfzMpZw
- https://youtu.be/RJUXKy60CXM?si=-u8ZMSlemlJblQHr
- https://youtu.be/uFOkMme19Zs?si=9T8u1Z6G2ulQGYi5


### Sites

Pour les sites, j'ai ouvert beaucoup de sites, mais pas beaucoup d'entre eux m'aidaient. J'ai fini par me concentrer sur deux sites seulement, le site officiel de [OpenAI](https://openai.com/fr-FR/index/whisper/) et le site officiel de [WhisperAI](https://whisperai.com/) pour récolter les informations et mieux comprendre le fonctionnement de WhisperAI.

Il y a un troisième site que j'ai utilisé, c'est le site de [Music.ai](https://music.ai/). Cependant, ce site ne m'a aucunement aidé avec la compréhension de WhisperAI. En fait, c'est un site qui est un peu semblable à WhisperAI, mais ce site offre un AI capable de transcrire les paroles de chansons ! Il est spécialisé dans la transcription de paroles de chansons. Je vais le tester après le jour de l'an, quand je vais me remettre à écrire des chansons, et je verrai son efficacité! Je suis vraiment excité à le tester :)


### Articles

Pour les articles, c'est eux qui m'ont le plus aidé dans ma recherche sur WhisperAI. C'est eux qui m'ont donné le plus d'informations. Par exemple, quand je cherchais un site qui parlait d'un certain sujet, le seul truc que je trouvais était pleins d'articles. Je n'arrivais pas à trouver des sites avec des informations vraiment précises et qui peuvent m'aider à donner des exemples et parler avec précisions. Bien sûr, après avoir lu et vérifié les informations contenus dans plusieurs articles, j'ai pu continuer avec confiance que ce que j'écris est bien et correct!

J'ai dû inclure un article de [Wikipedia](https://en.wikipedia.org/wiki/Spectrogram), bien que je ne voulais rien prendre de ce site puisque n'importe qui peut écrire dedans, mais je ne trouvais aucun site qui expliquait bien les spectogrammes. Du coup j'ai finis par lire l'article de Wikipedia et honnêtement il m'a énormément aidé à comprendre comment WhisperAI arrive à lire les fichiers audio! Je vous conseillerai de le lire, il est vraiment bien écrit.

### Github

Finalement, j'ai utilisé le repos [Github de WhisperAI](https://github.com/openai/whisper), qui était la principal source d'informations pour faire mon projet.


## Article récent qui traite de Whisper

J'ai utilisé **six** articles qui traitent de Whisper. Plusieurs d'entre eux parlaient en général sur comment Whisper fonctionne, ce que WhisperAI est vraiment, mais il y en avait certains qui donnaient des informations plus exactes. Par exemple, cet article de [Fortune](https://fortune.com/2023/03/01/openai-chatgpt-api-enterprise-commercial-instacart-shopify-snap-quizlet/) écrit par Jeremy Kahn le premier Mars 2023. Dans cet article, il parlait des entreprises qui sont en relation avec WhisperAI, qui l'utilisent, et d'ailleurs c'est là que j'ai trouvé que la compagnie Speak est la première à vraiment intégrer WhisperAI dans son application/site Web. J'en parle plus de cette compagnie dans les notes de cours !


## Quelques sources réseaux sociaux / chaîne youtube

Comme je l'ai déjà dis dans l'autre section, j'ai utilisé trois vidéos youtube, qui pour la plupart parlait de WhisperAI en général. Il y a une seule d'entre ces trois vidéos qui donnait un bon exemple d'utilisation de WhisperAI, et je m'en suis inspiré pour faire mon application à moi. Elle a été faite par Kevin Stratvert il y a 2 ans.<br>
La voici :<br>
https://youtu.be/ABFqbY_rmEk?si=ta8PvWXqNjTgE58l

Il y a une autre vidéo aussi, c'est un québécois qui l'a fait, mais en anglais. C'est la vidéo qui m'a aidé le plus, car il donnait vraiment beaucoup d'informations importantes et pertinentes! Je vous conseillerais de la regarder, elle est vraiment bien faite! <br>
La voici : <br>
https://youtu.be/uFOkMme19Zs?si=IJVWysebo8usHv-J

Pour finir, voici la vidéo faite par un IA, mais qui m'a quand même bien aidé : <br>
https://youtu.be/RJUXKy60CXM?si=rbESuXevOv9mM09c