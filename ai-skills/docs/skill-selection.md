# Skill Selection Guide

## Purpose

This guide explains how AI agents should discover, select, activate, and compose skills from this repository. It ensures consistent, appropriate skill usage across single-skill and multi-skill scenarios.

## Core Principles

- **Right tool for the job**: Select skills that best match the user's request and context.
- **Minimal selection**: Use the fewest skills necessary to address the task well.
- **Priority-aware**: Always respect the global priority system during selection and execution.
- **Context-driven**: Consider existing files, project structure, and constraints.
- **Precise over broad**: Prefer specific skills over generic ones when scope is clear.
- **Honesty-driven**: Selected skills must support engineering honesty practices.

## Discovery

Skills are discovered through machine-readable metadata in each `SKILL.md` frontmatter:

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

### Discovery Sources

- **Activation keywords**: Match user request against `activation` phrases.
- **Tags**: Match domain-relevant tags.
- **Name/category**: Direct lookup by skill name or category.
- **Content analysis**: Infer domain from request (files mentioned, project type, terminology).

## Activation Criteria

A skill should activate if ANY of these hold:

1. **Direct match**: User request explicitly matches activation examples or intent.
2. **Domain match**: Request clearly falls within the skill's Identity/Scope.
3. **File context**: Existing files suggest the domain (e.g., `.kicad_pcb`, `.sch`, `.brd` files suggest PCB-related work; HTML/CSS/JS suggest web).
4. **Task type**: Task is to design/build/review/fix within the skill's domain.
5. **Problem domain**: User describes domain-specific problems the skill addresses.

## When NOT to Activate

Do not activate a skill if:

- Request is clearly outside its stated scope ("When NOT to Activate").
- Another more specific skill is a better fit.
- Task is purely informational with no implementation/design work needed.
- Activation would violate boundaries defined in the skill.
- Context strongly indicates different domain.

## Selection Process

### Step 1: Analyze Request
- Parse user intent, goal, scope.
- Identify domain keywords and concepts.
- Note any files, paths, or project references mentioned.
- Identify constraints or explicit tech preferences.

### Step 2: Discover Candidates
- Scan all skills' metadata for matches.
- Consider activation phrases, tags, category.
- Look at existing files in workspace for domain hints.

### Step 3: Score & Filter
- **High confidence**: Direct activation match + context supports.
- **Medium confidence**: Domain match but no direct phrase match.
- **Low confidence**: Weak signals; likely not appropriate.

Filter out low-confidence candidates unless strongly justified.

### Step 4: Select Minimal Set
- Choose primary skill(s) covering core work.
- Add secondary skills only if sub-tasks require distinct domain expertise.
- Avoid loading skills "just in case".
- Prefer 1 skill when scope is clean; use multiple only when necessary.

### Step 5: Validate Selection
- Does each selected skill address a real need?
- Are there overlaps? Can they be avoided?
- Is the combination coherent?
- Does selection respect boundaries?

## Single-Skill Selection

Use single skill when:

- Task is clearly scoped to one domain.
- No cross-domain integration needed.
- Adding other skills doesn't add value.
- Boundaries are well-defined.

**Examples:**
- "Fix CSS layout issue" → `web-development`
- "Review PCB schematic" → `pcb-engineering`
- "Add API endpoint" → `web-development` / `api-development` depending on specificity

## Multi-Skill Selection

Use multiple skills when:

- Project spans multiple domains.
- Different phases require distinct expertise.
- Integration between domains is required.
- Subsystems need specialized handling.

**Examples:**
- **Website project**: `web-development` + `ui-ux-design` + `backend-engineering` + `database-engineering` + `security`
- **PCB project**: `pcb-engineering` + `electronics-engineering` + `embedded-systems`
- **AI project**: `ai-ml` + `python-development` + `backend-engineering` + `database-engineering`

## Skill Composition Rules

### Primary vs Secondary

- **Primary skill(s)**: Drive overall architecture, workflow, and success criteria.
- **Secondary skill(s)**: Provide specialized support for specific aspects.
- **Assign clear roles**: Each skill should have a distinct contribution.

### Avoid Duplication

- Don't load two skills covering identical concerns.
- Apply each skill only to its relevant sections/domains.
- If overlap exists, use the more specific skill or apply priority.
- Don't repeat the same guidance from multiple skills.

### Maintain Coherence

- Create a unified plan across all skills.
- Define shared interfaces/contracts between domains.
- Ensure outputs integrate cleanly.
- Keep terminology consistent.

### Respect Boundaries

- Let each skill own its domain expertise.
- Don't force one skill's patterns onto another domain.
- Defer to the appropriate skill for domain-specific decisions.

## Priority Application During Selection

1. **Safety and security** – Non-negotiable.
2. **User requirements** – Satisfy explicit valid requirements.
3. **Project constraints** – Respect stated constraints.
4. **Specialized skill instructions** – Apply loaded skills.
5. **General engineering best practices** – Apply sound principles.
6. **Optional improvements** – Only if no higher priority conflicts.

**Rule:** No skill may override higher-priority rules.

## Conflict Resolution

### Detecting Conflicts

- **Direct contradiction**: Opposing instructions between skills.
- **Scope overlap**: Both address same concern differently.
- **Priority violation**: A skill suggests violating higher priority.
- **Incompatible approaches**: Approaches that don't integrate well.

### Resolving Conflicts

1. **Identify**: Explicitly recognize the conflict.
2. **Prioritize**: Apply global priority order.
3. **Minimize scope**: Restrict each skill to its clearest domain.
4. **Choose simplest**: Prefer simpler, safer approach meeting requirements.
5. **Document**: Briefly note significant resolutions if they affect outcome.
6. **Preserve safety**: Never compromise safety/security.

## Context Awareness

Consider project context:

- **Existing files**: Look for file types, configs, structure.
- **Directory layout**: Suggests domains.
- **README/docs**: Reveal project type.
- **Constraints mentioned**: "no frameworks", "minimal", etc.

## Loading Skills

1. **Read completely**: Load full `SKILL.md` for each selected skill before acting.
2. **Understand applicability**: Identify which sections apply to current task.
3. **Extract relevant parts**: Apply only relevant workflows/principles.
4. **Merge guidance**: Combine into coherent approach.
5. **Stay flexible**: Don't blindly apply irrelevant instructions.
6. **Verify alignment**: Check against priorities throughout.

## Skill Selection Checklist

- [ ] Analyzed request thoroughly.
- [ ] Discovered relevant candidates via metadata/context.
- [ ] Selected minimal set.
- [ ] Primary/secondary roles defined for multi-skill.
- [ ] No obvious duplication/overlap issues.
- [ ] Selection respects boundaries.
- [ ] All loaded skills align with priority system.
- [ ] Context supports selection.

## Examples

**Example 1: Single Skill**  
Request: "Create simple landing page" → `web-development` (primary).

**Example 2: Multi-Skill (Web + Security)**  
Request: "Build secure web app with auth and DB" → `web-development` (primary), `database-engineering` (secondary), `security` (cross-cutting).

**Example 3: Multi-Skill (PCB)**  
Request: "MCU-based PCB with sensor" → `pcb-engineering` (primary), `electronics-engineering` (secondary), `embedded-systems` (secondary).

**Example 4: Avoid Over-Selection**  
Request: "Fix typo in README" → Likely no specialized skill needed; use general best practices.

---

**Key Takeaway:** Select the right skills, load them fully, apply only relevant parts, resolve conflicts by priority, and maintain coherence.