---
title: Boris Cherny, the creator of Claude Code, just shared 15 power features that most people never use.
source_url: "https://www.linkedin.com/posts/dr-axel-schell-7b2792158_claudecode-agenticai-anthropic-share-7445737394030592000-eF0H?utm_source=share&utm_medium=member_android&rcm=ACoAABVFmSQB_1DLOTmJwsRT2PNC0hrNEP6ztIA"
source_type: article
date_captured: "2026-04-09T06:24:48.242Z"
date_processed: "2026-04-09T06:25:58.247Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1491685293021991015"
status: published
notebooklm_notebook_id: eea0382d-c943-416b-a20b-4427b9f9b5aa
notebooklm_source_id: e10b16f2-32ba-4717-a213-9ba1eecb46ff
notebooklm_url: "https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa"
keywords:
  - Claude Code
  - Intelligence artificielle agentique
  - Développement logiciel automatisé
  - Fonctionnalités de programmation
  - Orchestration d'agents IA
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales

Ce rapport s'appuie sur une publication de Dr. Axel Schell, qui relaie et commente les 15 fonctionnalités avancées ("power features") de Claude Code, partagées initialement par son créateur, Boris Cherny [1]. L'idée principale qui se dégage de ce document est que les outils d'assistance au développement par intelligence artificielle évoluent rapidement vers des systèmes d'agents autonomes complexes. Claude Code ne se contente plus d'être un simple assistant de saisie ou un copilote réactif ; il devient une plateforme d'orchestration capable d'exécuter des tâches en parallèle, de fonctionner de manière autonome sur de longues périodes et d'être pilotée à distance [1, 2]. 

### 2. Les différents points de vue ou arguments présentés

Deux perspectives complémentaires émergent de ce contenu :
*   **Le point de vue du concepteur (Boris Cherny, via Dr. Schell) :** Il met en avant la flexibilité technique, l'ubiquité et la puissance brute de l'outil. L'argument sous-jacent est que les développeurs sous-utilisent les capacités d'automatisation de l'IA (comme les fonctions de traitement par lots ou de contrôle à distance) et devraient adopter ces fonctionnalités pour maximiser leur productivité [1].
*   **Le point de vue analytique et prospectif (Dr. Axel Schell) :** Schell soutient que des fonctionnalités telles que `/loop`, `/batch` et l'utilisation de "git worktrees" préfigurent l'avenir de la programmation agentique ("agentic coding") [2]. Il avance l'argument fort selon lequel nous passons d'un modèle de "pair programming" (programmation en binôme avec une IA) à l'orchestration de "flottes d'agents" travaillant en parallèle et de manière autonome, ce qui constitue un modèle opérationnel fondamentalement nouveau pour l'ingénierie logicielle [2].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le document regorge de détails techniques spécifiques sur l'utilisation de Claude Code :
*   **Mobilité et accès à distance :** Il est possible de coder depuis son téléphone via une application iOS [1]. La commande `/teleport` permet de rapatrier instantanément une session cloud sur un terminal local, tandis que `/remote control` permet de contrôler une session locale depuis un téléphone ou un navigateur [1]. La fonction "Dispatch" permet de déléguer des tâches à distance (gestion de fichiers, interaction sur Slack) [1].
*   **Autonomie et scalabilité :** La commande `/loop` permet de programmer Claude pour qu'il fonctionne jusqu'à une semaine entière, en gérant de manière autonome les revues de code, les "rebases" et le déploiement de Pull Requests (PRs) en production [1]. `/batch` permet de déployer des centaines, voire des milliers d'agents en parallèle [1]. De plus, l'utilisation de "Git worktrees" (avec la commande `claude -w`) permet d'exécuter des dizaines d'instances de Claude simultanément [1].
*   **Gestion de l'exécution et des erreurs :** Le système de "Hooks" est déterministe (suivi à 100%), par opposition au fichier de configuration `CLAUDE.md` qui n'a qu'une valeur consultative (suivi à 80%) [1]. Une combinaison de touches (Esc+Esc) permet de voyager dans le temps de la session en ouvrant un menu de points de contrôle pour restaurer le code ou la conversation [1].
*   **Interactions avancées :** Il est possible d'ajouter le terme "think" dans le prompt pour forcer l'IA à raisonner (effort élevé) avant d'écrire du code [1]. Les commandes `/btw` et `/branch` permettent respectivement de poser des questions annexes sans interrompre l'agent, et de dupliquer une session en cours de tâche (reprise avec `claude -r [id]`) [1].

### 4. Les problèmes, défis ou limitations identifiés

