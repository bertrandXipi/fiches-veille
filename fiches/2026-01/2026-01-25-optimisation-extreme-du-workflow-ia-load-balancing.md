---
title: "Optimisation extrême du workflow IA : Load balancing via Open Code"
source_url: "https://www.reddit.com/r/google_antigravity/s/pxopHuVHrR"
source_type: article
date_captured: "2026-01-25T15:34:03.812Z"
date_processed: "2026-01-25T16:06:15.560Z"
category: Dev
tags:
  - Google AI Pro
  - Antigravity
  - Open Code
  - Workflow
  - Optimisation
reading_time_minutes: null
language: fr
llm_provider: gemini
llm_model: gemini-cli
llm_prompt_version: v1
ingest_source: manual
discord_message_url: null
status: published
---

## Résumé

Retour d'expérience critique sur l'écosystème Google AI Pro. Si l'offre est attractive sur le papier, l'IDE natif Antigravity s'avère trop gourmand en ressources (consommation RAM excessive) pour des workflows intensifs impliquant de multiples agents en parallèle. Les tentatives d'intégration classiques avec Claude Code via proxy ont montré des latences inacceptables.

La solution a consisté à utiliser Open Code avec une authentification directe, permettant de configurer un équilibrage de charge (load balancing) sur 5 comptes Google simultanés. Cette architecture offre une capacité de traitement démultipliée (équivalente à 5 fois Claude Code Pro) et permet d'exploiter les modèles Opus 4.5 et Gemini 3 Pro sans friction, maximisant ainsi le retour sur investissement de l'abonnement.

## Points clés

- Limitations de performance de l'IDE Antigravity pour les tâches à haute vélocité.
- Mise en place d'un load balancing sur 5 comptes Google via Open Code.
- Gain massif de capacité et accès fluide aux modèles Opus 4.5 et Gemini 3 Pro.

## Concepts liés

[[Load Balancing]] | [[Multi-Agent]]

## Note originale

Aucune note.

## Source

- [Article original](https://www.reddit.com/r/google_antigravity/s/pxopHuVHrR)
