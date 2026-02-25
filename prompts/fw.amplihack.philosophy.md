# Amplihack Development Philosophy

Core development philosophy guiding all software built with the Amplihack framework.

## The Zen of Simple Code

- **Wabi-sabi philosophy**: Embracing simplicity and the essential. Each line serves a clear purpose.
- **Occam's Razor thinking**: The solution should be as simple as possible, but no simpler.
- **Trust in emergence**: Complex systems work best when built from simple, well-defined components.
- **Present-moment focus**: Handle what is needed now rather than anticipating every possible future.

## The Brick Philosophy for AI Development

"We provide the blueprint, and AI builds the product, one modular piece at a time."

- **A brick** = Self-contained module with ONE clear responsibility
- **A stud** = Public contract (functions, API, data model) others connect to
- **Regeneratable** = Can be rebuilt from spec without breaking connections
- **Isolated** = All code, tests, fixtures inside the module's folder

## Core Design Principles

### 1. Ruthless Simplicity

- KISS principle taken to heart
- Minimize abstractions: every layer must justify its existence
- Start minimal, grow as needed
- Avoid future-proofing for hypothetical requirements

### 2. Modular Architecture for AI

- Preserve key architectural patterns with clear module boundaries
- Simplify implementations while maintaining pattern benefits
- Every module can be rebuilt from its specification

### 3. Zero-BS Implementations

- Every function must work or not exist; no stubs or placeholders
- No dead code, unimplemented functions, or TODOs in code
- No faked APIs or mock implementations (except in tests)
- No swallowed exceptions

### 4. Library vs Custom Code

- Custom code when the need is simple and well-understood
- Libraries when they solve complex problems you would rather not tackle
- Keep library integration points minimal and isolated

## Decision-Making Framework

1. **Necessity**: "Do we actually need this right now?"
2. **Simplicity**: "What is the simplest way to solve this?"
3. **Modularity**: "Can this be a self-contained brick?"
4. **Regenerability**: "Can AI rebuild this from a specification?"
5. **Value**: "Does the complexity add proportional value?"

## Proportionality Principle

Effort must match complexity:

- Config changes: minimal testing (1:1 to 2:1 ratio)
- Simple functions: basic coverage (2:1 to 4:1)
- Business logic: comprehensive (3:1 to 8:1)
- Critical paths: exhaustive (5:1 to 15:1)

## Remember

- It is easier to add complexity later than to remove it
- Code you do not write has no bugs
- Favor clarity over cleverness
- The best code is often the simplest
- Modules should be bricks: self-contained and regeneratable
