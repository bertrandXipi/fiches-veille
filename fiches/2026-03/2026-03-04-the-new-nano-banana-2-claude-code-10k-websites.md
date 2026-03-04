---
title: The NEW Nano Banana 2 + Claude Code = $10k Websites
source_url: "https://youtu.be/q0TgUtj6vIs?is=DMUNpbwL4snbFl4Z"
source_type: article
date_captured: "2026-03-04T07:41:43.242Z"
date_processed: "2026-03-04T07:43:15.556Z"
tags: []
language: fr
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1478658685571039335"
status: published
notebooklm_notebook_id: 5ac37432-e593-4bb7-b761-a4301800efc4
notebooklm_source_id: d92933fd-8ed2-4839-b236-28f25daa58fe
notebooklm_url: "https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4"
keywords:
  - Claude Code
  - Développement web 3D
  - Animation par défilement
  - Intelligence artificielle vidéo
  - Déploiement via GitHub
---

## Résumé (NotebookLM)

### 1. Le contexte et les idées principales
Dans cette présentation, le créateur (Nate Herk) dévoile une méthode innovante permettant de créer des sites web de très haute qualité, comparables à ceux d'entreprises comme Apple, en une trentaine de minutes [1, 2]. L'idée centrale est d'utiliser l'intelligence artificielle pour générer des sites web de type "landing page" avec des animations complexes basées sur le défilement (scroll-driven animations) [3, 4]. 

Plutôt que de coder des animations 3D complexes, la technique consiste à transformer une vidéo générée par l'IA en une séquence d'images fixes (frames) qui défilent en fonction de la position de l'utilisateur sur la page, créant ainsi une illusion d'animation 3D fluide ou de "stop-motion" [4-6]. Le processus complet est piloté par l'assistant IA Claude Code, qui agit comme un développeur web autonome [7, 8].

### 2. Les différents points de vue ou arguments présentés
L'argument majeur de la vidéo est que la création de sites web hautement professionnels n'est plus le monopole des grandes agences de design facturant des dizaines de milliers de dollars pour des mois de travail [2]. Le présentateur soutient qu'un développeur solo ou une petite agence utilisant l'IA peut désormais fournir un travail d'une qualité équivalente en seulement quelques jours [9].

Il avance également l'idée que le prototypage et le développement itératif sont grandement facilités en séparant l'environnement de développement (local) de la production (le web) [2, 8]. Enfin, il démontre que l'utilisation de fichiers de configuration personnalisés ("skills") permet de guider l'IA pour qu'elle respecte les meilleures pratiques de conception sans avoir à tout réexpliquer à chaque fois [10, 11].

### 3. Les détails techniques, exemples concrets et données mentionnées
Le flux de travail technique repose sur un écosystème d'outils précis :
*   **Création de l'animation** : Le créateur utilise *Nano Banana 2* (via la plateforme key.ai) pour générer une image de départ (ex: un mixeur vide) et une image de fin (ex: un mixeur plein de fruits) avec un fond noir et sans ombres [12, 13]. Il utilise ensuite *Kling 3.0* pour animer la transition entre ces deux images [13].
*   **Développement web** : L'environnement de travail est *Visual Studio Code* avec l'extension *Claude Code* (nécessitant un abonnement Anthropic Pro ou Max) [7].
*   **Traitement de la vidéo** : L'outil gratuit *FFmpeg* est utilisé par l'IA pour extraire environ 120 images (frames) au format WebP à partir de la vidéo générée [4, 5, 14].
*   **Architecture et déploiement** : Le code est testé en local (localhost), poussé sur un dépôt *GitHub* (système de contrôle de version), puis déployé automatiquement sur le web via *Vercel* [8, 11, 15, 16].
*   **Exemples concrets** : Le créateur montre un site pour une caméra avec un effet "rayons X", une Apple Watch dont les composants se dévoilent, et construit en direct un site pour une marque fictive de mixeur nommée "Obsidian Vortex" [3, 12, 17].
*   **Fichiers "Skills"** : Il utilise des fichiers markdown personnalisés ("front-end design skill" et "video to website skill") qui contiennent les instructions secrètes pour formater le site correctement [10, 18].

