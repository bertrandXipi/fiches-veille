---
title: The NEW Nano Banana 2 + Claude Code = $10k Websites
source_url: "https://youtu.be/q0TgUtj6vIs?is=4ABRx82nnJlvGlTR"
source_type: article
date_captured: "2026-03-04T07:45:36.131Z"
date_processed: "2026-03-04T07:47:01.204Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1478659663208779908"
status: published
notebooklm_notebook_id: eea0382d-c943-416b-a20b-4427b9f9b5aa
notebooklm_source_id: 21d19557-3a39-4029-ae35-54351bc60885
notebooklm_url: "https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa"
keywords:
  - Claude Code
  - Développement web 3D
  - Animation par défilement
  - Intelligence artificielle vidéo
  - Déploiement via GitHub
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales

Le contenu présenté par Nate Herk se concentre sur l'utilisation de l'intelligence artificielle pour révolutionner la création de sites web haut de gamme [1]. L'idée principale est qu'il est désormais possible de construire des pages de destination (landing pages) professionnelles avec des animations 3D dynamiques fluides — similaires à celles d'Apple — en seulement une trentaine de minutes [1]. L'auteur démontre comment combiner des générateurs d'images et de vidéos par IA avec des assistants de codage pour transformer une simple vidéo en un site web interactif basé sur le défilement (scroll) [2, 3]. Ce processus permet non seulement de démocratiser le design web avancé, mais offre également une opportunité lucrative : vendre ces sites à des entreprises pour des montants allant de 5 000 $ à 10 000 $ [4].

### 2. Les différents points de vue ou arguments présentés

L'auteur avance plusieurs arguments majeurs en faveur de cette nouvelle méthode de travail :
*   **L'inefficacité du modèle traditionnel :** Les agences de conception web classiques facturent souvent des dizaines de milliers de dollars et prennent des mois pour livrer des sites complexes [5]. En revanche, l'IA permet de livrer un produit similaire, voire supérieur, en un ou deux jours [4].
*   **L'accessibilité technique :** Il n'est plus nécessaire d'avoir des compétences poussées en développement ou en modélisation 3D [1]. L'IA prend en charge la génération des assets visuels et l'écriture du code, rendant la création accessible même aux débutants, à condition de suivre les bonnes étapes [1, 6].
*   **Un modèle commercial très rentable :** Proposer ces sites rapides à produire à des prix compétitifs ($5k-$10k) permet de dégager d'importantes marges tout en fidélisant le client via des contrats de maintenance et d'hébergement mensuels [4].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le processus s'appuie sur une pile technologique (stack) précise et innovante :
*   **Génération visuelle :** L'auteur utilise *Nano Banana 2* (via l'interface key.ai) pour créer des images de départ et de fin d'un produit (ex: un mixeur vide, puis rempli de fruits) [6, 7]. Ensuite, *Kling 3.0* est utilisé pour animer la transition entre ces deux images afin de créer une vidéo fluide [7].
*   **Développement Web :** Le cœur du système est *Claude Code*, utilisé sous forme d'extension dans l'éditeur *Visual Studio Code* (nécessitant un abonnement Anthropic Pro ou Max) [8].
*   **Le mécanisme d'animation :** L'outil *FFmpeg* extrait plus d'une centaine d'images (frames) au format WebP à partir de la vidéo générée [9, 10]. Le site utilise ensuite une technique semblable au "stop-motion" : chaque image est associée à une position de défilement (scroll) sur la page, ce qui donne l'illusion d'une animation 3D interactive [3].
*   **Outils personnalisés :** L'auteur fournit des "skills" (compétences) sous forme de fichiers Markdown (ex: *front-end design skill* et *video to website skill*) qui dictent à Claude Code les meilleures pratiques pour coder ces animations [11].
*   **Exemples :** Le rapport montre la création d'un site fictif pour un mixeur nommé "Obsidian Vortex", un site pour un appareil photo avec une vision "Rayons X", et un site pour une Apple Watch qui se déplie [2, 6, 12].
*   **Déploiement :** Le code est d'abord testé en local (localhost sur le port 51006) [13], puis poussé sur *GitHub* pour le contrôle de version, et enfin déployé automatiquement et gratuitement via *Vercel* [14-16].

### 4. Les problèmes, défis ou limitations identifiés

