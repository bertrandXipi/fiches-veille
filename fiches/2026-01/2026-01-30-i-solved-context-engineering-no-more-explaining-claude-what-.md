---
title: "I solved context engineering, no more explaining Claude what my app does : r/vibecoding"
source_url: "https://www.reddit.com/r/vibecoding/s/wAPk3ypjsJ"
source_type: article
date_captured: "2026-01-30T21:33:04.845Z"
date_processed: "2026-01-30T21:33:49.102Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1466909106110726480"
status: published
notebooklm_notebook_id: c4dba600-dd91-4027-ba33-8ad93f971a31
notebooklm_source_id: 313c163c-c8df-4d76-a404-31e72e553727
notebooklm_url: "https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31"
keywords:
  - Context engineering
  - Vibe coding
  - Claude Code
  - MCP integration
  - AI ticket generation
---

## Résumé (NotebookLM)

Voici une analyse approfondie et structurée du contenu du fil de discussion Reddit intitulé "I solved context engineering, no more explaining Claude what my app does".

### 1. Contexte et Idées Principales

Le fil de discussion principal émane d'un développeur expérimenté ("senior dev") identifié sous le pseudonyme **Icy-Physics7326**, qui partage son expérience sur le développement d'applications complètes assisté par l'IA, une pratique souvent appelée "vibe coding" [1, 2].

L'idée centrale repose sur la résolution d'un obstacle majeur dans le développement assisté par les LLM (Large Language Models) comme Claude : la **perte de contexte** ("context loss"). L'auteur explique que si la programmation conversationnelle fonctionne pour de petits scripts, elle échoue à mesure que les projets grandissent [2]. Le modèle oublie les décisions passées, ne scanne pas l'intégralité du code et perd le fil des spécifications techniques au fil des sessions [3].

Pour pallier cela, l'auteur a créé un outil nommé **Scope**, conçu pour structurer et ingérer le contexte du projet de manière dynamique, transformant ainsi l'interaction avec l'IA d'une simple conversation à une ingénierie de contexte rigoureuse [3, 4].

### 2. Les Différents Points de Vue et Arguments

Le rapport met en lumière une tension entre les méthodes traditionnelles de "vibe coding" et une approche plus structurée.

*   **Le point de vue de l'auteur :** Il argumente que la méthode courante consistant à maintenir manuellement des fichiers de documentation (comme `CLAUDE.md`) est inefficace car ces fichiers deviennent rapidement obsolètes ("stale") [3]. Il soutient que l'IA travaille nettement mieux avec un contexte structuré (tickets, spécifications précises) qu'avec une documentation en texte libre [4].
*   **La réaction de la communauté :** Les retours sont très positifs et valident le problème identifié. L'utilisateur **ederrabelo** mentionne qu'il devenait "fou" à force de copier-coller du contexte entre différents outils comme Manus, Lovable ou GPT coder, et voit un grand potentiel dans une solution qui centralise cet état [5].
*   **L'évolution du développement :** Un autre commentaire suggère que le "spec driven development" (développement piloté par les spécifications) pourrait devenir la nouvelle norme ("meta") avec des modèles avancés comme Claude 4.5 [6]. Cela indique un changement de paradigme où le développeur se concentre sur la définition des besoins plutôt que sur l'écriture du code.

### 3. Détails Techniques, Exemples Concrets et Données

L'auteur fournit une description précise de la stack technique et de la méthodologie utilisée pour construire sa solution "Scope" :

*   **La Stack Technologique :**
    *   **Claude Code :** Utilisé pour construire l'application elle-même [7].
    *   **Codex :** Utilisé pour tester et donner du feedback sur l'intégration MCP [7].
    *   **Qdrant :** Une base de données vectorielle utilisée pour la recherche sémantique sur le contexte du projet [7].
    *   **Anthropic API :** Utilisée pour la génération des tickets [7].

