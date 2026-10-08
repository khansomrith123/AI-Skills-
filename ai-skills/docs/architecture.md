# Architecture

## Purpose

This document defines the architectural design of the AI Skills Repository: how skills are structured, discovered, selected, composed, and applied. It ensures consistency, scalability, and adherence to core principles.

## Design Goals

- **Reusability**: Skills are reusable instruction modules across different AI agents.
- **Self-containment**: Each skill is complete and understandable on its own.
- **Scalability**: Easy to add new skills without restructuring the whole system.
- **Composability**: Support for single-skill and multi-skill workflows.
- **Clarity**: Clear separation of concerns between templates, docs, skills, and examples.
- **Safety-first**: Enforce priority system and engineering honesty.
- **Agent-centric**: Written for AI agents to read and apply.

## Repository Structure

```
ai-skills/
│
├── README.md                        # Main entry point
│
├── templates/
│   ├── SKILL_TEMPLATE.md             # Canonical template for individual skills
│   └── PROJECT_SKILL_TEMPLATE.md     # Template for multi-skill composition
│
├── docs/
│   ├── skill-authoring.md             # Authoring guide
│   ├── skill-selection.md             # Selection/composition guide
│   └── architecture.md                # This document
│
├── skills/
│   ├── web-development/
│   │   ├── SKILL.md                   # Full skill instruction module
│   │   ├── README.md                  # Skill summary
│   │   └── examples/                  # Usage examples
│   │
│   ├── pcb-engineering/
│   │   ├── SKILL.md
│   │   ├── README.md
│   │   └── examples/
│   │
│   └── electronics/
│       ├── SKILL.md
│       └── README.md
│
└── examples/
    ├── website-agent.md               # End-to-end website example
    ├── pcb-agent.md                   # End-to-end PCB example
    └── multi-skill-agent.md           # Multi-skill coordination example
```

## Core Concepts

### Skill
A self-contained instruction module that teaches an AI agent how to think and act in a specific domain.

### Skill Metadata
Machine-readable frontmatter enables discovery/selection.

### Composition
Orchestrating multiple skills to handle cross-domain projects.

### Orchestration
Agent coordinates selection, loading, priority resolution, merging, and unified delivery.

## Priority System

| Priority | Rule | Notes |
|---|---|---|
| 1 | Safety and security | Never compromised |
| 2 | User requirements | Explicit valid requirements |
| 3 | Project constraints | Technical/legal/budget/resource |
| 4 | Specialized skill instructions | From loaded skills |
| 5 | General engineering best practices | Sound principles |
| 6 | Optional improvements | Only if no conflicts |

**Rule:** No skill may override higher-priority rules.

## Engineering Honesty

Never falsely claim: Tested, Simulated, Manufactured, Verified, Security audited, Electrically validated.

Must distinguish: Designed, Reviewed, Simulated, Tested, Verified, Manufactured, Validated.

## Work Order

1. Understand
2. Plan
3. Build
4. Test
5. Review
6. Deliver

## Technology Selection

- Requirement-driven
- No default bias
- Minimal complexity
- Prefer existing
- Justify additions
- Fit over trend

## Skill Structure (21 Sections)

1. Identity, 2. Purpose, 3. When to Activate, 4. When NOT to Activate, 5. Role, 6. Core Principles, 7. Requirements Analysis, 8. Planning Workflow, 9. Implementation Workflow, 10. Engineering Standards, 11. Architecture, 12. Security, 13. Error Handling, 14. Testing, 15. Quality Assurance, 16. Common Mistakes, 17. Performance, 18. Maintainability, 19. Documentation, 20. Final Review, 21. Final Response.

## Multi-Skill Architecture

- **Orchestrator**: Agent coordinates
- **Primary**: Drive flow/architecture
- **Secondary**: Domain expertise
- **Cross-cutting**: Apply broadly
- **Boundaries**: Apply only where relevant

### Conflict Resolution
Detect → Apply priority → Preserve safety → Minimize scope → Choose simplest safe → Apply.

## Discovery & Selection Flow

Request → Analyze → Discover → Filter → Select minimal set → Validate → Load completely → Resolve → Execute.

## Extensibility

Add skill: create dir, copy template, write SKILL.md + README + examples, update root README, validate. Structure scales to 25+ domains.

## File Naming

- Directories: kebab-case
- Skill files: SKILL.md, README.md
- Docs: kebab-case.md
- Examples: kebab-case.md

## Versioning

Skills version independently (semver). Templates aim for backward compatibility.

## Design Principles

Agent-first, minimal but complete, explicit over implicit, pragmatic, honest, safety-driven, composable, maintainable.

---

This architecture balances structure with flexibility for both single-skill and multi-skill coordination.