Malgré la rapidité du processus, plusieurs défis techniques surviennent lors de la démonstration :
*   **Synchronisation des animations :** Lors du test du site du mixeur, la caractéristique numéro 2 (feature 2) apparaissait trop tard à l'écran lors du défilement, la rendant presque invisible pour l'utilisateur [17, 18].
*   **Problèmes de déploiement (Assets manquants) :** Lors du premier déploiement sur Vercel, les images (frames) de l'animation n'ont pas été chargées [16]. Claude Code avait exclu ces lourds fichiers visuels lors de l'envoi (push) vers GitHub, ce qui a rendu l'animation inexistante sur la version en ligne [19].
*   **Limites de contexte de l'IA (Context Rot) :** L'auteur mentionne qu'à 53% d'utilisation du contexte de l'IA, il est préférable d'effacer la conversation pour éviter que l'IA ne se "perde" ou ne devienne confuse (un phénomène appelé "context rot") [18].
*   **Optimisation mobile :** À la fin du processus, le site fonctionnait sur mobile, mais n'était pas encore pleinement optimisé (responsive design), ce qui constitue une étape supplémentaire obligatoire [20].

### 5. Les solutions, recommandations ou perspectives proposées

Pour contourner ces limitations, plusieurs solutions pratiques sont mises en avant :
*   **Itération par le prompt :** Pour corriger l'apparition tardive du texte, il suffit de formuler le problème à Claude Code ("La caractéristique 2 apparaît trop tard") pour qu'il modifie automatiquement le code Javascript ou CSS [18, 21].
*   **Correction du pipeline de déploiement :** Pour le bug de Vercel, l'instruction directe donnée à l'IA d'inclure explicitement le dossier "frames" dans le dépôt GitHub a résolu le problème immédiatement [19].
*   **Utilisation d'environnements séparés :** L'auteur insiste sur l'importance de tester le site en "localhost" (environnement de test/staging) avant de pousser les modifications en production sur le vrai nom de domaine, évitant ainsi de casser le site en direct [5].
*   **Amélioration continue :** Il est recommandé de mettre à jour le fichier "skill.md" avec ses propres préférences (couleurs, comportements) pour que l'IA apprenne et produise de meilleurs résultats dès le premier essai lors des futurs projets [4, 14, 22].

### 6. Une synthèse critique et les implications pratiques

Ce contenu met en lumière une transition paradigmatique dans le développement web. En déléguant la logique de programmation et la création d'assets visuels à des intelligences artificielles complémentaires (LLMs pour le code, générateurs de diffusion pour la vidéo), la création de sites web hautement interactifs passe d'un processus d'ingénierie complexe à un processus de direction artistique et de *prompt engineering*. 

**Implications pratiques :**
L'abaissement radical de la barrière à l'entrée menace directement les agences web traditionnelles qui justifient leurs tarifs élevés par la complexité technique de ces animations interactives. Cependant, la méthode n'est pas encore infaillible. Le rôle de l'humain reste indispensable pour orchestrer les différents outils, superviser le contrôle qualité (corriger les bugs d'affichage, assurer l'optimisation mobile) et comprendre l'architecture de déploiement (Git, Vercel). En fin de compte, cette approche offre un avantage concurrentiel massif aux freelances et petites agences capables d'adopter ces outils d'automatisation IA pour proposer des expériences web premium à une fraction du temps et du coût habituels.

## 💼 Post LinkedIn

Créer une page web avec des animations 3D dignes d'Apple prenait des mois. Aujourd'hui ? 30 minutes chrono [1].

Je viens de décortiquer une méthode stupéfiante. 
La combinaison magique s'appelle Claude Code et Nano Banana 2 [1, 2].
Le résultat ? Des landing pages ultra-premium créées de zéro.

Comment ça fonctionne exactement ?

→ Génération des images de départ et de fin d'un produit avec Nano Banana 2 [2, 3].
→ Création d'une animation vidéo fluide pour lier les deux plans [3].
→ Extraction de plus de 100 images de la vidéo pour créer une animation contrôlée par le scroll de l'utilisateur [4, 5].
→ Claude Code génère l'ensemble du code, teste en local et déploie le tout sur Vercel via GitHub [6-8].

Tout ça avec de simples fichiers de compétences pour guider l'IA [9].

Le plus fou n'est pas la prouesse technique. C'est le modèle d'affaires.
Un site interactif de ce calibre peut se vendre entre 5 000 $ et 10 000 $ à une entreprise [10].
Le tout réalisé en un temps record au lieu de plusieurs semaines de développement classique [10, 11].

Les barrières techniques s'effondrent les unes après les autres. Le code n'est plus un obstacle, c'est devenu une simple commande conversationnelle [12].

Pensez-vous que cette automatisation va faire disparaître les agences web traditionnelles ou simplement élever le standard de qualité du marché ?

#IntelligenceArtificielle #WebDesign #ClaudeCode

## Mots-clés

- **Claude Code**
- **Développement web 3D**
- **Animation par défilement**
- **Intelligence artificielle vidéo**
- **Déploiement via GitHub**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/eea0382d-c943-416b-a20b-4427b9f9b5aa)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://youtu.be/q0TgUtj6vIs?is=4ABRx82nnJlvGlTR)
