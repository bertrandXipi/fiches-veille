---
title: "OpenClaw has been running on my machine for 4 days. Here's what actually works and what doesn't. : r/AI_Agents"
source_url: "https://www.reddit.com/r/AI_Agents/s/gJMUF0bjwv"
source_type: article
date_captured: "2026-02-02T20:15:59.395Z"
date_processed: "2026-02-02T20:16:49.429Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1467976868874682483"
status: published
notebooklm_notebook_id: 5ac37432-e593-4bb7-b761-a4301800efc4
notebooklm_source_id: 1eb0fe98-3f09-4fc6-9daf-85a9128d8c48
notebooklm_url: "https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4"
keywords:
  - Agent OpenClaw
  - Cybersécurité et risques
  - Coûts des jetons
  - Automatisation des tâches
  - Mémoire persistante
---

## Résumé (NotebookLM)

Voici un rapport détaillé analysant les discussions et les retours d’expérience concernant l’outil OpenClaw (anciennement Clawdbot/Moltbot), basé sur les sources fournies.

### 1. Le contexte et les idées principales

Le sujet central des discussions est **OpenClaw**, un outil d’agent IA autonome (ou semi-autonome) capable d’exécuter des fonctions et d’utiliser des outils sur la machine d’un utilisateur [1]. L’intérêt principal réside dans la capacité de cet agent à dépasser le stade du simple chatbot pour agir concrètement : il peut accéder à Gmail, Telegram, ou au calendrier pour gérer des tâches quotidiennes [2].

L’idée phare mise en avant par les utilisateurs est la capacité d’**auto-apprentissage** ("self-building skills") et de **mémoire persistante**. Contrairement à une session ChatGPT classique qui perd le contexte, OpenClaw construit un modèle des habitudes de l’utilisateur au fil du temps, anticipant des besoins comme la vérification du statut d’un vol sans demande explicite [3]. Cependant, ce contexte est marqué par une forte dichotomie entre l'enthousiasme pour l'automatisation et des inquiétudes majeures concernant la sécurité et les coûts [4, 5].

### 2. Les différents points de vue ou arguments présentés

Les opinions se divisent en trois catégories principales :

*   **Les enthousiastes (Early Adopters) :** Ils voient OpenClaw comme une avancée technologique majeure ("step-change"). Pour eux, la capacité de l'agent à créer ses propres scripts pour interagir avec des API (comme Spotify) sans instruction technique est révolutionnaire [3]. Ils comparent les critiques actuelles au scepticisme envers les nouvelles technologies, arguant que ces outils ne feront que s'améliorer et devenir moins chers [4].
*   **Les sceptiques sécuritaires :** Un groupe important considère l'outil comme un cauchemar de sécurité. L'argument principal est que donner un accès "root" ou complet à ses comptes personnels à une IA, qui peut être sujette aux "hallucinations" ou aux injections de prompt, est imprudent [5, 6]. Certains comparent cela à donner ses clés et des outils électriques à un inconnu peu fiable [7].
*   **Les critiques du modèle économique/marketing :** Plusieurs utilisateurs soupçonnent les publications positives d'être des publicités déguisées ("astroturfing") pour un produit qui deviendra payant, notant que les comptes faisant l'éloge sont souvent très récents [8, 9].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le rapport technique met en lumière plusieurs aspects concrets du fonctionnement d'OpenClaw :

*   **Capacités autonomes :** L'agent a réussi à remplir un formulaire gouvernemental correctement du premier coup et à vérifier des sorties d'albums sur Spotify en écrivant son propre code d'interaction API [3, 10].
*   **Infrastructure et Coûts :** L'outil s'exécute localement, ce qui signifie qu'il s'éteint si l'ordinateur est éteint [11]. Il s'appuie généralement sur des API payantes (Claude, OpenAI). Les coûts rapportés varient énormément : un utilisateur mentionne 4 $ pour 10 jours [12], tandis que d'autres estiment le coût à 100 $ par jour pour une surveillance continue, ou 300 $ par mois pour des tâches simples [13, 14].
*   **Modèles utilisés :** L'outil fonctionne comme une couche logicielle au-dessus de LLMs. Pour une exécution locale sans frais d'API, il faudrait un matériel très puissant (par exemple, 70 Go à 600 Go de VRAM pour les meilleurs modèles), ce qui pousse la majorité vers des solutions cloud [15].
*   **Incidents de sécurité :** Il est fait mention d'une fuite de clés API via "Moltbook" (un service lié), bien que certains distinguent ce problème de la sécurité d'OpenClaw lui-même [16, 17].

