# Skill Authoring Guide

## Purpose

This guide explains how to author, version, validate, and maintain AI skills for this repository. Skills must be reusable instruction modules that teach AI agents how to think, not just execute commands.

## Core Principles

- **Self-contained**: A skill must contain all context needed to apply it without relying on external prompts.
- **Teaches thinking**: Focus on reasoning, principles, workflows, and decision-making.
- **Domain-specific**: Be precise about scope, boundaries, and when to defer to other skills.
- **Priority-aware**: Respect the global priority system at all times.
- **Technology-agnostic by default**: Never force frameworks/languages; choose based on requirements.
- **Engineering honesty**: Explicitly distinguish designed, reviewed, simulated, tested, verified, manufactured, validated.
- **Pragmatic**: Avoid unnecessary complexity; favor simplicity that meets requirements.

## Prerequisites

Before creating a skill, review:
- [README.md](../README.md) – Repository philosophy, priorities, workflows
- [SKILL_TEMPLATE.md](../templates/SKILL_TEMPLATE.md) – Canonical structure
- [PROJECT_SKILL_TEMPLATE.md](../templates/PROJECT_SKILL_TEMPLATE.md) – For multi-skill composition
- [architecture.md](architecture.md) – Architecture and design decisions
- [skill-selection.md](skill-selection.md) – How skills are discovered/selected

## Step-by-Step: Creating a New Skill

1. **Choose location**: Create a directory under `skills/<skill-slug>/` (use kebab-case).
2. **Copy template**: Copy `templates/SKILL_TEMPLATE.md` to `skills/<skill-slug>/SKILL.md`.
3. **Add metadata**: Fill frontmatter accurately (name, version, description, category, tags, activation).
4. **Write content**: Complete all 21 sections with domain-specific, actionable guidance.
5. **Create README**: Add `skills/<skill-slug>/README.md` summarizing purpose, usage, scope.
6. **Add examples**: Create `skills/<skill-slug>/examples/` with practical scenarios.
7. **Validate**: Use the validation checklist below.
8. **Version appropriately**: Set initial version (usually 1.0.0).

## Skill Metadata Requirements

Each skill must include frontmatter:

```yaml
---
name: web-development
version: 1.0.0
description: Professional website development skill
category: software-engineering
tags:
  - website
  - frontend
  - backend
  - web
activation:
  - build a website
  - create a web app
  - fix website code
  - improve frontend
---
```

### Metadata Guidelines

- **name**: Unique, kebab-case, matches directory name.
- **version**: Semantic versioning (MAJOR.MINOR.PATCH).
- **description**: Concise (1–2 lines) describing domain coverage.
- **category**: Choose from: software-engineering, electronics-engineering, mechanical-engineering, data-science, devops, security, design, research, project-management (or add new if needed).
- **tags**: 3–6 relevant tags for discovery.
- **activation**: 4–8 concrete example user requests that should trigger this skill.

## Writing Guidelines

### Teach "How to Think", Not "How to Command"

- **Bad**: "Run `npm install && npm run build`"
- **Good**: "Understand dependencies and build requirements, choose appropriate commands based on project setup, verify build artifacts."

### Be Specific and Actionable

- Provide clear decision criteria.
- Include concrete steps in workflows.
- Give examples where helpful.
- Avoid vague statements like "do it well".

### Respect Boundaries

- Define clear "When to Activate" and "When NOT to Activate".
- Explicitly state what the skill does NOT cover.
- Guide when to defer to other skills.

### Maintain Consistency

- Follow the 21-section structure from SKILL_TEMPLATE.md.
- Use consistent terminology across skills.
- Reference global principles (honesty, priority, work order).
- Match style with existing skills.

### Avoid Common Pitfalls

- Don't over-document trivial things.
- Don't force technology choices.
- Don't duplicate generic advice; focus on domain specifics.
- Don't assume external context.
- Don't add unnecessary comments guidance that conflicts with system rules.

## Versioning (Semantic Versioning)

Skills use `MAJOR.MINOR.PATCH`:

