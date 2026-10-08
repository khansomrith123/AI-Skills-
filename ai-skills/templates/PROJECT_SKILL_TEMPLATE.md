---
name: project-skill-template
version: 1.0.0
description: Template for composite projects using multiple skills with orchestration guidance
category: project-management
tags:
  - multi-skill
  - composition
  - orchestration
  - project-template
activation:
  - define multi-skill project
  - combine skills for project
  - orchestrate multiple skills
---

# Project Skill Template (Multi-Skill Composition)

## 1. Identity

**Purpose:** This is a composition/orchestration template, not a standalone skill. It defines which skills are needed for a project type and how they should work together.

**Scope:** Planning multi-skill coordination, resolving conflicts, sharing requirements, and maintaining coherent execution.

**Distinction:** Unlike individual skills, this template focuses on "which skills and how they cooperate", not domain-specific implementation details.

## 2. Purpose

This template helps an AI agent:

- Identify required and optional skills for a project class.
- Define skill composition and primary/secondary roles.
- Establish shared requirements across skills.
- Resolve conflicts via the global priority system.
- Create a unified workflow across multiple skills.
- Ensure no skill overrides higher-priority rules.
- Prevent duplication or contradiction between skills.

## 3. Project Definition

### Project Metadata

- **Project Type:** [e.g., Website Project, PCB Project, AI Project]
- **Project Name:** [Name/identifier]
- **Description:** [Brief project description]
- **Complexity:** [simple | moderate | complex]
- **Primary Goal:** [Main objective]

### Project Objective

[Clearly state what the project aims to achieve and success criteria.]

## 4. User Requirements

### Core Requirements

- [Requirement 1]
- [Requirement 2]
- [Requirement 3]

### Non-Functional Requirements

- [Performance, security, usability, etc.]
- [Constraints: budget, timeline, resources]

### Constraints

- [Technical constraints]
- [Platform/environment constraints]
- [Compliance/regulatory constraints if any]

## 5. Required Skills

List skills that are essential for this project type.

| Skill | Purpose in Project | Contribution |
|---|---|---|
| [web-development / pcb-engineering / etc.] | [Why required] | [What it provides] |
| [skill-name-2] | [Why required] | [What it provides] |

## 6. Optional Skills

List skills that may be useful depending on scope.

| Skill | When to Include | Contribution |
|---|---|---|
| [skill-name] | [Trigger conditions] | [What it adds] |

## 7. Skill Activation Rules

Define when each skill activates in this project context:

- **Primary skill(s):** [Which skill(s) drive architecture and workflow?]
- **Secondary skill(s):** [Which activate based on specific sub-tasks?]
- **Conditional activation:** [Conditions for including optional skills]
- **Exclusion rules:** [When not to load certain skills]

## 8. Skill Priority

Apply the global priority system. For this project, clarify application:

1. **Safety and security** – Highest priority across all skills.
2. **User requirements** – Override skill preferences if conflicting.
3. **Project constraints** – Must be respected by all skills.
4. **Specialized skill instructions** – Apply per skill, but resolve conflicts by priority.
5. **General engineering best practices** – Shared across skills.
6. **Optional improvements** – Lowest priority.

**Conflict resolution rule:** If any loaded skill conflicts with a higher-priority rule, the higher-priority rule wins. The agent must not allow a skill to override safety/security, user requirements, or project constraints.

## 9. Skill Dependencies

Define relationships between skills:

| From Skill | To Skill | Relationship | Notes |
|---|---|---|---|
| [skill A] | [skill B] | [depends on / complements / informs] | [How they interact] |

## 10. Skill Composition

### Composition Model

Describe how skills combine:

- **Orchestration approach:** [Sequential, parallel by phase, or task-based?]
- **Primary coordinator:** The agent acts as orchestrator, applying each skill only where relevant.
- **Boundaries:** Each skill stays in its domain; avoid overlapping guidance.
- **Unification:** Merge outputs into one coherent plan/solution.

### Role Assignment

