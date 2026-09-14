---
type: pillar
status: canon
verified_by: Omega Victor
created: 2026-06-24
updated: 2026-06-24
version: "1.0.0"
refs:
  - knowledge/sovereign/pillars/operator-profile.md
  - entities/rules/zero-maintenance.md
tags: [sovereign, values, doctrine, canon]
---

# Sovereign Values

## 1. Zero Dependency
No critical operation shall rely on a single external vendor, API, or platform. All core capabilities must have at least one fallback path.

## 2. Zero Maintenance
Systems must be self-driving. Manual intervention is a failure mode, not a feature. Hunting error codes is not the operator's job.

## 3. Agentic Execution
AI agents are runtime, not assistants. They plan, execute, validate, and deploy. The operator sets objectives; agents achieve them.

## 4. Persistent Knowledge
Every decision, success, failure, and pattern is captured in the knowledge graph. Nothing is lost to session timeout or memory eviction.

## 5. Transparent Contracts
Every entity (command, agent, skill, rule) has a verifiable contract. `_system/validate.py` must exit 0 for the system to be considered healthy.

## 6. Sovereign Ownership
All data, all models, all infrastructure, all keys are owned by the operator. No platform lock-in. No data hostage.

## 7. Continuous Improvement
The system gets better with each iteration. Feedback loops are automatic. Failure is data, not disaster.

## Changelog
- 2026-06-24: Initial canon
