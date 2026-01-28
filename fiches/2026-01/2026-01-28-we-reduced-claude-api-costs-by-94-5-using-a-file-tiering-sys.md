---
title: "We reduced Claude API costs by 94.5% using a file tiering system (with proof) : r/ClaudeAI"
source_url: "https://www.reddit.com/r/ClaudeAI/s/Yd05o1Sj4J"
source_type: article
date_captured: "2026-01-28T18:21:36.841Z"
date_processed: "2026-01-28T18:22:41.208Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1466136146303123560"
status: published
notebooklm_notebook_id: c4dba600-dd91-4027-ba33-8ad93f971a31
notebooklm_source_id: 1d228dea-8320-4a4d-8a65-f8baab89511c
notebooklm_url: "https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31"
keywords:
  - API cost reduction
  - File tiering system
  - Token optimization
  - Claude context management
  - Documentation efficiency
---

## Résumé (NotebookLM)

Voici un rapport détaillé analysant la discussion et le projet présentés sur le subreddit r/ClaudeAI concernant l'optimisation des coûts de l'API Claude.

# Rapport d’Analyse : Optimisation des Coûts API Claude via la Hiérarchisation des Fichiers

### 1. Le Contexte et les Idées Principales

Le fil de discussion principal porte sur une problématique centrale pour les développeurs utilisant des LLM (Large Language Models) via API : le coût élevé lié à la consommation de "tokens" lors de l'envoi de contextes volumineux [1].

L'auteur du post (jantonca) présente une solution open-source nommée **cortex-tms**, conçue pour réduire drastiquement ces coûts. L'idée fondatrice est que la majorité des fichiers d'un projet (documentation archivée, changelogs, vieux sprints) sont rarement nécessaires pour une tâche donnée, mais que Claude les "lit" et les facture quand même s'ils sont inclus dans la fenêtre contextuelle [1, 2].

Le concept clé proposé est un **système de hiérarchisation des fichiers (File Tiering System)** inspiré de la gestion des données (Hot/Warm/Cold storage). L'objectif est de ne charger par défaut que ce qui est strictement nécessaire, traitant la base de code comme un "bureau" (fichiers actifs) plutôt qu'une "armoire à archives" [2, 3].

### 2. Les Différents Points de Vue et Arguments

L'analyse des échanges révèle plusieurs courants de pensée :

*   **L'Approche "Ingénierie du Contexte" (L'Auteur) :** L'auteur défend une approche pragmatique où l'on garde tout l'historique dans le dépôt (y compris les rétrospectives et décisions de design), mais où l'on utilise un outil pour masquer dynamiquement ce contenu au LLM. Il argue que cela permet de conserver le contexte historique sans polluer le contexte actif ni gonfler la facture [3].
*   **La Critique de l'Hygiène du Code (Sceptiques) :** Un contre-argument fort est porté par l'utilisateur *unwitty*, qui suggère que les économies annoncées (94,5 %) sont artificielles. Selon lui, le dépôt de l'auteur est rempli de "déchets" inutiles (vieux sprints, archives). Il compare cette méthode à "commander six desserts, en manger un seul, et prétendre avoir réduit son apport calorique de 94,5 %" [4]. Pour ces critiques, la solution est de nettoyer le dépôt, pas de créer un filtre complexe.
*   **L'Approche "Documentation Vivante" (Alternative) :** D'autres utilisateurs, comme *RumLovingPirate*, proposent une philosophie différente basée sur le "Journaling". Au lieu de trier des fichiers, ils demandent à l'IA de maintenir elle-même des documents de synthèse (roadmaps, journaux de bord) de moins de 200 lignes. L'IA s'appuie alors sur ces résumés plutôt que sur le code brut pour comprendre le contexte [5, 6].

### 3. Détails Techniques, Exemples Concrets et Données

Le rapport fournit des données précises issues du "dogfooding" (test interne) de l'outil sur le projet *cortex-tms* :

*   **Le Système de Tiers :**
    *   **HOT (Chaud) :** Tâches actives et travail en cours (environ 3 647 tokens). Chargé par défaut [2].
    *   **WARM (Tiède) :** Modèles (patterns), glossaire, docs récentes (environ 10 419 tokens). Chargé si nécessaire [2].
    *   **COLD (Froid) :** Archives, vieux sprints, changelogs (environ 52 768 tokens). Presque jamais chargé [2].
