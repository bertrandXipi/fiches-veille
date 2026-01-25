---
title: I built an app that detects plaque and every tooth from a single photo. I have a strong feeling that this side project is about to become something much bigger. : r/buildinpublic
source_url: https://www.reddit.com/r/buildinpublic/comments/1qmbghf/i_built_an_app_that_detects_plaque_and_every/
source_type: article
date_captured: 2026-01-25T17:43:51.455Z
date_processed: 2026-01-25T18:47:00.000Z
tags: []
language: fr
ingest_source: discord
discord_message_url: https://discord.com/channels/1026842752232734811/1449479522993836213/1465039480061952252
status: published
notebooklm_notebook_id: c4dba600-dd91-4027-ba33-8ad93f971a31
notebooklm_source_id: b110a6a1-8e65-4ea9-a7db-4cd234016fd3
notebooklm_url: https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31
---

## Résumé (NotebookLM)

Voici un rapport détaillé analysant le fil de discussion Reddit concernant l'application de détection de plaque dentaire.

### 1. Le contexte et les idées principales du post

Le fil de discussion provient du subreddit `r/buildinpublic`, une communauté où les créateurs partagent l'évolution de leurs projets. L'auteur, l'utilisateur `w-zhong`, présente une application mobile ("Brushmo") qu'il a développée sur une période de quatre semaines, en y consacrant environ quatre heures par jour [1, 2].

L'idée centrale est l'utilisation de la vision par ordinateur (Computer Vision) pour l'hygiène bucco-dentaire. L'application permet aux utilisateurs de prendre une simple photo de leur dentition pour obtenir trois résultats clés :
1.  L'identification individuelle de chaque dent.
2.  La détection de la plaque dentaire sur différentes zones.
3.  Des conseils pratiques et fondés sur des preuves pour améliorer le brossage [2].

Le projet a évolué d'une "idée brute" vers un produit utilisable disponible sur l'App Store. L'auteur souligne également une refonte technique majeure effectuée parallèlement au développement des algorithmes, passant d'une architecture React Native à une solution native SwiftUI pour l'interface, et une migration vers une architecture "cloud-native" sur AWS pour le backend [3].

### 2. Les différents points de vue ou arguments présentés

Les réactions dans les commentaires révèlent un spectre varié d'opinions, allant de l'enthousiasme à un scepticisme pragmatique.

*   **L'enthousiasme et la validation du besoin :** Plusieurs utilisateurs expriment un fort intérêt. Un utilisateur, `John-FitnessRefined`, apprécie particulièrement la possibilité de vérifier la présence de caries ou de plaque depuis le confort de son domicile avant de prendre rendez-vous chez le dentiste [4]. D'autres qualifient l'idée de "géniale" et voient un potentiel commercial énorme ("Big-big"), suggérant que le produit a dépassé le stade du simple gadget pour atteindre un niveau d'intérêt industriel [5].
*   **La curiosité technique :** La communauté étant composée de développeurs, plusieurs questions portent sur les outils utilisés (IDE) et la méthodologie d'entraînement des algorithmes. On s'interroge notamment sur la provenance des données labellisées nécessaires à l'apprentissage automatique [5, 6].
*   **Le scepticisme sur l'utilité (Product-Market Fit) :** Un courant critique, représenté par `MrBilal34` et `agin_`, questionne la pertinence du produit. L'argument principal est que les personnes soucieuses de mesurer leur plaque dentaire ont probablement déjà une excellente hygiène ou utilisent des solutions analogiques éprouvées (comme les révélateurs de plaque à mâcher), jugées "100 fois plus précises" que la reconnaissance d'image actuelle [4].

### 3. Les détails techniques, exemples concrets et données mentionnées

Le rapport met en lumière plusieurs aspects techniques spécifiques qui sous-tendent le projet :

*   **Architecture logicielle :** L'application a subi une migration technique significative. Le frontend a été refactorisé de React Native vers **SwiftUI** (natif iOS), nécessitant l'utilisation de l'environnement de développement Xcode [3, 5]. Le backend repose sur une infrastructure **AWS** (Amazon Web Services) qualifiée de "cloud-native" [3].
*   **Intelligence Artificielle et Données :** L'auteur a collaboré directement avec des cliniques et des dentistes pour obtenir et labelliser les données nécessaires à l'entraînement des modèles, plutôt que d'utiliser un dataset public existant [6].
*   **Performance réelle (Test utilisateur) :** L'utilisateur `HowWeBuilt` fournit un retour d'expérience concret après avoir testé l'application. Sur une photo prise de face, l'algorithme a détecté les 4 dents supérieures et les 2 canines inférieures. Cependant, le taux de détection de plaque rapporté sur une dent spécifique n'était que de 4 %, ce qui a semblé faible ou peu concluant à l'utilisateur [5, 7].

