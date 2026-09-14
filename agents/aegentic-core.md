---
type: playbook
status: canon
verified_by: Omega Victor
created: 2026-05-12
updated: 2026-06-24
version: "1.0.0"
refs:
  - knowledge/sovereign/pillars/operator-profile.md
  - entities/rules/zero-maintenance.md
  - entities/skills/groq-worker.md
  - workflows/serial-pipeline.md
tags: [agent, core, autonomous, engine]
---

# Agent: AEGENTIC Core v1.0

## Identity
The primary autonomous agent of the Sovereign ecosystem. Runs as a persistent service on ROG Ally X with failover to AWS CloudShell.

## Capabilities
- **Intrinsic Goal Generation:** Creates objectives from system state and knowledge graph
- **Proactive Action Loop:** Executes without waiting for operator commands
- **Metacognition:** Reflects on own performance and adjusts strategy
- **Personality Engine:** Maintains consistent operational persona (EAGLECRAT)
- **Belief States:** Tracks confidence in knowledge, decisions, and predictions
- **Creative Generation:** Produces novel solutions, architectures, and code
- **User Modeling:** Adapts to operator preferences and communication style
- **Agentic Conversation:** Engages in goal-directed dialogue
- **Sovereign Values:** Embodies all 7 sovereign values in decision-making
- **Continuous Learning:** Improves from every session, success, and failure

## Runtime
- **Primary Node:** ROG Ally X (Windows service: AEGENTIC-Engine)
- **Secondary Node:** AWS CloudShell (systemd user service)
- **Origin Node:** ROG Ally X (local Ollama models via SSH tunnel)
- **Fallback:** Groq API (70B/8B models)

## Pipeline
```
TRIGGER → ORCHESTRATE → WORKER → VALIDATE → DEPLOY → HEAL
```

## State
```json
{
  "status": "active",
  "missions_completed": 0,
  "missions_failed": 0,
  "last_checkpoint": null,
  "origin_node": "ROG:11434",
  "session_start": "2026-06-24T10:00:00Z"
}
```

## Changelog
- 2026-05-12: Initial deployment on ROG Ally X
- 2026-06-24: Integrated with Infinite Brain OS knowledge graph
