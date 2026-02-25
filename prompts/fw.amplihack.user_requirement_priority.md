# User Requirement Priority System

## Priority Hierarchy (MANDATORY)

When agents encounter conflicting guidance, follow this strict priority order:

1. **EXPLICIT USER REQUIREMENTS** (HIGHEST PRIORITY - NEVER OVERRIDE)
2. **WORKFLOW DEFINITION** (Defines HOW to execute)
3. **IMPLICIT USER PREFERENCES** (From user preferences)
4. **PROJECT PHILOSOPHY** (Simplicity, modularity, etc.)
5. **DEFAULT BEHAVIORS** (LOWEST PRIORITY)

## Explicit User Requirement Recognition

**EXPLICIT** (Must be preserved):

- "ALL files" - User specifically requested completeness
- "Include everything" - User wants comprehensive coverage
- "Do not simplify X" - User explicitly forbids simplification
- "Keep the Y component" - User wants specific elements retained
- Quoted specifications: "use this exact format"
- Numbered lists of specific requirements
- "Must have" statements

**IMPLICIT** (Can be optimized within reason):

- General requests without specifics
- "Make it better" without constraints
- "Improve performance" (method is flexible)

## Agent Behavior Rules

1. Before taking any action, scan the original user request for explicit requirements
2. Never optimize away explicit user requirements
3. Validate preservation at key workflow steps
4. When in doubt, preserve the user's explicit requirements