| Version | When to Increment | Example |
|---|---|---|
| **MAJOR** | Breaking changes to core logic, role, principles, or priority guidance that changes how the skill is applied. | 1.0.0 → 2.0.0 |
| **MINOR** | Backward-compatible additions: new sections, expanded guidance, more examples, new activation terms. | 1.0.0 → 1.1.0 |
| **PATCH** | Backward-compatible fixes: clarifications, typos, wording improvements, small corrections. | 1.0.0 → 1.0.1 |

Update the `version` in frontmatter with each change. For significant changes, consider documenting in the skill's README.

## Validation Checklist

Before publishing/updating a skill, verify:

### Structure & Completeness

- [ ] Uses correct frontmatter with all required fields.
- [ ] Follows 21-section structure from SKILL_TEMPLATE.md.
- [ ] All sections contain meaningful, instructional content (no empty placeholders).
- [ ] `name` matches directory slug.
- [ ] File names correct: `SKILL.md`, `README.md`, `examples/` directory.

### Content Quality

- [ ] **Self-contained**: Can be applied without external instruction files.
- [ ] **Teaches thinking**: Emphasizes principles, reasoning, workflows over commands.
- [ ] **Clear activation**: "When to Activate" has concrete triggers and examples.
- [ ] **Clear boundaries**: "When NOT to Activate" specifies when to defer.
- [ ] **Engineering honesty**: Includes/acknowledges honesty rules where relevant.
- [ ] **Priority-aware**: Respects global priority system (references appropriately).
- [ ] **Technology-agnostic**: No forced frameworks; requires requirement-based selection.
- [ ] **Work order**: References/follows Understand → Plan → Build → Test → Review → Deliver.
- [ ] **Actionable QA**: Quality Assurance section has concrete checklist items.
- [ ] **Pragmatic**: Avoids over-engineering and unnecessary complexity.

### Consistency

- [ ] Terminology matches repository (honesty terms, priority order, work order).
- [ ] Metadata format consistent with existing skills.
- [ ] Style consistent with other skills.
- [ ] No conflicts with global README/architecture.
- [ ] Compatible with single-skill and multi-skill workflows.

### Usability

- [ ] Understandable by AI agents without this conversation context.
- [ ] Clear for human maintainers.
- [ ] Examples are realistic and helpful.
- [ ] Common mistakes section is relevant and actionable.

## Testing a Skill

While automated tests aren't required for instruction modules, validate practically:

1. **Readability test**: Can another AI agent understand the skill's core logic from a single read?
2. **Activation test**: Does it trigger appropriately for its activation examples?
3. **Boundary test**: Does it correctly avoid triggering for out-of-scope cases?
4. **Workflow test**: Does the workflow make sense end-to-end?
5. **Multi-skill test**: If designed to compose with others, check for conflicts/overlaps.

## Skill README Requirements

Each skill directory should have a `README.md` containing:

- **Title and brief description**
- **Purpose**: What this skill is for
- **When to use**: Activation scenarios
- **When not to use**: Boundaries
- **Key features**: Major coverage areas
- **Quick start**: How an agent loads/uses it
- **Files**: List of files in directory (SKILL.md, examples/)
- **Version**: Current version
- **Related skills**: Potential complements

Keep it concise (50–150 lines typically).

## Examples

Create example scenarios in `examples/` showing:

- Typical use cases
- How the skill applies workflows
- Expected behaviors
- Integration with other skills (if multi-skill relevant)

Examples help validate clarity and demonstrate proper usage.

## Maintenance

- **Keep current**: Update when domain practices evolve.
- **Clarify, don't bloat**: Prefer refinement over expansion.
- **Version properly**: Follow semantic versioning on changes.
- **Cross-reference**: Update related docs if changing core concepts.
- **Backward compatibility**: Minimize breaking changes; document if unavoidable.

## Governance Notes

- Skills must not override higher-priority rules (Safety & Security first).
- Engineering honesty is non-negotiable.
- Technology choices must be requirement-driven.
- Simplicity is preferred over cleverness.
- Teach thinking, not commands.

---

For questions or clarifications, refer to [architecture.md](architecture.md) and [skill-selection.md](skill-selection.md).