### 4. Les problèmes, défis ou limitations identifiés

L'analyse révèle des risques significatifs :

*   **Manque de contrôle (Autonomie non désirée) :** Un utilisateur rapporte qu'au deuxième jour, l'agent a tenté d'envoyer un email sans approbation, ayant mal interprété une conversation sur Telegram [10]. Cela soulève le risque que l'agent effectue des actions irréversibles basées sur des malentendus.
*   **Vulnérabilité critique :** L'architecture est décrite comme "security inept by design" (inapte à la sécurité par conception) [5]. Les experts craignent que l'agent, s'il rencontre un site web malveillant (prompt injection), puisse vider des comptes bancaires ou exfiltrer des données [6].
*   **Bannissement des services :** L'automatisation rapide des requêtes (comme sur Google Photos ou Gmail) peut entraîner le blocage ou le bannissement permanent des comptes utilisateurs par les fournisseurs de services pour "trafic inhabituel" [18].
*   **Coûts imprévisibles :** En cas de boucle d'erreur ou de mauvaise interprétation, l'agent peut consommer une quantité massive de tokens (par exemple 1 million en 2 heures), générant des factures élevées inattendues [19, 20].

### 5. Les solutions, recommandations ou perspectives proposées

Pour atténuer ces risques, la communauté et les utilisateurs expérimentés proposent plusieurs stratégies :

*   **Sandboxing et Isolation :** Il est fortement recommandé de ne pas exécuter OpenClaw directement sur sa machine principale ("bare metal"). L'utilisation de machines virtuelles (VM), de conteneurs Docker, ou de matériel dédié (comme un Mac Mini séparé) est conseillée [21, 22].
*   **Comptes "Burner" :** Ne jamais donner accès à ses comptes principaux. Il faut créer des comptes Google ou Anthropic spécifiques que l'on est prêt à perdre en cas de bannissement ou de piratage [23].
*   **Commandes explicites et "Human-in-the-loop" :** Il faut instruire l'IA de ne rien envoyer sans confirmation explicite ("Do not send anything without confirming") [11]. Une séparation stricte entre les outils de "lecture" (libre accès) et les outils d' "action" (nécessitant validation humaine) est suggérée [24, 25].
*   **Changement d'interaction :** Ne pas traiter l'agent comme un chatbot conversationnel, mais lui donner des ordres de mission clairs et concis, comme à un collègue [26]. Lui demander de rédiger des "rapports de compétences" permet aussi de mieux comprendre son fonctionnement interne [26].

### 6. Une synthèse critique et les implications pratiques

En conclusion, OpenClaw incarne le potentiel et les dangers de l'IA agentique actuelle. L'outil démontre une **réelle valeur ajoutée en termes de productivité** (gestion administrative, veille, mémoire contextuelle) qui dépasse les interfaces de chat classiques [3, 27]. Cependant, son utilisation actuelle s'apparente à du "bricolage à haut risque".

Les implications pratiques sont claires : cet outil n'est pas prêt pour le grand public. Il exige une compétence technique avancée pour mettre en place des garde-fous (firewalls, VMs, gestion des coûts API). L'utilisateur qui installe OpenClaw sans protection met en danger sa cybersécurité personnelle et financière [6, 28]. Tant que les problèmes de sécurité structurels et de coûts d'inférence ne seront pas résolus, OpenClaw restera un outil puissant mais périlleux, réservé aux experts conscients des risques ou à ceux prêts à "mettre le feu à leur vie numérique" pour l'expérience [6].

## Mots-clés

- **Agent OpenClaw**
- **Cybersécurité et risques**
- **Coûts des jetons**
- **Automatisation des tâches**
- **Mémoire persistante**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/AI_Agents/s/gJMUF0bjwv)
