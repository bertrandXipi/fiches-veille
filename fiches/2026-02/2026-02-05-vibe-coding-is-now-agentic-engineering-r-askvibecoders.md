---
title: "Vibe coding is now \"agentic engineering\" : r/AskVibecoders"
source_url: "https://www.reddit.com/r/AskVibecoders/s/GUFoh1oqkx"
source_type: article
date_captured: "2026-02-05T13:51:38.933Z"
date_processed: "2026-02-05T13:52:29.341Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1468967310269223016"
status: published
notebooklm_notebook_id: 5ac37432-e593-4bb7-b761-a4301800efc4
notebooklm_source_id: cbec2f04-f702-4b7a-8782-2f4fa1008260
notebooklm_url: "https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4"
keywords:
  - Agentic engineering
  - Vibe coding
  - Agents LLM
  - Développement logiciel
  - Supervision humaine
---

## Résumé (NotebookLM)

Voici un rapport détaillé analysant le contenu des discussions sur le « Vibe Coding » et l'émergence de l'« Agentic Engineering », basé sur les sources fournies.

***

# Rapport sur l'Évolution du Développement Assisté par IA : Du « Vibe Coding » à l'« Agentic Engineering »

### 1. Le contexte et les idées principales

Le cœur des discussions analysées repose sur une rétrospective publiée par Andrej Karpathy, un an après son tweet viral sur le « vibe coding » (codage à l'instinct ou à l'ambiance) [1]. Le concept initial de *vibe coding* décrivait une manière de programmer décontractée, rendue possible par l'intelligence artificielle, où l'utilisateur déléguait l'écriture du code à une IA en acceptant le résultat sans trop de vérification, principalement pour des projets jetables ou ludiques [2].

Cependant, le contexte technologique a évolué. La capacité des grands modèles de langage (LLM) a augmenté au point où la programmation via des agents IA devient un flux de travail par défaut pour les professionnels [2]. Karpathy propose donc une nouvelle terminologie : l'**« Agentic Engineering »** (ingénierie agentique).

L'idée principale est de distinguer deux approches :
1.  **Vibe Coding :** Une approche « accepter tout et espérer le meilleur », ludique et rapide [2].
2.  **Agentic Engineering :** Une approche professionnelle où l'humain orchestre des agents avec une surveillance stricte pour obtenir un effet de levier sans compromettre la qualité du logiciel [2].

### 2. Les différents points de vue ou arguments présentés

Les sources révèlent une fracture nette dans la communauté entre l'usage récréatif et l'usage professionnel, ainsi qu'un débat sur la terminologie.

*   **La légitimité professionnelle :** Plusieurs intervenants soutiennent le changement de nom. L'argument est que « vibe coding » sonne peu sérieux (« comme si vous étiez défoncé »), tandis que « agentic engineering » semble être une compétence employable et crédible pour les entreprises [3, 4].
*   **Le scepticisme sémantique :** Certains utilisateurs perçoivent ce changement comme un simple « rebranding » ou un terme plus chic pour désigner la même activité. Pour eux, qu'on l'appelle *vibe coding* ou *agentic engineering*, le processus reste le même : décrire ce que l'on veut et corriger l'IA [5].
*   **La distinction par l'usage :** Un point de vue nuancé émerge, suggérant que les deux termes coexistent légitimement mais s'appliquent à des contextes différents. Le week-end est propice au *vibe coding* (projets personnels sans contrainte), tandis que la semaine de travail exige de l'ingénierie agentique (rigueur, maintenance) [4].
*   **La compétence perçue :** Il est suggéré que les véritables gagnants de cette évolution ne sont pas les débutants, mais les ingénieurs seniors capables de superviser le code, alors que le *vibe coding* pourrait être une « impasse » pour les juniors [6, 7].

### 3. Les détails techniques, exemples concrets et données mentionnées

Les discussions fournissent des exemples précis illustrant la différence technique entre les deux modes de fonctionnement :

*   **Scénario « Vibe Coding » :**
    *   **Cas d'usage :** Création d'un clone de l'application « Superwhisper », petits outils personnels, musique ou projets de week-end [4].
    *   **Méthode :** L'utilisateur se soucie peu de la maintenabilité à long terme. Si un bug survient, il demande simplement à l'IA (comme Claude) de lire les logs et de se débrouiller. L'objectif est d'avoir quelque chose qui fonctionne immédiatement pour un usage personnel [4].
    *   **Flux :** « Vibes Guaranteed » (Ambiances garanties), peu de contrôle sur la structure interne [4].

