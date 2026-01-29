---
title: "https://services.google.com/fh/files/misc/google_cloud_future_of_ai_perspectives_for_startups_2025.pdf"
source_url: "https://services.google.com/fh/files/misc/google_cloud_future_of_ai_perspectives_for_startups_2025.pdf"
source_type: article
date_captured: "2026-01-29T06:49:47.913Z"
date_processed: "2026-01-29T06:59:01.967Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1466324433147793604"
status: published
notebooklm_notebook_id: c4dba600-dd91-4027-ba33-8ad93f971a31
notebooklm_source_id: b5bf5fbe-d6dc-4d25-8a2d-da1f12ccef4a
notebooklm_url: "https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31"
keywords:
  - AI Agent Experiences
  - RAG 2.0 Integration
  - Multimodal Frontier Models
  - AI Startup Disruption
  - Bio and Hardware AI
---

## Résumé (NotebookLM)

Voici une analyse approfondie et structurée du rapport « Future of AI: Perspectives for Startups 2025 » publié par Google Cloud.

### 1. Le contexte et les idées principales

Le document est un recueil de perspectives pour l'année 2025, rassemblant les points de vue de dirigeants de Google Cloud et de fondateurs ou investisseurs de premier plan (GV, Greylock, a16z, etc.). L'idée centrale est que l'IA entre dans une nouvelle phase de maturité : nous passons de l'engouement initial pour les modèles de langage (LLM) à une ère d'infrastructure spécialisée, d'agents autonomes et d'applications industrielles concrètes [1, 2].

Le rapport souligne que l'architecture informatique traditionnelle est en train d'être rendue obsolète par les exigences de l'IA générative, nécessitant une densification massive du calcul et des systèmes de refroidissement liquide [3, 4]. Parallèlement, le paysage logiciel évolue vers des « usines logicielles » (software factories) où l'IA ne se contente pas d'assister, mais génère du code de production à partir d'exigences commerciales brutes [5]. L'objectif pour 2025 n'est plus seulement l'efficacité, mais la création de nouveaux revenus (topline growth) et d'expériences impossibles auparavant [6].

### 2. Les différents points de vue ou arguments présentés

Le rapport met en lumière plusieurs débats et divergences d'opinion entre les experts :

*   **Vitesse d'adoption vs Réalité du terrain :** Alors que certains investisseurs comme Elad Gil considèrent que l'IA est encore « sous-médiatisée » (underhyped) et qu'elle n'en est qu'à ses débuts transformateurs [7], d'autres comme Dylan Fox (AssemblyAI) et Jennifer Li (a16z) avertissent que l'adoption généralisée en entreprise sera plus lente que prévu. Ils soutiennent que des problèmes de « dernier kilomètre » (last-mile issues) et d'intégration système complexes doivent être résolus avant que la technologie ne devienne omniprésente [8, 9].
*   **La fin des « LLM Wrappers » :** Il existe un consensus fort sur le fait que les startups qui se contentent d'être une interface légère au-dessus d'un modèle (LLM wrappers) ne survivront pas. David Friedberg et d'autres insistent sur la nécessité de créer un moteur de valeur durable, via la génération de données propriétaires ou des effets de réseau, pour éviter la commoditisation [10, 11].
*   **Agents autonomes vs Humain dans la boucle :** Bien que l'avenir semble se diriger vers des agents autonomes, Harrison Chase (LangChain) reste sceptique sur l'autonomie totale à court terme. Il argumente en faveur de systèmes avec « humain dans la boucle » (human-in-the-loop) pour garantir la fiabilité et permettre au système d'apprendre des interactions [12, 13].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le rapport fournit des détails techniques précis sur l'évolution de la technologie :

*   **Infrastructure et Matériel :** Amin Vahdat de Google décrit une rupture avec le matériel standard. Il mentionne l'importance des réseaux spécialisés comme l'Inter Chip Interconnect (ICI) pour les TPU et NVLink pour les GPU, ainsi que les limites actuelles de la mémoire à haute bande passante (HBM) créant un « mur de mémoire » [14].
*   **Modèles Gemini 2.0 :** Ces modèles sont présentés comme nativement multimodaux (texte, image, audio, vidéo) avec des fenêtres contextuelles allant jusqu'à 2 millions de tokens et des capacités de raisonnement (Thinking model) [15, 16].
*   **Convergence RAG et Long Contexte :** Douwe Kiela (Contextual AI) explique techniquement que le RAG (Retrieval-Augmented Generation) et les modèles à long contexte convergent. Il décrit comment l'attention clairsemée (sparse attention) dans les modèles à long contexte revient fonctionnellement à faire du RAG en ignorant la majorité des tokens non pertinents [17].
*   **Applications concrètes :**
    *   **Biologie et Agriculture :** L'utilisation de « modèles de langage génomiques » (GLMs) permet de prédire des séquences d'ADN pour créer des cultures résistantes ou des médicaments biologiques ciblés [18].
    *   **Web3 et IA :** Des agents IA utilisant des rails de paiement blockchain (stablecoins) pour effectuer des micro-transactions ou gérer des portefeuilles d'investissement de manière autonome [19].

