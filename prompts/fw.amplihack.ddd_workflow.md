# Document-Driven Development (DDD) Workflow

Systematic methodology for large features where documentation comes first and acts as the specification.

## Core Principle

Documentation IS the specification. Code implements what documentation describes.

## When to Use DDD

- New features requiring multiple files (10+ files)
- System redesigns or major refactoring
- API changes affecting documentation
- High-stakes user-facing features
- Complex integrations requiring clear contracts

## The 5-Phase Workflow

### Phase 1: Planning and Design

- Design feature before touching files
- Create comprehensive plan
- Build shared understanding
- Output: plan document

### Phase 2: Documentation Retcon

- Update docs, configs, READMEs
- Apply retcon writing (write as if feature already exists)
- Iterate until approved
- User must commit when satisfied

### Phase 3: Implementation Planning

- Assess current code vs new docs
- Plan all implementation changes
- Break into chunks
- User approval to proceed

### Phase 4: Code Implementation

- Write code matching docs exactly
- Test as user would
- Iterate until working
- User authorization for each commit

### Phase 5: Testing and Cleanup

- Clean temporary files
- Final verification
- Push/PR with explicit authorization

## Key Techniques

### Retcon Writing

Write documentation in present tense as if the feature already exists:

- "The authentication module handles..." (not "will handle")
- "Users can access..." (not "will be able to access")
- "The API returns..." (not "will return")

### Context Poisoning Prevention

- Maximum DRY: single source of truth
- Eliminate conflicting documentation
- Update all references when changing anything

### File Crawling

Process many files systematically with 99.5% token reduction by processing in batches rather than loading all at once.

## Authorization Model

- User controls all git operations
- No auto-commits
- Iteration supported in Phases 2 and 4
- Clear checkpoints with approval gates

## Philosophy Alignment

- **Ruthless Simplicity**: Start minimal, avoid future-proofing
- **Modular Design**: Bricks and studs, regeneratable from specs
- **Human Architects, AI Builds**: Human designs and reviews, AI implements

## Benefits

- Prevents context poisoning
- Reviewable design before expensive implementation
- No drift between docs and code
- AI-optimized workflow with clear specifications
