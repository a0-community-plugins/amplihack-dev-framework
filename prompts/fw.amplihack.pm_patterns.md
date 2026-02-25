# PM Architect Cognitive Offloading Patterns

How to decompose product management tasks into specialized agent-solvable units, reducing token pressure and enabling parallel execution.

## Core Principle

"What can you decompose and break apart into smaller, useful units? Have agents help solve for and build agents for tackling those smaller units first."

Benefits:

- Reduced cognitive load on single agent
- Reusable components for future epics
- Parallel execution for faster analysis
- Distributed token usage across focused contexts

## Decomposition Patterns

### Pattern 1: Epic Planning Decomposition

Decompose complex feature planning into specialized analysis tasks:

1. **user-research-agent**: Research user needs and expectations
2. **competitive-analysis-agent**: Analyze competitor patterns
3. **technical-feasibility-agent**: Evaluate technical constraints
4. **business-value-agent**: Assess value proposition and ROI
5. **security-agent**: Security requirements and threat model

Execute all tasks in parallel, synthesize results into epic plan.

### Pattern 2: Backlog Refinement at Scale

For large backlogs:

1. Create batch-processor agent with iteration tracking
2. Process first 10 items to identify patterns
3. Extract template from first 10
4. Apply template to remaining items in parallel batches
5. Review exceptions that do not fit the template

### Pattern 3: Multi-Workstream Coordination

For coordinating multiple workstreams:

1. Workstream analyzer agents (one per workstream) - check health, dependencies, progress
2. Dependency mapper agent - identify cross-workstream dependencies
3. Risk aggregator agent - combine risk signals
4. Synthesis agent - produce coordinated status report

## Key Takeaway

Break large PM tasks into specialized agents. Parallel execution enables 3-6x speedup. Template extraction from initial analysis enables batch processing.
