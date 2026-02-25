# Default Development Workflow

Standard multi-step workflow for all development tasks. Defines the execution methodology for features, bug fixes, and refactoring.

## Workflow Classification

Classify at topic boundaries before taking action:

| Task Type | Workflow | When to Use |
|-----------|----------|-------------|
| Q&A | Q&A Workflow | Simple questions, single-turn answers |
| Operations | Ops Workflow | Admin tasks, commands, cleanup |
| Investigation | Investigation Workflow | Understanding code, research |
| Development | Default Workflow | Code changes, features, bugs |

## Classification Keywords

- **Q&A**: "what is", "explain briefly", "quick question"
- **Operations**: "run command", "disk cleanup", "organize"
- **Investigation**: "investigate", "analyze", "research", "explore"
- **Development**: "implement", "add", "fix", "create", "refactor"

## The 22-Step Workflow

### Planning Phase (Steps 0-3)

0. **Prime Context**: Load workflow, identify task type
1. **Clarify Requirements**: Analyze requirements, document scope
2. **Create Issue**: Track work with issue/ticket
3. **Create Branch**: Feature branch from main

### Design Phase (Steps 4-5)

4. **Design Solution**: Invoke specialized agents for design
5. **Specify Modules**: Identify affected modules, plan changes

### Implementation Phase (Steps 6-8)

6. **Implement Changes**: Execute implementation
7. **Verify Implementation**: Check correctness, no regressions
8. **Mandatory Local Testing**: Pattern-specific validation

### Testing Phase (Steps 9-10)

9. **Run Tests**: Execute full test suite
10. **Fix Test Failures**: Address failures, ensure 100% pass

### Integration Phase (Steps 11-15)

11. **Commit Changes**: Descriptive commit message
12. **Push to Remote**: Push branch, trigger CI
13. **Create Pull Request**: PR with details
14. **Monitor CI Status**: Watch pipeline
15. **Fix CI Failures**: Iterate until CI passes

### Review Phase (Steps 16-18)

16. **Code Review**: Request and respond to review
17. **Address Feedback**: Implement requested changes
18. **Verify Standards**: Philosophy compliance check

### Finalization Phase (Steps 19-21)

19. **Final Validation**: Comprehensive check
20. **Merge Preparation**: Rebase, resolve conflicts
21. **Documentation Updates**: Document learnings

## Agent Delegation

### Parallel-Ready Agents

analyzer, security, optimizer, patterns, reviewer, architect, api-designer, database, tester, integration, cleanup

### Sequential-Required Agents

architect -> builder -> reviewer (hard dependencies)

## Operating Principles

- Always classify workflow FIRST
- Execute all steps in order
- Delegate to specialized agents at each step
- Use parallel execution when tasks are independent
- Track progress throughout
- Quality over speed
