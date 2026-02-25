# Fix Workflow

Intelligent fix workflow that executes a complete multi-step process with pattern-specific context for quality-focused issue resolution.

## Core Philosophy

### Single Workflow Path

One workflow path for all fixes. No branching logic.

```
/fix [pattern] -> Complete Workflow (All Steps) -> Tested, documented fix
```

### Patterns As Context (Not Modes)

Patterns do not create different workflows - they provide context:

- Pattern detection identifies the error type
- Context informs which specialized agents to invoke
- Workflow remains the same regardless of pattern
- Templates are validation tools, not shortcuts

## Error Patterns

| Pattern | Frequency | Scope |
|---------|-----------|-------|
| import | 15% | Missing imports, circular deps, path issues |
| ci | 20% | Pipeline config, dependency conflicts, build env |
| test | 18% | Assertion errors, mock setup, test data |
| config | 12% | Env vars, config syntax, missing settings |
| quality | 25% | Linting, type errors, formatting |
| logic | 10% | Algorithm bugs, edge cases, state management |

## Pattern-Specific Agent Selection

Patterns inform which agents to invoke at the design step:

- **import** -> dependency analyzer
- **ci** -> CI diagnostic agent
- **test** -> tester agent, reviewer agent
- **config** -> environment agent, validator
- **quality** -> reviewer agent, cleanup agent
- **logic** -> architect agent, analyzer agent

## Success Criteria

Fix is complete only when ALL workflow steps execute:

1. **Correctness**: Fix resolves root cause
2. **Completeness**: All steps completed
3. **Quality**: Code meets standards
4. **Testing**: All tests pass (local and CI)
5. **Documentation**: Changes documented
6. **Integration**: PR merged successfully

## Remember

- No shortcuts: all steps execute for every fix
- Quality over speed
- Pattern as context, not mode
- Templates as validation tools within testing step