Bien que l'outil soit puissant, plusieurs défis ou limitations inhérents à l'usage de l'IA sont mis en évidence de manière implicite ou explicite :
*   **L'aveuglement visuel de l'IA :** Sans accès à un navigateur, Claude "devine" ("guessing") l'interface utilisateur. Il lui manque un retour visuel pour itérer correctement sur le rendu final d'une application [1].
*   **Le manque de fiabilité des instructions textuelles :** L'utilisation du fichier `CLAUDE.md` pour guider l'IA présente des limites, car l'IA ne suit ces instructions que dans environ 80% des cas, ce qui n'est pas suffisant pour des processus stricts [1].
*   **Les blocages liés aux permissions :** Lorsqu'un agent autonome rencontre une demande d'autorisation de l'interface système, le processus peut s'interrompre si l'utilisateur n'est pas devant son écran [1].
*   **Le risque d'hallucination ou de code erroné :** Si l'IA n'a aucun moyen de vérifier son propre travail, elle risque de produire un résultat incorrect ou de tourner en rond [1].

### 5. Les solutions, recommandations ou perspectives proposées

Pour pallier ces défis, plusieurs recommandations très concrètes sont formulées :
*   **Pour le retour visuel :** Il est fortement recommandé de donner accès à un navigateur à Claude afin qu'il puisse voir, écrire et itérer jusqu'à ce que le résultat visuel soit correct [1].
*   **Pour la fiabilité d'exécution :** Il faut utiliser les "Hooks" plutôt que le fichier `CLAUDE.md` lorsque l'on souhaite un comportement déterministe et garanti à 100% à chaque exécution [1].
*   **Pour la gestion des permissions à distance :** Une solution ingénieuse consiste à router les demandes de permission (via les Hooks) vers WhatsApp, permettant au développeur d'approuver ou de rejeter les appels d'outils depuis son téléphone, garantissant un contrôle total sans interruption du flux [1].
*   **Pour l'exactitude du code (la règle d'or) :** Le conseil présenté comme "le plus important" est de toujours fournir à Claude un moyen de vérifier sa propre production, en incluant des tests automatisés ou des résultats attendus explicites, afin qu'il puisse itérer jusqu'à l'obtention du code correct [1].

### 6. Une synthèse critique et les implications pratiques

En synthèse, ce contenu illustre une transition technologique majeure. L'assistance par IA pour les développeurs a dépassé le stade de l'autocomplétion ou du simple chatbot interactif. Les outils comme Claude Code deviennent des gestionnaires de flux de travail asynchrones et massivement parallèles [1, 2].

**Implications pratiques pour l'industrie :**
Le rôle du développeur logiciel est en train de muter de manière fondamentale [2]. Au lieu d'écrire des lignes de code une à une, l'ingénieur de demain s'apparentera davantage à un chef d'orchestre ou un gestionnaire de systèmes. Ses compétences clés consisteront à formuler des instructions claires (prompts avec "think"), à écrire des tests rigoureux pour que les agents puissent s'auto-évaluer, et à concevoir des architectures où des centaines d'agents (via `/batch` ou Git worktrees) pourront intervenir simultanément sans créer de conflits [1]. La possibilité de laisser des agents gérer l'intégration continue (auto rebase, auto PR) pendant une semaine entière, et de valider les permissions critiques via WhatsApp depuis son smartphone [1], promet d'accélérer drastiquement les cycles de développement tout en libérant l'humain des tâches de maintenance les plus répétitives.

## 💼 Post LinkedIn

Fini le pair programming avec un simple assistant IA [1].

Boris Cherny, le créateur de Claude Code, vient de dévoiler 15 astuces que presque personne n'utilise au quotidien [2].

La vraie leçon derrière tout ça ?
On ne parle plus de coder plus vite. On parle d'orchestrer des flottes d'agents qui travaillent en parallèle, sans s'arrêter [1].
Un changement de modèle absolu [1].

Quelques pépites pour ton workflow :
→ /loop : Claude code, fait sa propre revue et pousse en production de manière autonome pendant une semaine [2].
→ /batch : Tu lances des dizaines ou des centaines d'agents en simultané sur tes tâches [2].
→ Esc+Esc : Une vraie machine à remonter le temps pour restaurer ton code ou ta conversation à un point précis [2].
→ Hooks vs CLAUDE.md : Un fichier de contexte est respecté à 80%, alors que les hooks t'assurent une exécution à 100% à chaque fois [2].

Le détail qui tue.
Tu peux recevoir les demandes de permission de tes agents sur WhatsApp et tout valider depuis ton téléphone [2].
Tu ne codes plus, tu diriges.

Et toi, quelle est ta technique préférée pour dompter Claude Code ?

#ClaudeCode #AgenticAI #DevTools

## Mots-clés

- **Claude Code**
- **Intelligence artificielle agentique**
- **Développement logiciel automatisé**
- **Fonctionnalités de programmation**
- **Orchestration d'agents IA**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.linkedin.com/posts/dr-axel-schell-7b2792158_claudecode-agenticai-anthropic-share-7445737394030592000-eF0H?utm_source=share&utm_medium=member_android&rcm=ACoAABVFmSQB_1DLOTmJwsRT2PNC0hrNEP6ztIA)
