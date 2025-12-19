---
title: Architecture et fonctionnement des Agent Skills de Claude
source_url: "https://leehanchung.github.io/blogs/2025/10/26/claude-skills-deep-dive/"
source_type: article
date_captured: "2025-12-18T20:21:06.969Z"
date_processed: "2025-12-19T07:00:43.035Z"
category: Dev
tags:
  - Claude
  - Anthropic
  - Agent
  - Prompt Engineering
  - Architecture
  - Skills
reading_time_minutes: null
language: fr
llm_provider: gemini
llm_model: gemini-cli
llm_prompt_version: v1
ingest_source: discord
discord_message_url: "https://discord.com/channels/1026842752232734811/1449479522993836213/1451308316801241158"
status: published
---

## Résumé

Le système 'Agent Skills' de Claude introduit une architecture de méta-outils reposant sur l'injection d'instructions spécialisées (prompts) plutôt que sur l'exécution de code ou d'appels de fonctions classiques. Ces compétences, structurées dans des dossiers contenant un fichier SKILL.md, permettent de modifier dynamiquement le contexte de la conversation et les permissions d'exécution pour guider le modèle dans des tâches complexes.

Contrairement aux approches traditionnelles, la sélection d'une compétence n'utilise pas de routage algorithmique mais s'appuie entièrement sur le raisonnement sémantique de Claude face aux descriptions fournies. La conception des Skills suit le principe de 'divulgation progressive', ne chargeant les instructions détaillées et les ressources (scripts, assets) qu'au moment de l'invocation pour optimiser l'efficacité de l'agent.

## Points clés

- Les Skills fonctionnent par expansion de prompt et modification de contexte, non par exécution de code direct.
- La découverte et l'invocation reposent sur le raisonnement du LLM (descriptions sémantiques) et non sur une classification algorithmique.
- Structure basée sur un fichier SKILL.md combinant métadonnées YAML (Frontmatter) et instructions Markdown.
- Principe de 'Divulgation Progressive' : chargement dynamique des détails et ressources (scripts, assets) seulement si nécessaire.
- Gestion fine des permissions via le champ 'allowed-tools' pour sécuriser l'usage des sous-outils (ex: git, npm).

## Concepts liés

[[Prompt Injection]] | [[Meta-tool]] | [[Progressive Disclosure]] | [[Context Modification]]

## Note originale

Aucune note.

## Source

- [Article original](https://leehanchung.github.io/blogs/2025/10/26/claude-skills-deep-dive/)
