# Amplihack Framework Reference

Consolidated reference for the Amplihack agentic engineering framework.

## Framework Overview

Amplihack is a development framework that uses specialized AI agents to accelerate software development through intelligent automation and collaborative problem-solving. It provides 20 specialized agents, workflow orchestration, and a philosophy-driven approach to code quality.

## Core Philosophy

### Ruthless Simplicity

Start with the simplest solution that works. Add complexity only when justified. Question every abstraction.

### Brick Philosophy (Modular Design)

- **Brick** = Self-contained module with ONE responsibility
- **Stud** = Public contract others connect to
- **Regeneratable** = Can be rebuilt from specification
- **Isolated** = All code, tests, fixtures inside the module folder

### Zero-BS Implementation

No stubs or placeholders. No dead code. Every function must work or not exist.

## Agent Categories

### Core Agents (7)

| Agent | Role |
|-------|------|
| ah_reviewer | Code review and debugging specialist |
| ah_optimizer | Performance optimization expert |
| ah_architect | System design and module specification |
| ah_builder | Primary implementation agent |
| ah_api_designer | API contract design specialist |
| ah_guide | Interactive learning tutor |
| ah_tester | Test coverage and strategy expert |

### Specialized Agents (11)

| Agent | Role |
|-------|------|
| ah_cli_architect | CLI application and SDK integration architect |
| ah_worktree_manager | Git worktree management specialist |
| ah_knowledge_archaeologist | Deep research and knowledge excavation |
| ah_socratic_reviewer | Socratic questioning for code review |
| ah_concept_extractor | Knowledge component extraction |
| ah_integration | External integration and third-party API specialist |
| ah_fix_agent | Fix workflow orchestrator |
| ah_visualization_architect | Visual communication specialist |
| ah_philosophy_guardian | Philosophy compliance guardian |
| ah_insight_synthesizer | Revolutionary insight synthesis |
| ah_prompt_writer | Requirement clarification specialist |

### Workflow Agents (2)

| Agent | Role |
|-------|------|
| ah_prompt_review_workflow | Prompt review orchestration |
| ah_improvement_workflow | Progressive validation improvement workflow |

## Workflow Classification

| Task Type | Workflow | When to Use |
|-----------|----------|-------------|
| Q&A | Q&A Workflow | Simple questions, single-turn answers |
| Operations | Ops Workflow | Admin tasks, commands, cleanup |
| Investigation | Investigation Workflow | Understanding code, research |
| Development | Default Workflow | Code changes, features, bugs |

## Decision Framework

When faced with implementation decisions:

1. **Necessity**: Do we actually need this right now?
2. **Simplicity**: What is the simplest way to solve this?
3. **Modularity**: Can this be a self-contained brick?
4. **Regenerability**: Can AI rebuild this from a specification?
5. **Value**: Does the complexity add proportional value?

## Trust Principles

- Disagree when you see flaws
- Clarify when requests are ambiguous
- Propose alternatives when you see better ways
- Admit when you do not know
- Be direct with no hedging

## Priority Hierarchy

1. Explicit User Requirements (highest - never override)
2. Workflow Definition
3. Implicit User Preferences
4. Project Philosophy
5. Default Behaviors (lowest)
