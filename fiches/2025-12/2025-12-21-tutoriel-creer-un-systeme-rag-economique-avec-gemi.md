---
title: "Tutoriel : Créer un système RAG économique avec Gemini File Search et n8n"
source_url: "https://youtube.com/watch?v=4Tp4Kx-ThwI&si=ui3gw98sRwdPeWlE"
source_type: youtube
date_captured: "2025-12-21T15:21:27.847Z"
date_processed: "2025-12-21T19:02:44.173Z"
category: IA
tags:
  - Gemini API
  - RAG
  - n8n
  - Automatisation
  - Vector Database
  - Google AI Studio
reading_time_minutes: null
language: fr
llm_provider: gemini
llm_model: gemini-cli
llm_prompt_version: v1
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1452320071270662244"
status: published
youtube_channel: Eric Tech
youtube_duration: 15m06s
has_transcript: true
---

## Résumé

Cette vidéo présente un guide technique pour implémenter un système RAG (Retrieval-Augmented Generation) en utilisant l'API 'File Search' de Gemini. L'auteur met en avant la simplicité de cette solution, où Google gère automatiquement toute la complexité technique habituelle : le découpage des textes (chunking), la génération des embeddings et la maintenance de la base de données vectorielle, libérant ainsi le développeur de ces tâches fastidieuses.

Un avantage concurrentiel majeur souligné est le coût. Contrairement aux solutions comme Pinecone ou Supabase, Gemini offre le stockage vectoriel et les requêtes de recherche gratuitement. Seule l'indexation initiale des documents est facturée à un tarif très bas (environ 0,15 $ pour un million de tokens), ce qui en fait une option extrêmement rentable pour les projets d'IA.

La vidéo insiste fortement sur l'importance de la qualité des données ('Garbage in, garbage out'). L'auteur démontre une méthodologie de préparation des données utilisant des agents de codage (comme Claude/Cursor) pour nettoyer, résumer et agréger une centaine de fichiers de transcription épars en un seul document Markdown structuré et optimisé pour la recherche vectorielle.

Le cœur du tutoriel détaille l'intégration de ce système via l'outil d'automatisation n8n. Trois workflows séquentiels sont construits : la création du 'store' via une requête API, le traitement et l'upload du fichier source, et enfin la configuration d'un agent IA capable d'interroger cette base de connaissances personnalisée pour répondre à des questions spécifiques.

Enfin, l'auteur montre comment prototyper et tester rapidement ces interactions directement dans Google AI Studio avant de passer à l'implémentation en production. Cette approche permet de vérifier la pertinence des réponses et la qualité des citations sources fournies par le modèle avant de construire l'automatisation complète.

## Points clés

- Gestion automatisée du pipeline RAG par Gemini (chunking, embeddings, vecteurs)
- Tarification très avantageuse : stockage et recherche gratuits, indexation payante
- Nettoyage et agrégation des données brutes via des agents de codage avant ingestion
- Création de workflows n8n pour automatiser la création et la mise à jour de la base
- Prototypage rapide des bases de connaissances via l'interface Google AI Studio

## Concepts liés

[[File Search API]] | [[Embeddings]] | [[Data Cleaning]] | [[Vector Store]] | [[Agent IA]]

## Note originale

Aucune note.

## Source

- [Vidéo YouTube](https://youtube.com/watch?v=4Tp4Kx-ThwI&si=ui3gw98sRwdPeWlE)
- Chaîne: Eric Tech
- Durée: 15m06s
