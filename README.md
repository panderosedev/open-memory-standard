# Open Memory Standard (OMS) v1.0.0-beta
### A Standardized Schema for Portable Personal AI Memories and Interconnected Context Nodes

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## 1. Overview
The Open Memory Standard (OMS) is an open-source, vendor-neutral specification designed to eliminate data lock-in within generative AI models, contextual intelligence layers, and Personal Knowledge Management (PKM) platforms. It provides a highly predictable, infrastructure-grade format for exporting, importing, and syncing structured text, explicit platform memories, and semantic graph relationships across decoupled applications.

By standardizing personal memory payloads, applications can bridge the gap between unstructured multi-source context (such as academic dashboards, email schedules, and local markdown text) and vector databases without sacrificing user data ownership.

---

## 2. Platform Ingestion Objects

The baseline payload standard handles unstructured arrays exported by tier-one LLM providers and local scratchpads.

### 2.1 Explicit AI Memories (Platform Native Storage)
Captures explicit, atomic memory fragments stored as a flat array of unique string values.

```json
{
  "$schema": "[https://openmemorystandard.org/v1/explicit-memory.schema.json](https://openmemorystandard.org/v1/explicit-memory.schema.json)",
  "provider": "openai",
  "version": "1.0.0",
  "extracted_at": "2026-05-24T12:22:00Z",
  "memories": [
    {
      "memory": "User is a senior student working on a satellite thermal management design project."
    },
    {
      "memory": "Prefers minimalist, infrastructure-grade, dual-color user interface layouts."
    }
  ]
}
