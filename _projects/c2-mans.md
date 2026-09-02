---
layout: page
title: C2-MANS
description: A neuro-symbolic multi-agent system for logically consistent long-form narrative generation.
img:
importance: 1
category: research
---

C2-MANS combines large language models with structured Pydantic state models to maintain consistency across a generated narrative.

The system uses a CrewAI pipeline with four specialized agents. Scene-level constraints and post-generation state synchronization help preserve facts and relationships across chapters. Persistent storage layers such as `RelationshipGraph` and `TimeLedger` support autonomous generation of 10-chapter novellas.

**Technologies:** Python, CrewAI, Pydantic, large language models, persistent state management.
