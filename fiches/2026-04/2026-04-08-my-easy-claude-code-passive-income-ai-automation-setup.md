---
title: My Easy Claude Code Passive Income AI Automation Setup
source_url: "https://youtu.be/3hioz8dlTFs?is=Ai7AnXABd1KO-hXG"
source_type: article
date_captured: "2026-04-08T17:50:40.641Z"
date_processed: "2026-04-08T17:51:56.544Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1491495509695922276"
status: published
notebooklm_notebook_id: eea0382d-c943-416b-a20b-4427b9f9b5aa
notebooklm_source_id: ec638413-81c8-401a-8d91-bd0f1d7a0c44
notebooklm_url: "https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa"
keywords:
  - Claude Code Automation
  - Revenu passif IA
  - Boucles While Bash
  - Programmes Bug Bounty
  - Intégration de compétences (Skills)
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales
La vidéo issue de la chaîne YouTube "All About AI" présente une méthode permettant de générer des revenus passifs en utilisant "Claude Code", un outil d'intelligence artificielle [1]. L'idée principale repose sur la création de petites automatisations (ou "skills") qui s'exécutent en boucle de manière autonome dans un terminal [1, 2]. Le créateur explique qu'en raison de récents changements liés aux applications tierces, il est devenu pertinent d'utiliser directement les fonctionnalités natives de Claude Code via des sessions sans interface graphique (headless) pour garantir la stabilité du système [1]. L'objectif est de montrer comment, avec un peu de créativité, des tâches simples peuvent être automatisées pour surveiller des données en ligne et générer un profit régulier [2, 3].

### 2. Les différents points de vue ou arguments présentés
L'auteur défend l'idée que l'automatisation par l'IA n'a pas besoin d'être excessivement complexe pour être rentable. Il souligne qu'une simple boucle d'exécution peut rapporter entre 100 $ et 200 $ par semaine, bien que cela nécessite une certaine créativité initiale pour trouver la bonne niche [3]. Il argumente également en faveur de l'utilisation des commandes natives de Claude (comme la commande `claude -p`) plutôt que des solutions tierces non officielles (comme "open claw"), car ces dernières risquent de violer les conditions d'utilisation d'Anthropic [4, 5]. Enfin, il présente cette approche comme étant très accessible : même si l'utilisateur ne sait pas coder la compétence, il peut demander à Claude de lire sa propre documentation pour s'auto-configurer [6].

### 3. Les détails techniques, exemples concrets et données mentionnées
Le système technique repose sur une boucle bash très simple exécutée dans le terminal : `while true; do claude -p /nom_du_skill; sleep 60; done` [1, 7, 8]. Cette commande lance une requête structurée, attend un délai défini (ici 60 secondes), puis recommence [1, 7]. Les compétences (skills) sont stockées sous forme de fichiers Markdown (ex: `autocali.md` ou `automail.md`) qui contiennent des instructions étape par étape [2, 6, 9].

Le créateur illustre son propos avec deux exemples concrets :
*   **Le programme de Bug Bounty "Cali"** : Un script surveille un marché de prédictions pour y déceler des bugs. Les rémunérations varient selon la gravité : 25 $ (mineur), 50 $ (modéré), 100 $ (sévère) et un bonus de 10 $ pour les bugs de pré-listing [2, 3]. Le système est 100 % autonome et envoie un e-mail au support dès qu'une faille est détectée [2].
*   **L'agrégateur Hacker News** : Un tutoriel en direct où Claude est chargé de récupérer les 5 meilleurs articles de Hacker News (via un script Python générant un fichier `news.json`) et de les envoyer par e-mail à l'aide d'un jeton d'authentification Gmail [8, 10-12]. 

Un détail technique crucial mentionné est la nécessité de modifier le fichier `settings.json` de Claude Code pour autoriser l'exécution automatique des commandes bash sans confirmation manuelle de l'utilisateur [12].

### 4. Les problèmes, défis ou limitations identifiés
Bien que le système soit présenté comme "facile", plusieurs défis sont identifiés. Tout d'abord, l'aspect financier n'est pas garanti : si certains projets rapportent de l'argent, le créateur admet que d'autres peuvent en faire perdre [2]. De plus, la mise en place demande de la créativité pour identifier des opportunités viables [3]. 

