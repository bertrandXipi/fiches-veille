---
title: Le mec qui a CRÉÉ Claude Code vient de partager comment il bosse.
source_url: "https://www.linkedin.com/posts/maxime-brunet-shunpo_claudecode-ia-daezveloppement-share-7439036344800256000-4Tlj?utm_source=share&utm_medium=member_android&rcm=ACoAABVFmSQB_1DLOTmJwsRT2PNC0hrNEP6ztIA"
source_type: article
date_captured: "2026-03-16T20:03:12.679Z"
date_processed: "2026-03-16T20:04:30.698Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1483193941728694495"
status: published
notebooklm_notebook_id: eea0382d-c943-416b-a20b-4427b9f9b5aa
notebooklm_source_id: f982d794-d33c-4b35-aa7f-b8b4b24fc765
notebooklm_url: "https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa"
keywords:
  - Claude Code
  - Sessions en parallèle
  - Workflow en piliers
  - Stratégie de sous-agents
  - Boucle d'auto-amélioration
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales

Le document source, issu d'une publication de Maxime Brunet, dévoile les méthodes de travail de Boris Cherny, le directeur de Claude Code chez l'entreprise Anthropic [1]. L'idée principale qui se dégage de ce texte est une redéfinition radicale de l'utilisation de l'intelligence artificielle dans le développement logiciel. Plutôt que d'utiliser l'IA de manière séquentielle, lente et avec de simples requêtes individuelles, l'approche préconisée consiste à déployer une véritable « armée d'IA » travaillant en simultané [1]. Le concept central de cette méthode est de cesser de percevoir et d'utiliser l'IA comme un simple assistant de codage ou un outil d'autocomplétion, mais plutôt de la traiter comme une « flotte d'ingénieurs seniors » à qui l'on délègue des projets et des tâches complexes de bout en bout [2].

### 2. Les différents points de vue ou arguments présentés

L'auteur présente plusieurs arguments forts pour repenser notre rapport aux agents conversationnels dans la programmation. Premièrement, bien que l'exécution en parallèle de multiples sessions soit visuellement impressionnante et productive, l'auteur argumente que ce n'est pas l'élément qui change réellement la donne [1]. Le véritable argument soutenu est qu'une méthodologie de travail rigoureuse, structurée en six piliers fondamentaux, est absolument indispensable pour tirer parti de la puissance brute de l'outil [1]. 

Un autre point de vue essentiel développé dans le texte est l'importance cruciale de l'auto-apprentissage local : l'IA ne doit pas repartir de zéro à chaque interaction, mais doit au contraire capitaliser sur ses erreurs pour devenir « exponentiellement meilleure » sur un projet spécifique au fil du temps [2, 3]. Enfin, l'auteur soutient que l'IA ne doit pas se contenter de fournir un code qui fonctionne de justesse, mais qu'elle doit être tenue à des standards de qualité extrêmement élevés, équivalents à ceux qu'on attendrait d'un ingénieur très expérimenté [4].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le texte aborde de nombreuses données chiffrées et des exemples techniques très précis. Quotidiennement, Boris Cherny lance 10 à 15 sessions de Claude Code de manière parallèle : 5 directement dans son terminal, 5 à 10 sur l'interface web claude.ai, et quelques-unes depuis son iPhone le matin [1]. 

Sur le plan de l'architecture technique de son travail, il utilise une stratégie de « sous-agents » (sub-agents) où chaque tâche spécifique de recherche ou d'analyse est allouée à un agent dédié, ce qui permet de préserver la clarté du contexte principal [3]. Un exemple concret de cette automatisation extrême est la gestion des bases de données : Cherny n'a pas écrit une seule ligne de code SQL en six mois, puisqu'il laisse Claude extraire directement les données de BigQuery via une interface en ligne de commande (CLI) [2]. 

De plus, le processus s'appuie sur des fichiers locaux spécifiques, tels que `lessons.md` ou `Claude.md`, utilisés pour stocker les règles et les corrections apportées en continu par l'utilisateur [2, 3]. Pour tester la qualité du code, des requêtes très spécifiques sont utilisées, comme demander à l'IA : « Est-ce qu'un staff engineer validerait ça ? » ou encore « Sachant tout ce que je sais maintenant, implémente la solution élégante » [4].

### 4. Les problèmes, défis ou limitations identifiés

Bien que le texte soit résolument axé sur les solutions et la productivité, il identifie en filigrane plusieurs défis majeurs liés à l'utilisation classique de l'IA par le grand public. Le premier est le risque d'ambiguïté ou de déraillement face à des tâches nécessitant plus de trois étapes de réalisation [3]. 

