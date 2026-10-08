# AI Skills Repository

# 💫 About Me khan somrith:

## 🌐 Socials:
[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/Eed7EX3eYG) [![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/khansomrith) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/KhanSomrith) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/KhanSomrith) [![TikTok](https://img.shields.io/badge/TikTok-%23000000.svg?logo=TikTok&logoColor=white)](https://tiktok.com/@khansomrith) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/@UCGVpz8QxoTH5iP38oeeA-1w)  

A curated collection of reusable, domain-specific AI instruction modules designed to help AI agents operate with clarity, structure, and engineering discipline.

## Overview

This repository contains professional-grade skill definitions for AI agents. Each skill provides:

- a clear role and operating context
- domain-specific best practices
- structured workflows for understanding, planning, building, testing, and reviewing work
- explicit quality and safety standards
- activation rules for when a skill should be used

Unlike ordinary chatbot prompts, these are instruction modules intended to shape how an AI system thinks and works in a given domain.

## Why this repository exists

AI agents perform best when they are equipped with relevant expertise before taking action. Skills provide that expertise in a reusable, modular format.

This enables:

- consistent engineering behavior across tasks and agents
- stronger quality assurance and review standards
- safer execution in sensitive or high-risk domains
- easier reuse across future projects and domains
- clearer separation between what is designed, tested, simulated, and verified

## Core concepts

### What is an AI skill?

An AI skill is a self-contained instruction module that:

- defines the agent's role and responsibilities
- establishes professional principles for the target domain
- provides structured operational workflows
- identifies when to activate and when to defer
- explains how to reason about tradeoffs, constraints, and priorities
- includes review and verification standards

### Priority system

Skills are designed to work together under a clear hierarchy:

1. Safety and security
2. User requirements
3. Project constraints
4. Specialized skill instructions
5. General engineering best practices
6. Optional improvements

This ensures that no skill can override higher-priority rules.

### Engineering honesty

All agents using this repository are expected to distinguish accurately between:

- designed
- reviewed
- simulated
- tested
- verified
- manufactured
- validated

The repository emphasizes transparent reporting about what was actually performed and what remains unverified.

## Repository structure

```text
ai-skills/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── skill-authoring.md
│   └── skill-selection.md
├── examples/
│   ├── multi-skill-agent.md
│   ├── pcb-agent.md
│   └── website-agent.md
├── skills/
│   ├── electronics/
│   ├── pcb-engineering/
│   └── web-development/
├── templates/
│   ├── PROJECT_SKILL_TEMPLATE.md
│   └── SKILL_TEMPLATE.md
└── .
```

## Available skills

| Skill | Category | Version | Status | Description |
|---|---|---:|---|---|
| [web-development](skills/web-development/SKILL.md) | Software Engineering | 1.0.0 | Production | End-to-end guidance for building professional websites and web applications with quality, security, and maintainability in mind. |
| [pcb-engineering](skills/pcb-engineering/SKILL.md) | Electronics Engineering | 1.0.0 | Production | Domain-specific workflow for PCB design, validation, manufacturability, and engineering honesty in hardware projects. |
| [electronics](skills/electronics/README.md) | Electronics Engineering | — | Available | Supporting guidance for electronics-focused work, design review, and domain-specific engineering decisions. |

## Typical workflow

When a task arrives, the agent should follow this pattern:

1. analyze the request and identify the domain
2. discover relevant skills by metadata and activation keywords
3. select the best-fit skill or combination of skills
4. load the full skill instructions before acting
5. resolve conflicts according to the priority order
6. understand the problem and constraints
7. plan the implementation
8. build the solution in a careful, maintainable way
9. test and review against quality criteria
10. deliver a final summary that is honest about what was done and what remains unverified

## Skill lifecycle

The repository supports a complete skill lifecycle:

1. Discovery
2. Selection
3. Loading
4. Planning
5. Execution
6. Testing
7. Review
8. Delivery

This lifecycle keeps agent behavior consistent and predictable across different domains.

## Skill authoring

To create a new skill:

1. start from the template in [templates/SKILL_TEMPLATE.md](templates/SKILL_TEMPLATE.md)
2. add the required metadata and activation keywords
3. define the skill's domain, purpose, and boundaries
4. include workflows, standards, and review criteria
5. validate the skill against the repository guidance
6. document usage and expected behavior clearly

## Documentation

- [Skill Authoring Guide](docs/skill-authoring.md) — how to create and validate skill modules
- [Skill Selection Guide](docs/skill-selection.md) — how agents discover and compose skills
- [Architecture](docs/architecture.md) — repository design and system principles
- [Skill Template](templates/SKILL_TEMPLATE.md) — base template for writing a new skill
- [Project Skill Template](templates/PROJECT_SKILL_TEMPLATE.md) — guidance for multi-skill coordination

## Planned growth

The repository is structured to support expansion across domains such as:

- Web development
- Frontend engineering
- Backend engineering
- Full-stack development
- Mobile app development
- PCB design
- Electronics engineering
- Embedded systems
- Robotics
- Data engineering
- AI and machine learning
- Security
- DevOps and cloud engineering
- UX design and product engineering

## Contributing

Contributions are welcome. When adding or modifying skills:

- maintain the repository architecture and naming conventions
- use the skill templates as the starting point
- preserve consistency with existing guidance and standards
- favor clarity and reasoning over command-like shortcuts
- respect engineering honesty and priority rules
- update relevant documentation when new capabilities are introduced
- apply semantic versioning appropriately

## Support

### GitHub

https://github.com/khansomrith123

Best for:

- bug reports
- feature requests
- contribution discussions
- issue tracking

### Discord

https://discord.com/invite/Eed7EX3eYG

Best for:

- questions
- usage guidance
- community discussion
- support and feedback

Please note that response times are not guaranteed.

---

This repository is designed primarily for AI agents, while remaining useful to developers and engineers who maintain and extend the system. Every instruction module is written to be explicit, reusable, and grounded in good engineering practice.