Sur le plan technique, l'automatisation peut générer des comportements indésirables si elle est mal calibrée. Par exemple, lors du test en direct, le script a envoyé cinq e-mails séparés au lieu d'un seul e-mail regroupant les cinq articles [13]. Un autre problème soulevé est la fréquence d'exécution : une boucle réglée sur 60 secondes est souvent trop agressive, ce qui entraîne la récupération redondante des mêmes données [13]. Enfin, l'évolution constante des outils tiers liés à l'IA oblige à s'adapter en permanence pour maintenir les scripts fonctionnels [1].

### 5. Les solutions, recommandations ou perspectives proposées
Pour pallier ces limitations, le créateur propose plusieurs solutions pratiques. Pour éviter le spam et la redondance, il recommande d'ajuster le délai de la boucle, par exemple en remplaçant `sleep 60` par `sleep 3600` afin d'exécuter le script une fois par heure (soit 3600 secondes) [4, 13]. 

Pour faciliter la création des fichiers de configuration, il suggère une astuce de "méta-prompting" : utiliser la commande `fetch` pour que Claude aille lire la documentation officielle d'Anthropic sur la création de "skills", puis lui demander de générer lui-même le modèle de base (placeholder) du script [6]. Enfin, il insiste sur l'importance de structurer les fichiers de compétences de manière très séquentielle (Étape 1, Étape 2, etc.) afin que l'IA exécute la tâche de manière identique à chaque itération [9].

### 6. Une synthèse critique et les implications pratiques
En synthèse, ce contenu démontre comment les grands modèles de langage, couplés à des outils en ligne de commande comme Claude Code, démocratisent l'accès à l'automatisation avancée et au "web scraping" intelligent. L'implication pratique majeure est qu'il n'est plus nécessaire d'être un ingénieur logiciel chevronné pour créer des robots de surveillance (bots) capables d'interagir avec des API, de lire des journaux de données ou d'envoyer des e-mails automatisés [2, 11, 14]. 

Toutefois, le terme "revenu passif" doit être nuancé. Bien que l'exécution soit autonome, la conception, le débogage (comme l'ajustement des envois d'e-mails) et la recherche de niches rentables (comme les programmes de bug bounty spécifiques) exigent un travail actif et une veille technologique constante [3, 13]. En respectant les environnements d'exécution natifs de Claude pour éviter les violations de conditions d'utilisation, cette méthode offre une base solide pour quiconque souhaite explorer l'automatisation personnelle ou la création de micro-services rentables [4, 5].

## 💼 Post LinkedIn

Générer 100$ à 200$ par semaine en 100% passif avec l'IA ? C'est le petit système que je viens de découvrir [1].

On pense souvent qu'il faut des usines à gaz. Faux.
Un simple terminal. Une boucle. Et c'est tout.

La solution s'appuie sur des sessions Claude Code qui tournent discrètement en arrière-plan [2].

Comment ça fonctionne concrètement ?

→ Tu crées une compétence IA spécifique dans un fichier markdown [3].
→ Tu lances une simple commande "while true" dans ton terminal [2].
→ Ton bot s'exécute de façon autonome toutes les 60 secondes ou chaque heure [4, 5].

Le cas d'usage le plus malin ?
Scanner en continu des marchés de prédiction pour trouver des bugs informatiques [1, 6].
Dès qu'une anomalie apparaît, le système envoie un email au support. Résultat : entre 25$ et 100$ empochés par faille signalée [6].

Ça marche aussi très bien pour notre veille.
Tu peux configurer le script pour récupérer les 5 meilleurs articles Hacker News et te les envoyer directement par mail [7, 8].

Propre, sans infraction aux règles d'utilisation des plateformes [5].

Et toi, quelle tâche ultra-répétitive vas-tu automatiser aujourd'hui depuis ton terminal ?

#IntelligenceArtificielle #Automatisation #ClaudeCode

## Mots-clés

- **Claude Code Automation**
- **Revenu passif IA**
- **Boucles While Bash**
- **Programmes Bug Bounty**
- **Intégration de compétences (Skills)**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://youtu.be/3hioz8dlTFs?is=Ai7AnXABd1KO-hXG)