### 4. Les problèmes, défis ou limitations identifiés
Malgré l'automatisation, plusieurs défis techniques sont mis en évidence lors de la démonstration :
*   **Saturation du contexte ("Context Rot")** : À un moment donné, la mémoire de l'IA atteint 53%. Le créateur doit effacer la conversation pour éviter que l'IA ne perde le fil ou ne devienne confuse [19].
*   **Synchronisation du défilement** : Lors des premiers tests du site du mixeur, l'apparition des textes (la fonctionnalité numéro 2) était mal synchronisée avec le défilement et apparaissait trop tard à l'écran, nécessitant une correction manuelle via un prompt [19, 20].
*   **Problèmes de déploiement** : Lors de l'envoi du code sur Vercel via GitHub, le dossier contenant les dizaines d'images (frames) a été exclu par défaut. Le site s'est chargé sans le mixeur visuel, obligeant le créateur à forcer l'inclusion des images dans le code source (via un nouveau "commit") pour réparer l'animation [16, 21].
*   **Optimisation mobile** : Le site généré n'est pas nativement optimisé pour les téléphones portables dès la première itération, ce qui représente une étape de travail supplémentaire ("next step") [22].

### 5. Les solutions, recommandations ou perspectives proposées
Pour pallier ces défis et maximiser l'efficacité, l'auteur propose plusieurs recommandations :
*   **Utiliser le "Plan Mode"** : Avant de laisser l'IA coder, il recommande d'utiliser ce mode pour que Claude génère un plan d'action (to-do list) que l'utilisateur peut valider et ajuster [4, 14, 17].
*   **Amélioration continue des "Skills"** : À chaque fois qu'une erreur est corrigée (comme le timing du texte), il conseille de demander à l'IA de mettre à jour le fichier markdown du "skill" afin que cette erreur ne se reproduise plus lors des futurs projets [6, 11].
*   **Modèle commercial (Perspectives)** : Le créateur propose de transformer cette compétence en un business lucratif. En ciblant des niches spécifiques, il est possible de créer des sites de démonstration, de les présenter aux clients, et de vendre ces sites entre 5 000 $ et 10 000 $ avec un délai de livraison de seulement deux jours, tout en ajoutant des revenus récurrents via l'hébergement et la maintenance [9].

### 6. Une synthèse critique et les implications pratiques
Le contenu illustre une évolution majeure dans le développement web assisté par l'IA. Au lieu d'utiliser des modèles 3D complexes (comme WebGL ou Three.js) qui demandent une grande expertise technique, l'utilisation de séquences d'images (frames) extraites de vidéos générées par l'IA offre un "raccourci" brillant pour obtenir un résultat visuel similaire [4, 6, 12]. 

Les implications pratiques sont immenses pour les freelances et les agences : cela abaisse considérablement la barrière à l'entrée pour la création d'expériences web premium [2, 9]. Toutefois, la méthode n'est pas un "bouton magique" infaillible. Elle nécessite une compréhension fondamentale de l'architecture web (différence entre un environnement local, GitHub et le cloud/Vercel) [8, 11], ainsi qu'une capacité à déboguer les erreurs de déploiement [21]. Le succès de cette méthode repose sur la capacité de l'utilisateur à orchestrer plusieurs outils d'IA distincts (générateurs d'images, générateurs de vidéos et assistants de code) pour produire un résultat final cohérent et monétisable.

## 💼 Post LinkedIn

Créer un site web animé façon Apple ne prend plus des mois de développement [1].

Fini les devis exorbitants et les agences hors de prix [2]. Tu peux maintenant générer une landing page 3D ultra-premium depuis ton éditeur [3, 4].

Comment on fait ça ?

En couplant la création vidéo IA avec un agent de développement. Le workflow est redoutablement efficace.

→ Tu génères une vidéo fluide de ton produit avec Nano Banana 2 [5, 6].
→ Claude Code extrait l'animation image par image avec FFmpeg [7, 8].
→ L'IA rédige tout le code de la page à ta place [9].
→ Le défilement de l'utilisateur anime le produit en temps réel [4, 10].

Une dinguerie visuelle.

Tu obtiens un rendu final exceptionnel en 30 minutes chrono [1, 2]. C'est exactement le type d'expérience web immersive qui se facture aujourd'hui entre 5 000 et 10 000 dollars aux marques [11].

Le marché du web design est en train de basculer violemment. 

Es-tu prêt à laisser un agent IA coder tes prochaines interfaces ?

#IntelligenceArtificielle #WebDesign #ClaudeCode

## Mots-clés

- **Claude Code**
- **Développement web 3D**
- **Animation par défilement**
- **Intelligence artificielle vidéo**
- **Déploiement via GitHub**

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/5ac37432-e593-4bb7-b761-a4301800efc4)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://youtu.be/q0TgUtj6vIs?is=DMUNpbwL4snbFl4Z)