*   **Scénario « Agentic Engineering » :**
    *   **Cas d'usage :** Environnement professionnel complexe, gestion d'un « monorepo » intégrant plusieurs langages (TypeScript, PHP, Python) et plusieurs serveurs communiquant entre eux [8].
    *   **Méthode :** Développement piloté par des spécifications (*spec-driven development*). L'ingénieur doit faire effectuer des recherches dans la base de code par l'IA pour chaque tâche.
    *   **Contrainte :** L'humain doit corriger l'IA 90 % du temps car celle-ci tend à « réinventer la roue » plutôt que de modifier le code existant [8].
    *   **Rôle :** L'humain n'écrit plus le code directement 99 % du temps, mais agit comme un superviseur et un architecte [3].

### 4. Les problèmes, défis ou limitations identifiés

Malgré l'enthousiasme, plusieurs limites critiques sont identifiées dans les sources :

*   **Qualité et maintenance du code :** Le *vibe coding* est associé à la production de code « sale » ou à l'expédition de bugs tard dans la nuit (« shipping bugs at 2am ») [9]. Il y a une inquiétude croissante concernant la dette technique générée par du code écrit sans rigueur [10].
*   **Intégration dans l'existant :** L'IA peine encore à s'intégrer fluidement dans des bases de code existantes et complexes sans une supervision humaine lourde. Elle manque souvent de contexte global pour réutiliser efficacement les composants existants [8].
*   **Risque professionnel :** L'apparition de termes comme « spécialistes du nettoyage de vibe coding » sur LinkedIn suggère que cette pratique crée des dégâts que des ingénieurs doivent ensuite réparer [10]. De plus, il existe une crainte que cette approche soit un piège pour les débutants qui n'apprennent pas les fondamentaux [7].
*   **Addiction et culture :** Certaines sources mentionnent le *vibe coding* comme une « addiction », soulignant un changement culturel où l'on oublie presque que le code existe pour se concentrer uniquement sur le résultat immédiat [11, 12].

### 5. Les solutions, recommandations ou perspectives proposées

Pour transformer l'usage de l'IA en une pratique durable, les recommandations suivantes émergent :

*   **Adopter la rigueur de l'ingénierie :** Il est recommandé de passer d'une posture passive (« accepter tout ») à une posture active de surveillance et de contrôle qualité [2]. L'« Agentic Engineering » est présenté comme une discipline avec de la profondeur, une compétence qui s'apprend et se perfectionne [3].
*   **Développement piloté par les spécifications :** Dans un cadre professionnel, il est crucial de fournir à l'agent un contexte précis et des spécifications claires, et de le forcer à analyser la base de code existante avant de générer du nouveau code [8].
*   **Nouveaux rôles professionnels :** Le marché semble s'orienter vers des rôles de supervision. On ne cherche plus seulement des codeurs, mais des personnes capables d'orchestrer des agents [3] ou de nettoyer le code généré par l'IA [10].
*   **Distinction claire des contextes :** Il est implicitement conseillé de réserver le *vibe coding* au prototypage rapide ou aux loisirs, et d'appliquer les principes *agentiques* pour tout logiciel destiné à la production ou à la maintenance [4].

### 6. Une synthèse critique et les implications pratiques

L'analyse de ces sources indique que le développement logiciel traverse une phase de transition majeure. Le terme « Vibe Coding », bien que populaire et évocateur de la facilité créative offerte par l'IA [1, 11], devient insuffisant pour décrire l'intégration de ces outils dans des processus industriels sérieux.

**Implications pratiques :**
1.  **Évolution du métier :** Le développeur évolue vers un rôle de chef d'orchestre. La compétence clé n'est plus la syntaxe, mais la capacité à évaluer la qualité du travail de l'IA, à définir des architectures et à déboguer des systèmes complexes [3, 5].
2.  **Marché de l'emploi :** L'adoption du terme « Agentic Engineering » par des figures comme Karpathy signale une professionnalisation. Les entreprises chercheront probablement des profils capables de démontrer une maîtrise « agentique » plutôt que de simples utilisateurs d'outils génératifs [3, 10].
3.  **Dette technique :** Une adoption naïve du *vibe coding* en entreprise risque d'accélérer la dette technique, nécessitant des interventions coûteuses de refactorisation a posteriori. La rigueur de l'ingénierie agentique est la réponse proposée à ce risque [2, 8].

En conclusion, si le *vibe coding* a démocratisé la création logicielle par le plaisir et la rapidité, l'« agentic engineering » tente de restaurer la structure et la fiabilité nécessaires à la pérennité des systèmes informatiques.

## Mots-clés

- **Agentic engineering**
- **Vibe coding**
- **Agents LLM**
- **Développement logiciel**
- **Supervision humaine**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/AskVibecoders/s/GUFoh1oqkx)