*   **Mécanisme de Fonctionnement (MCP) :**
    L'innovation clé réside dans l'utilisation du **MCP (Model Context Protocol)**. Au lieu de copier-coller des instructions, l'IA "interroge" directement le projet via ce protocole [4].
    *   *Exemple concret :* Au lieu que le développeur doive taper manuellement le contexte technique à chaque requête, Claude peut extraire automatiquement : "Rails 7, PostgreSQL, JWT auth, ticket 4 of 12" [3].

*   **Processus de "Dogfooding" :**
    L'auteur a utilisé l'IA pour construire l'outil destiné à l'IA. Il demandait constamment à Claude et Codex : "Ce contexte est-il utile ? Qu'est-ce qui manque ?". Il a itéré sur le format de sortie du MCP jusqu'à ce que les modèles confirment que c'était supérieur aux fichiers statiques [7].

### 4. Problèmes, Défis et Limitations Identifiés

L'analyse du contenu révèle plusieurs défis inhérents à l'utilisation actuelle des LLM pour le codage :

*   **La "Context Compaction" :** L'auteur note que les modèles ont tendance à "compresser silencieusement" le contexte, ce qui conduit à l'oubli de décisions importantes prises plus tôt dans le projet [3].
*   **Les Hallucinations et Duplications :** Sans un contexte clair, Claude a tendance à reconstruire des fonctionnalités qui existent déjà ("duplicate features") car il ne scanne pas tout le code [3]. L'auteur cite un exemple frappant où Claude a construit une "v2" entière de son API sans le lui dire, simplement parce qu'il avait oublié les endpoints existants [2].
*   **La Maintenance Manuelle :** La limitation principale des approches actuelles est la charge cognitive imposée au développeur, qui doit réexpliquer son application à chaque nouvelle session ("Every new session I'd re-explain my app") [2].

### 5. Solutions, Recommandations et Perspectives

La solution proposée, **Scope**, et les recommandations qui en découlent se structurent autour de l'automatisation du contexte :

*   **Approche par "Wizard" et Tickets :** La solution capture les besoins initiaux via un questionnaire adaptatif ("Wizard"), puis génère des tickets structurés contenant des critères d'acceptation et des dépendances claires [3, 4].
*   **Suivi de la Progression :** L'outil maintient un état de ce qui est fait et de ce qui reste à faire, empêchant l'IA de se perdre ou de tourner en rond [4].
*   **Recommandation Clé :** L'auteur conclut que des tickets avec un périmètre clair ("clear scope") réduisent drastiquement les hallucinations de l'IA [4].
*   **Perspective d'Avenir :** L'intégration via MCP est présentée comme une technologie sous-estimée pour maintenir l'état d'un projet à travers plusieurs sessions de travail [4].

### 6. Synthèse Critique et Implications Pratiques

Ce rapport met en évidence une maturation de l'usage de l'IA dans le développement logiciel. On passe d'une phase exploratoire et conversationnelle ("vibe coding") à une phase d'ingénierie plus rigoureuse.

**Implications Pratiques :**
Pour les développeurs utilisant des outils comme Claude Code, ce retour d'expérience suggère que la qualité du code généré dépend moins du "prompting" instantané que de la gestion de l'architecture de l'information (Context Engineering). L'utilisation de bases de données vectorielles (comme Qdrant) et de protocoles standardisés (MCP) pour nourrir l'IA semble être la voie à suivre pour dépasser le stade des scripts simples et construire des applications complexes et maintenables.

**Critique :**
Bien que la solution semble efficace, elle souligne une lacune actuelle des modèles : leur incapacité à gérer nativement la mémoire à long terme d'un projet complexe sans outils externes. Le besoin de créer un outil tiers pour "rappeler" à Claude ce qu'il a codé la veille démontre que nous sommes encore dans une phase intermédiaire de l'assistance au développement par IA, où l'humain doit orchestrer la mémoire de la machine.

## Mots-clés

- **Context engineering**
- **Vibe coding**
- **Claude Code**
- **MCP integration**
- **AI ticket generation**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/vibecoding/s/wAPk3ypjsJ)
