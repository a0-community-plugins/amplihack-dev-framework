# Frontmatter Standards

YAML frontmatter provides machine-readable metadata for all extensibility mechanisms.

## Purpose

1. **Automatic discovery** - Tools can find and catalog all components
2. **Dependency tracking** - Understand what invokes what
3. **Philosophy validation** - Verify alignment with core principles
4. **Version management** - Track breaking changes
5. **Auto-documentation** - Generate guides from metadata

## Standards by Component Type

### Commands

```yaml
---
name: command-name          # Kebab-case, matches /command-name
version: 1.0.0              # Semantic versioning
description: One-line summary  # Under 80 characters
triggers:                    # User request patterns
  - "Pattern that suggests this command"
---
```

### Skills

```yaml
---
name: skill-name
version: 1.0.0
description: One-line summary
triggers:
  - "Context or request that activates"
---
```

### Subagents (Agents)

```yaml
---
name: agent-name
version: 1.0.0
description: Detailed description with usage examples
role: "Agent's specialized role"
model: inherit
---
```

### Workflows

```yaml
---
name: workflow-name
version: 1.0.0
description: What this workflow orchestrates
type: workflow
---
```

## Versioning Rules

- **MAJOR**: Breaking changes (changed interface, removed features)
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (no interface changes)

## Naming Conventions

- Commands: kebab-case (`expert-panel`, `knowledge-builder`)
- Skills: kebab-case (`session-learning`, `code-visualizer`)
- Agents: kebab-case (`fix-agent`, `philosophy-guardian`)
- Workflows: SCREAMING_SNAKE_CASE (`DEFAULT_WORKFLOW`, `INVESTIGATION_WORKFLOW`)