### 4. Les problèmes, défis ou limitations identifiés

Malgré l'innovation, plusieurs limitations techniques et fonctionnelles ont été soulevées par la communauté :

*   **Précision de la détection :** Le testeur principal a noté que la détection était "très prometteuse mais pouvait être améliorée". L'application n'a pas réussi à identifier toutes les dents sur une seule photo, et les résultats concernant la quantité de plaque (4 %) ne semblaient pas correspondre à un niveau de fiabilité clinique ("show my dentist level") [5, 7].
*   **Limitation de la prise de vue unique :** Le concept repose sur "une seule photo" [2], mais cela s'avère insuffisant pour capturer la complexité d'une dentition complète en 3D. Les utilisateurs suggèrent que l'approche actuelle manque de profondeur pour une analyse complète [7].
*   **Exclusivité de plateforme :** L'application n'est disponible que sur iOS pour le moment, ce qui a provoqué une demande immédiate pour une version Android de la part de l'utilisateur `Capuchoochoo` [4].
*   **Concurrence analogique :** La technologie doit prouver sa supériorité face aux méthodes traditionnelles (comprimés révélateurs) qui sont bon marché et extrêmement précises, rendant l'adoption de l'IA potentiellement superflue pour certains segments de marché [4].

### 5. Les solutions, recommandations ou perspectives proposées

Les commentaires offrent des pistes constructives pour l'évolution du produit :

*   **Imagerie composite :** Pour pallier les limites de la photo unique, il est suggéré de permettre à l'utilisateur de prendre plusieurs clichés sous différents angles. L'application pourrait alors assembler ces images pour former une "compréhension composite" de la dentition, améliorant ainsi la précision globale [7].
*   **Pivot vers le B2B :** Plutôt que de viser uniquement le grand public (qui peut être sceptique), il est recommandé de présenter cette technologie aux acteurs de l'industrie de la santé bucco-dentaire. Le niveau actuel de la technologie est perçu comme suffisant pour initier des contacts professionnels ("start showing contacts in the oral healthcare industry") [5].
*   **Comparaison avec d'autres modèles :** Un utilisateur mentionne avoir exploré une idée similaire avec des modèles d'IA comme "nano banana" (probablement une référence à des modèles légers type NanoDet ou une appellation spécifique de niche), suggérant qu'il existe d'autres architectures de modèles à explorer pour optimiser la détection sur mobile [7].

### 6. Synthèse critique et implications pratiques

Ce projet illustre parfaitement la démocratisation de l'IA appliquée à la santé (HealthTech) par des développeurs indépendants.

**Synthèse :**
L'application *Brushmo* démontre qu'il est techniquement possible, pour un développeur isolé, de déployer des solutions de vision par ordinateur complexes en quelques semaines. La collaboration avec des dentistes pour les données d'entraînement [6] est le point fort du projet, lui conférant une crédibilité que les projets purement "tech" n'ont souvent pas. Cependant, le fossé entre une "démo technique impressionnante" et un "dispositif médical fiable" reste le défi majeur. Les retours indiquent que si l'application détecte bien les dents, la quantification précise de la pathologie (plaque) reste perfectible [5].

**Implications pratiques :**
1.  **Pour le développeur :** La priorité doit être l'amélioration de la précision algorithmique, probablement via l'imagerie multi-angle suggérée par les utilisateurs. Le passage à SwiftUI et AWS indique une volonté de scalabilité, mais le produit doit d'abord prouver sa fiabilité clinique.
2.  **Pour le marché :** Il existe une tension entre le besoin de "télédentisterie" (vérifier ses dents à la maison) et la réalité des outils existants. Pour réussir, l'application ne doit pas seulement détecter la plaque, mais offrir une expérience utilisateur supérieure aux méthodes chimiques (pas de taches bleues sur les dents, suivi historique, gamification).
3.  **Potentiel :** Si la précision atteint un seuil critique, ce type d'outil pourrait intéresser les compagnies d'assurance ou les fabricants de brosses à dents électriques pour des partenariats, dépassant le simple cadre de l'application grand public [5].

## 📚 NotebookLM

[Ouvrir dans NotebookLM](https://notebooklm.google.com/notebook/c4dba600-dd91-4027-ba33-8ad93f971a31)

Utilisez NotebookLM pour:
- Poser des questions approfondies sur le contenu
- Générer des résumés personnalisés selon vos besoins
- Créer des podcasts audio pour écouter en déplacement
- Explorer les concepts et leurs interconnexions
- Comparer avec d'autres sources du notebook

## Source

- [Article original](https://www.reddit.com/r/buildinpublic/comments/1qmbghf/i_built_an_app_that_detects_plaque_and_every/)