### 4. Les problèmes, défis ou limitations identifiés

Plusieurs obstacles majeurs à la réussite des startups et à l'adoption de l'IA sont identifiés :

*   **Le problème du « Dernier Kilomètre » :** Les modèles fonctionnent bien à 80-90%, mais les 10% restants (fiabilité, gestion des exceptions, hallucinations) bloquent le déploiement en production [20]. Yoav Shoham note que dans l'entreprise, une IA brillante 95% du temps mais qui produit des absurdités 5% du temps est inacceptable [21].
*   **La rétention (Stickiness) :** Crystal Huang (GV) souligne un cycle de « micro-booms et bustes ». Les outils basés sur l'IA sont faciles à adopter mais tout aussi faciles à désinstaller. Il est difficile de créer une valeur durable quand les barrières à l'entrée sont faibles [22].
*   **Évaluation et Benchmarks obsolètes :** Les métriques traditionnelles comme le taux d'erreur de mot (Word Error Rate) ne suffisent plus. Les entreprises investissent sur des métriques trop génériques qui ne reflètent pas la réussite réelle d'un cas d'usage [23].
*   **Coûts et Énergie :** La densité de calcul requise pousse les infrastructures à leurs limites énergétiques, nécessitant une refonte complète des datacenters [4].

### 5. Les solutions, recommandations ou perspectives proposées

Pour surmonter ces défis, les experts proposent des stratégies claires :

*   **L'ajustement Produit-Algo (Product-Algo Fit) :** Au lieu de chercher la perfection du modèle, les entrepreneurs doivent concevoir des produits qui tirent parti des forces de l'IA tout en compensant ses imperfections (incertitudes, hallucinations) [24].
*   **Approche « Software Factory » :** Il faut passer de la vente de logiciels par siège (SaaS classique) à des modèles basés sur la valeur ou le résultat, où l'IA agit comme une usine générant du code ou des services [25, 26].
*   **Infrastructure « Agnostique » :** Construire une infrastructure flexible qui permet de changer de modèles (LLM) facilement, car ces derniers évoluent très vite et deviennent des commodités [27, 28].
*   **Données Propriétaires :** La véritable valeur réside dans les données structurées et non structurées propres à l'entreprise. Utiliser des bases de données vectorielles pour ancrer (grounding) les modèles et réduire les hallucinations est crucial [29].
*   **Passer du « Prompt and Pray » aux Systèmes IA :** Abandonner l'idée qu'un simple prompt suffit. Il faut construire des systèmes complets qui orchestrer plusieurs modèles et outils pour obtenir des résultats fiables [30, 31].

### 6. Une synthèse critique et les implications pratiques

Ce rapport marque une transition psychologique et technique dans l'écosystème IA. Nous quittons la phase de découverte magique pour entrer dans une phase d'ingénierie rigoureuse.

**Critique :** Le document, bien que très complet, reflète fortement une vision « techno-optimiste » de la Silicon Valley. Bien que les défis (hallucinations, coûts) soient mentionnés, la prémisse reste que l'IA va inévitablement transformer tous les secteurs [32]. La dimension sociale ou les impacts sur l'emploi sont abordés sous l'angle de l'augmentation de la productivité et de la libération des tâches banales [33], ce qui peut sembler idéaliste.

**Implications Pratiques pour les Startups :**
1.  **Ne vendez pas de l'IA, vendez du résultat :** L'IA est un outil, pas le produit final. Les clients se moquent du modèle utilisé ; ils veulent résoudre un problème [34].
2.  **Ciblez les flux de travail (Workflows) complets :** Ne faites pas juste un outil d'aide (co-pilote), visez l'agent qui exécute une tâche de bout en bout [35].
3.  **Soyez obsédés par l'évaluation :** Développez vos propres métriques d'évaluation (Evals) spécifiques à votre domaine pour prouver la fiabilité de votre solution [36].
4.  **Préparez-vous à l'interopérabilité :** Les futurs systèmes seront composés de multiples agents et modèles collaborant entre eux ; l'architecture technique doit être modulaire [37].

En somme, 2025 sera l'année où l'IA devra faire ses preuves en termes de ROI tangible, passant du statut de jouet technologique à celui de moteur économique industriel.

## Mots-clés

- **AI Agent Experiences**
- **RAG 2.0 Integration**
- **Multimodal Frontier Models**
- **AI Startup Disruption**
- **Bio and Hardware AI**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://services.google.com/fh/files/misc/google_cloud_future_of_ai_perspectives_for_startups_2025.pdf)