- **Lead skill:** [Drives overall structure/workflow]
- **Supporting skills:** [Handle specialized subdomains]
- **Cross-cutting skills:** [Apply across all work (e.g., security)]

## 11. Shared Requirements

Identify requirements that affect multiple skills:

- **Security**: Shared security requirements all skills must respect.
- **Data/model sharing**: Common data structures, types, interfaces.
- **Standards**: Shared naming, formatting, conventions.
- **Constraints**: Shared constraints enforced across all loaded skills.
- **Honesty**: Shared engineering honesty rules.
- **Testing**: Coordinated testing approach.

## 12. Conflict Resolution

### Conflict Types

- **Direct contradiction**: Conflicting instructions between skills.
- **Overlapping scope**: Both skills address same concern.
- **Priority conflict**: Skill suggests action violating higher priority.

### Resolution Strategy

1. **Identify conflict** – Detect contradiction/overlap explicitly.
2. **Apply priority order** – Resolve using global priority system.
3. **Preserve safety** – Never compromise safety/security.
4. **Minimize scope** – Apply each skill only to relevant tasks.
5. **Document resolution** – State how conflict resolved if significant.
6. **Prefer clarity** – Choose simpler, clearer approach.

## 13. Project Workflow

Unified workflow combining all loaded skills:

### Phase 1: Understand (All Skills)
- Analyze request against all relevant skills.
- Collect shared requirements.
- Identify which skills to load and why.
- Check for conflicts early.

### Phase 2: Plan (Orchestrated)
- Create unified plan respecting all loaded skills.
- Assign responsibilities by skill domain.
- Define integration points.
- Identify risks across domains.
- Validate plan against priorities.

### Phase 3: Build (Domain-Specific)
- Execute domain tasks using appropriate skill guidance.
- Maintain shared interfaces/contracts.
- Coordinate handoffs between domains.
- Avoid duplication.

### Phase 4: Test (Coordinated)
- Test within each domain per its skill.
- Integration testing across domains.
- Validate shared constraints satisfied.
- Be honest about what was tested.

### Phase 5: Review (Cross-Domain)
- Review against each skill's QA checklist where applicable.
- Cross-check integration points.
- Verify no priority violations.
- Confirm engineering honesty.
- Validate completeness.

### Phase 6: Deliver (Unified)
- Provide single coherent response.
- Clearly state what was done per domain if relevant.
- State testing/verification status honestly.
- Document limitations across domains.

## 14. Verification Criteria

Overall project verification:

- [ ] All required skills identified and loaded appropriately.
- [ ] Optional skills included only when justified.
- [ ] Conflicts resolved via priority system.
- [ ] Shared requirements satisfied across all domains.
- [ ] No skill violated higher-priority rules.
- [ ] Integration between domains works coherently.
- [ ] Each domain's critical QA items satisfied.
- [ ] Engineering honesty maintained throughout.
- [ ] Unified delivery is clear and complete.

## 15. Final Review

Before delivery:

1. **Composition check** – Skills used appropriately?
2. **Priority compliance** – All actions respect priority order?
3. **No duplication** – Avoided redundant work?
4. **Coherence** – Solution feels unified, not stitched?
5. **Honesty** – Status claims accurate across domains.
6. **Completeness** – Meets all user requirements.
7. **Safety/security** – No compromises.

## 16. Delivery Requirements

Unified delivery must include:

1. **Project summary** – Overall accomplishment.
2. **Skills used** – List required/optional skills and rationale.
3. **Changes** – All files created/modified across domains.
4. **Domain breakdown** – Brief what each skill contributed (concise).
5. **Integration notes** – How domains connect.
6. **Testing status** – Honest status for each relevant domain.
7. **Limitations** – Cross-domain caveats/unverified items.
8. **Usage** – How to build/run/use complete solution.
9. **Next steps** if needed.

---

**Note:** This template is for orchestration only. For domain implementation, load and follow the relevant individual skill files (SKILL.md). Never let composition override the global priority system (Safety & Security > User Requirements > Project Constraints > Specialized Skill Instructions > General Best Practices > Optional Improvements).