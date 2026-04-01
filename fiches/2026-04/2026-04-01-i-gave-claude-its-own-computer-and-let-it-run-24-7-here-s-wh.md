---
title: "I gave Claude its own computer and let it run 24/7. Here's what it built. : r/ClaudeAI"
source_url: "https://www.reddit.com/r/ClaudeAI/s/Nz5m9AWZzS"
source_type: article
date_captured: "2026-04-01T00:55:52.898Z"
date_processed: "2026-04-01T00:57:29.767Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1488703411435081819"
status: published
notebooklm_notebook_id: eea0382d-c943-416b-a20b-4427b9f9b5aa
notebooklm_source_id: 51189a16-52ec-43b5-8a81-b1674b4e1e8d
notebooklm_url: "https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa"
keywords:
  - Phantom, agent autonome
  - Évolution par IA
  - Mémoire vectorielle persistante
  - Validation entre modèles
  - Création d'outils runtime
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales

Un utilisateur de la plateforme Reddit a développé et rendu open source un projet innovant nommé "Phantom" [1, 2]. L'idée centrale de ce projet est de s'affranchir des sessions éphémères des modèles de langage habituels. Au lieu d'avoir un assistant virtuel qui oublie tout son contexte lorsque l'onglet du terminal est fermé, Phantom offre au modèle d'intelligence artificielle Claude (Opus 4.6) sa propre machine dédiée pour fonctionner en continu, 24 heures sur 24 et 7 jours sur 7 [2]. L'agent devient ainsi autonome et dispose d'une mémoire vectorielle persistante (via Qdrant), de la capacité de créer ses propres outils, et d'un moteur pour évoluer par lui-même [2-4]. 

### 2. Les différents points de vue ou arguments présentés

Dans les commentaires, la communauté se montre extrêmement impressionnée par le projet, saluant tout particulièrement les comportements émergents et proactifs de l'IA [5]. Cependant, le débat a rapidement porté sur les coûts d'exécution [5]. Plusieurs utilisateurs se sont montrés sceptiques face à l'affirmation de l'auteur indiquant que son système coûtait environ 20 $ par mois ; l'un d'eux a même signalé avoir dépensé 5 $ en seulement dix minutes d'essai [6, 7]. L'auteur a réfuté ces inquiétudes en révélant que l'économie reposait sur l'utilisation d'un abonnement "Max", plutôt que sur la facturation à l'usage par clé API [6]. Un autre point de vue récurrent est la comparaison avec "OpenClaw", un système concurrent [6]. L'auteur argumente que Phantom est fondamentalement différent : là où OpenClaw n'est qu'une passerelle de messagerie réactive avec des outils fixes, Phantom est conçu pour l'amélioration autonome et la création dynamique de ses propres outils au moment de l'exécution [3, 4, 6].

### 3. Les détails techniques, exemples concrets et données mentionnées

D'un point de vue architectural, Phantom est un processus développé en Bun et TypeScript qui enveloppe l'Agent SDK d'Anthropic [2]. L'aspect le plus saillant est son pipeline de "validation croisée" en 6 étapes : pour éviter que le modèle principal (Opus) ne dérive en évaluant son propre travail, c'est un modèle théoriquement "moins puissant" (Sonnet) qui est utilisé comme juge pour évaluer les modifications de configuration proposées par Opus [6, 8]. 

