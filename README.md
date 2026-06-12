# Workflow Commands

A collection of agentic workflow command specifications for autonomous, end-to-end software delivery. Each file defines a self-contained command — its role agents, artifacts, gate criteria, and step-by-step execution flow — that an agentic system follows to take a project from scope to delivery.

The two workflows represent opposite ends of the delivery spectrum: a lightweight startup flow optimized for speed, and a formal enterprise flow optimized for governance and traceability.

## Commands

### `BUILD_STARTUP_PRODUCT_FROM_SCOPE`

**File:** [`quick-production.md`](quick-production.md)

Autonomously transforms a given scope and feature list into working software. It creates lightweight documents, generates implementation tasks, builds and tests the product, fixes defects, and delivers a runnable package — **without stopping for human approval**.

When information is missing, the workflow makes the most reasonable startup-friendly assumption, documents it, and continues.

Optimizes for: speed, working software, simple architecture, fast iteration, and minimal bureaucracy.

Key sections:
- Startup execution principle & autonomous behavior rules
- Core and minimal agent sets
- Lightweight artifacts
- Workflow steps with non-stop execution policy
- Validation gates and autonomous looping rules
- Definition of Done and default assumptions

### `RUN_ENTERPRISE_PROJECT_MANAGEMENT_FLOW`

**File:** [`enterprise-development.md`](enterprise-development.md)

Runs the full enterprise project lifecycle from scope analysis to post-release review. It coordinates 18 role agents, creates and validates project artifacts, enforces formal gate criteria, and advances only when each step's exit criteria are met.

Unlike the startup workflow, this flow respects formal governance, approval gates, scope control, UAT acceptance, release governance, and audit-ready documentation. It interrupts the user **only** for blocking clarifications, mandatory approvals, or human decisions on scope, budget, UAT, release, or production risk.

Optimizes for: scope control, traceability, formal approval, estimation accuracy, delivery predictability, risk visibility, and audit-safe documentation.

Key sections:
- Enterprise execution principle
- 18 role agents (Orchestrator, PM, Product Owner, BA, UX, Team/Tech Leads, Developers, QA, Sponsor, UAT Owner, SME, DevOps, Finance, and more)
- Enterprise artifacts and interruption policy
- Clarification and approval formats
- Detailed workflow steps with agent activation per step
- Final delivery format and Definition of Done

## Choosing a Workflow

| | Startup (`quick-production.md`) | Enterprise (`enterprise-development.md`) |
|---|---|---|
| **Goal** | Ship working software fast | Controlled, auditable delivery |
| **Approval gates** | None — fully autonomous | Formal, multi-level |
| **Documentation** | Lightweight | Audit-ready |
| **Interrupts user** | Only if truly blocked | For clarifications, approvals, key decisions |
| **Best for** | MVPs, prototypes, fast iteration | Regulated, governed, large-scale projects |

## Usage

These files are specifications, not executable scripts. Provide the relevant command file as instructions to an agentic system (e.g. a coding agent), supply your project scope and feature list, and the agent follows the defined roles, artifacts, and steps to deliver the software.
