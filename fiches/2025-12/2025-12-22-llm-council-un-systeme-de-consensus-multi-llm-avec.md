---
title: "LLM Council : Un système de consensus multi-LLM avec revue par les pairs"
source_url: "https://share.google/Y9nwDJanUFLTuvAfg"
source_type: article
date_captured: "2025-12-22T06:26:56.846Z"
date_processed: "2025-12-22T07:01:43.790Z"
category: IA
tags:
  - LLM
  - OpenRouter
  - Consensus
  - Benchmark
  - Open Source
  - Vibe Coding
reading_time_minutes: null
language: fr
llm_provider: gemini
llm_model: gemini-cli
llm_prompt_version: v1
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1452547943474139238"
status: published
---

## Résumé

Ce projet expérimental propose une approche originale pour obtenir des réponses de haute qualité en réunissant plusieurs modèles de langage (LLM) au sein d'un 'conseil'. L'application locale interroge simultanément plusieurs modèles via OpenRouter, puis orchestre une phase de revue où chaque modèle évalue anonymement les réponses des autres.

Le processus se conclut par une synthèse finale rédigée par un modèle désigné comme 'Président', qui s'appuie sur les réponses individuelles et les critiques croisées. Développé quasi intégralement par 'vibe coding' (génération de code par IA), cet outil permet de comparer objectivement les performances des modèles récents comme GPT-5.1 ou Gemini 3.0 Pro.

## Points clés

- Interrogation parallèle de multiples LLMs via l'API OpenRouter
- Système de notation croisée où les modèles s'évaluent mutuellement à l'aveugle
- Génération d'une réponse finale synthétisée par un 'Chairman LLM'
- Architecture locale combinant FastAPI (Python) et React
- Approche 'Vibe Coding' assumée : code généré par IA et fourni sans maintenance

## Concepts liés

[[LLM Council]] | [[Automated Peer Review]] | [[Aggregated Intelligence]] | [[Model Arbitration]]

## Note originale

Source : GitHub

## Source

- [Article original](https://share.google/Y9nwDJanUFLTuvAfg)