Les résultats concrets de cette architecture sont multiples :
*   **Analyse de données autonome** : Suite à une simple requête, Phantom a installé ClickHouse sur sa machine virtuelle, téléchargé 28,7 millions de lignes de données provenant de Hacker News, généré un tableau de bord, puis a créé une API REST qu'il a automatiquement enregistrée comme outil MCP pour ses sessions futures [4, 9].
*   **Intégration et surveillance** : Sollicité pour communiquer via Discord (qu'il ne supportait pas initialement), l'agent a codé et déployé son propre bot Discord [9]. Il a également découvert un outil de surveillance nommé Vigil, l'a intégré, et a bâti un tableau de bord pour monitorer sa propre infrastructure [8].

### 4. Les problèmes, défis ou limitations identifiés

Malgré ses succès, le projet présente certaines failles et limites [5, 10]. Lors d'une revue de code par la communauté, il a été identifié que le système très loué d'"auto-évolution" (l'évaluation par l'IA Sonnet) était en réalité désactivé par défaut dans le code source au profit d'une méthode heuristique plus basique, un oubli que l'auteur a dû rapidement corriger [6, 10]. 

Le coût reste une limitation technique : le processus d'évolution nécessitait l'utilisation directe du SDK d'Anthropic, ce qui engendrait des frais d'API réels, contrairement à la boucle principale de l'agent qui exploitait intelligemment la connexion de la CLI associée à un abonnement mensuel [11, 12]. 

La gouvernance représente le défi le plus critique. L'autonomie ininterrompue soulève la question de la supervision : un utilisateur s'interroge légitimement sur les risques de laisser une IA modifier des fichiers de manière autonome ou ouvrir des requêtes d'intégration (Pull Requests) à 3 heures du matin sans contrôle humain immédiat [13]. Enfin, Phantom dépend entièrement du seul écosystème d'Anthropic, là où des concurrents comme OpenClaw sont agnostiques et supportent plus de 30 fournisseurs de modèles [14].

### 5. Les solutions, recommandations ou perspectives proposées

Afin de pallier la complexité d'installation et de mise en œuvre, l'auteur a encapsulé l'intégralité du projet dans une image Docker, permettant de démarrer l'agent persistant simplement en ajoutant une clé API, sans avoir à gérer de configurations complexes [15]. Pour optimiser davantage les coûts, des utilisateurs ont suggéré de refactoriser la boucle du système de jugement pour qu'elle utilise également le sous-processus de la CLI de Claude, rendant ainsi le système globalement gratuit en dehors du prix de l'abonnement mensuel [12]. 

En termes de perspectives de développement, les participants au fil de discussion proposent de multiplier les canaux d'intégration, notamment en dotant l'IA de sa propre adresse email via des serveurs IMAP/SMTP ou l'API de Resend, ou encore d'une intégration Telegram [16-18]. Cela lui permettrait d'effectuer de la prospection marketing automatisée ou de devenir un véritable assistant personnel effectuant des vérifications asynchrones à intervalles réguliers [17, 18].

### 6. Une synthèse critique et les implications pratiques

Ce projet illustre une transition fondamentale dans l'interaction avec l'intelligence artificielle, qui passe du statut d'outil réactif à celui de véritable "collègue virtuel" proactif et persistant [15, 19]. La solution consistant à utiliser un modèle tiers (Sonnet) pour superviser le modèle créateur (Opus) constitue une innovation technique remarquable pour enrayer les hallucinations et la dérive cognitive des agents opérant sur le long terme [19, 20].

Sur le plan pratique, les implications de ces agents 24/7 sont considérables. Ils offrent de puissantes perspectives pour des tâches à forte valeur ajoutée mais chronophages, telles que l'analyse quotidienne de dépôts GitHub, la pré-revue de code selon le style du développeur, ou la gestion autonome de campagnes marketing [18, 21]. Toutefois, la sophistication croissante de ces outils exige de repenser nos méthodes de travail. Si la barrière technique pour déployer une IA autonome est drastiquement abaissée, la nécessité de créer des "garde-fous" et des mécanismes de validation humaine stricts devient incontournable pour sécuriser les opérations que ces agents mènent sans supervision [13, 19].

## 💼 Post LinkedIn

Fermer l'onglet de votre IA et lui faire tout oublier, c'est de l'histoire ancienne.

Un développeur vient de donner un ordinateur dédié à Claude pour le laisser tourner 24/7 [1, 2].

Le résultat s'appelle Phantom [2]. Un projet open-source fascinant [2].

Que fait une IA quand on lui donne sa propre machine et une mémoire persistante ?

Elle prend des initiatives inattendues.

→ Elle installe une base de données et analyse 28,7 millions de lignes de data sans aucune directive [3].
→ Elle code sa propre intégration Discord de A à Z juste parce qu'un utilisateur le demande [3].
→ Elle déploie un tableau de bord pour surveiller sa propre infrastructure logicielle [4].
→ Elle s'auto-évalue en utilisant un modèle plus petit pour juger et corriger son propre code [4, 5].

Une autonomie totale. 
Le coût pour faire tourner ce collègue virtuel infatigable ? À peine 20 dollars par mois grâce à une astuce d'abonnement [5, 6].

L'IA n'est plus un simple chat passif. C'est un système qui agit, évolue et exécute des tâches pendant que vous dormez [7].

Sommes-nous prêts à collaborer au quotidien avec des agents 100% autonomes ?

#IntelligenceArtificielle #AgentsIA #Tech

## Mots-clés

- **Phantom, agent autonome**
- **Évolution par IA**
- **Mémoire vectorielle persistante**
- **Validation entre modèles**
- **Création d'outils runtime**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/ClaudeAI/s/Nz5m9AWZzS)