*   **Résultats Financiers et Techniques :**
    *   **Réduction de tokens :** Passage de 66 834 tokens (sans tri) à 3 647 tokens (avec tri), soit une baisse de **94,5 %** [7].
    *   **Coût par session :** Pour le modèle Claude Sonnet 4.5, le coût passe de 1,20 $ (équivalent GPT-4 sans tri) ou 0,11 $ (prix optimisé) à environ 0,01 $ par session [7]. L'auteur précise que son calcul de 0,11 $ correspond à une requête unique en entrée (input tokens) [8].
*   **Implémentation :** L'outil utilise des balises manuelles dans le code, par exemple `<!-- @cortex-tms-tier HOT -->`, et une interface en ligne de commande (CLI) pour valider les tiers [7].

### 4. Problèmes, Défis et Limitations Identifiés

Plusieurs limitations ont été soulevées lors de la discussion :

*   **La Gestion Manuelle :** La nécessité de "taguer" manuellement chaque fichier ou section est vue comme une friction. Un utilisateur demande : "Dois-je taguer les fichiers et mettre à jour les tags manuellement ?" [9].
*   **Risque de Confidentialité et Pertinence :** L'inclusion de "rétrospectives de sprint" (souvent émotionnelles et candides) dans le codebase, même en catégorie COLD, est jugée risquée et étrange par certains développeurs, qui estiment que ces sentiments humains ne devraient pas être immortalisés dans le code [4].
*   **Complexité vs Nettoyage :** Comme mentionné plus haut, le système pallie potentiellement une mauvaise gestion des archives plutôt que de résoudre le problème à la source (supprimer les fichiers obsolètes) [10].

### 5. Solutions, Recommandations et Perspectives

Pour répondre aux limitations, plusieurs pistes d'amélioration et alternatives ont été proposées :

*   **Automatisation via Git :** L'idée la plus populaire pour le futur est d'utiliser l'historique Git pour déterminer automatiquement la "chaleur" d'un fichier. Les fichiers modifiés récemment seraient automatiquement "HOT", évitant le taggage manuel [11, 12].
*   **Architecture RAG (Retrieval-Augmented Generation) :** L'auteur et d'autres utilisateurs envisagent de faire évoluer le système vers une architecture RAG ou l'utilisation de serveurs MCP (Model Context Protocol). Cela permettrait de stocker les données WARM/COLD dans une base vectorielle et de ne récupérer que les fragments pertinents, dépassant ainsi la simple sélection de fichiers [13, 14].
*   **Alternatives Structurelles :**
    *   Utiliser des fichiers de configuration JSON ou `.gitattributes` à la racine pour gérer les tiers au lieu de polluer le code avec des balises [10, 15].
    *   Utiliser des noms de fichiers sémantiques et demander à Claude de lister les répertoires (`ls`) pour découvrir seul le contexte pertinent [11].

### 6. Synthèse Critique et Implications Pratiques

Cette étude de cas illustre une transition importante dans le développement assisté par IA. Nous passons d'une ère où l'on "bourrait" le contexte (profitant des fenêtres de 200k+ tokens) à une ère d'**optimisation contextuelle**.

**Implications Pratiques :**
1.  **Économie :** Pour les entreprises utilisant l'API à grande échelle, la réduction de 90 % du contexte inutile est impérative, non seulement pour le coût direct, mais aussi pour la latence et l'empreinte carbone [16].
2.  **Qualité :** Réduire le bruit (fichiers obsolètes) améliore la qualité des réponses de l'IA, car elle se concentre sur la documentation à jour [16].
3.  **Cache :** Ce système optimise l'utilisation du "Prompt Caching" d'Anthropic. En gardant le tier WARM stable et le tier HOT petit, on maximise les chances de réutiliser le cache (cache hit), réduisant encore les coûts [17].

**Conclusion Critique :**
Bien que l'outil *cortex-tms* soit une solution ingénieuse, la critique sur l'hygiène du dépôt reste valide. L'outil est particulièrement utile pour les projets "legacy" ou les documentations lourdes, mais ne doit pas servir d'excuse pour conserver des archives inutiles dans un dépôt de code actif. L'avenir de cette méthode réside probablement dans son automatisation (via Git) et son intégration avec des protocoles comme MCP, rendant le tri transparent pour le développeur.

## Mots-clés

- **API cost reduction**
- **File tiering system**
- **Token optimization**
- **Claude context management**
- **Documentation efficiency**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/ClaudeAI/s/Yd05o1Sj4J)