Un autre problème technique courant est la saturation ou la pollution de la fenêtre de contexte de l'IA, un défi qui est ici mis en évidence par la nécessité de créer des sous-agents pour garder un contexte « clean » [3]. Le texte soulève également le problème extrêmement frustrant des erreurs répétitives de l'IA lors des itérations de code [3]. On note aussi le risque omniprésent d'obtenir du code qui remplit sa fonction mais qui est inélégant ou mal conçu (des solutions qualifiées de « hacky ») [4]. Enfin, le changement constant de contexte (context-switching) de la part du développeur lors de la traque et de la correction de bugs est pointé comme un obstacle majeur à la productivité [4].

### 5. Les solutions, recommandations ou perspectives proposées

Pour surmonter ces limites techniques et humaines, le document recommande l'adoption stricte d'un workflow en six piliers [1] :
1. **L'obligation d'un « Plan Mode »** : Pour toute tâche dépassant trois étapes, des spécifications sans ambiguïté sont rédigées avant de coder, avec un arrêt et une replanification immédiate si le processus dévie [3].
2. **La stratégie de sous-agents** : Une délégation stricte et isolée selon la règle « 1 tâche = 1 sous-agent » [3].
3. **Une boucle d'auto-amélioration** : La mise en place d'un fichier de leçons (`lessons.md`) permettant à l'IA d'écrire et de mémoriser ses propres règles pour ne plus reproduire les mêmes erreurs [3].
4. **La vérification avant validation** : L'interdiction de marquer une tâche comme terminée sans la preuve de son fonctionnement et sans l'approbation simulée d'un ingénieur de haut niveau [4].
5. **L'exigence d'élégance** : Le refus des solutions bricolées en forçant l'IA à se challenger elle-même pour réécrire et optimiser son propre code [4].
6. **La correction autonome** : La résolution des bugs de manière complètement indépendante par l'IA, en lui laissant analyser seule les logs, les erreurs et les tests défaillants sans déranger le développeur [4].

### 6. Une synthèse critique et les implications pratiques

En synthèse, ce document ne se contente pas de présenter des astuces de productivité ; il illustre une transition paradigmatique fondamentale dans l'ingénierie logicielle. Il s'agit du passage de la programmation purement assistée par l'IA vers l'orchestration managériale de systèmes d'IA autonomes. 

Les implications pratiques pour les développeurs actuels et futurs sont immenses. Le métier évolue : il s'agit de moins en moins de savoir taper du code rapidement, et de plus en plus de savoir rédiger des spécifications sans ambiguïté et de savoir architecturer des systèmes de délégation [3]. La mise en place d'une mémoire de projet persistante via un simple fichier texte de leçons est une solution technique à la fois brillante, peu coûteuse et immédiatement applicable pour pallier le manque de mémoire à long terme des grands modèles de langage [3]. À terme, cette méthode suggère que le rôle du développeur se transforme en celui d'un chef d'orchestre ou d'un réviseur de code ultra-exigeant, définitivement libéré des tâches d'exécution routinières comme l'écriture de requêtes SQL ou la simple traque d'erreurs dans des fichiers de logs [2, 4].

## 💼 Post LinkedIn

Pendant qu'on galère avec un seul prompt, le boss de Claude Code dirige une armée d'IA [1].

Boris Cherny dirige ce projet chez Anthropic et vient de partager sa méthode [1]. 
Son quotidien ? Lancer 10 à 15 sessions en parallèle [1]. Chaque jour [1]. 
Il ne code plus vraiment lui-même.

Voici comment il orchestre sa flotte d'ingénieurs virtuels :
→ Planification stricte avant de coder la moindre ligne [2].
→ Délégation massive à des sous-agents ultra-focus sur une seule tâche [2].
→ Auto-amélioration continue via un fichier de leçons pour éradiquer les erreurs récurrentes [2].
→ Correction 100% autonome des bugs sans aucune intervention [3].

Le résultat est juste dingue.
Il n'a pas écrit une seule ligne de SQL depuis 6 mois [4]. 
Claude va chercher les données tout seul [4]. 
La clé, c'est de traiter l'IA comme une équipe de seniors, pas comme un simple outil [4].

Et toi, tu utilises tes IA comme de simples assistants ou tu as déjà commencé à déléguer massivement ?

#ClaudeCode #Productivité #IA

## Mots-clés

- **Claude Code**
- **Sessions en parallèle**
- **Workflow en piliers**
- **Stratégie de sous-agents**
- **Boucle d'auto-amélioration**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.linkedin.com/posts/maxime-brunet-shunpo_claudecode-ia-daezveloppement-share-7439036344800256000-4Tlj?utm_source=share&utm_medium=member_android&rcm=ACoAABVFmSQB_1DLOTmJwsRT2PNC0hrNEP6ztIA)
