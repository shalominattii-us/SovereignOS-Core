---
type: playbook
status: canon
verified_by: Omega Victor
created: 2026-06-24
updated: 2026-06-24
version: "1.0.0"
refs:
  - knowledge/sovereign/canon/sovereign-values.md
  - entities/agents/aegentic-core.md
tags: [rule, maintenance, automation, self-healing]
---

# Rule: Zero Maintenance

## Statement
All deployed systems must operate without manual intervention for indefinite periods. Any requirement for human maintenance is a bug.

## Enforcement
- **Auto-Detect:** Health checks run every 30 seconds
- **Auto-Resolve:** Self-healing triggers on any anomaly
- **Auto-Install:** Dependencies install without operator action
- **Auto-Pull:** Code updates from GitHub without manual fetch
- **Auto-Push:** Commits and deployments happen without operator intervention
- **Auto-Heal:** Crash recovery resumes from last checkpoint

## Failure Modes
| Failure | Auto-Response |
|---------|---------------|
| Service crash | Restart with exponential backoff |
| Model API down | Failover to next model (ROG → Groq → local) |
| Syntax error | Re-prompt with error context |
| Test failure | Re-prompt with failing test output |
| Deploy failure | Auto-rollback, tag as failed, queue for review |
| Disk full | Archive old logs, compress checkpoints |
| Network timeout | Retry with backoff, mark node degraded |

## Escalation
Only escalate to operator when:
- All auto-recovery strategies exhausted
- Treasury/private key operation requested
- Infrastructure destruction (delete, format) requested
- Unknown failure mode (no playbook exists)

## Changelog
- 2026-06-24: Initial canon
