# Expert Panel Review Pattern

Multiple expert agents independently review a solution, each casting a vote with detailed rationale. Votes are aggregated for a final decision.

## When to Use

- Multiple expert judgments needed for diverse evaluation
- Quantifiable decisions with clear vote-based outcomes
- Protection against individual expert bias
- Code review approvals and merge decisions
- Design review boards with multi-stakeholder approval
- Critical quality gates requiring consensus

## How It Works

1. **Parallel Expert Reviews**: Multiple domain experts independently analyze the solution
2. **Individual Voting**: Each expert casts APPROVE/REJECT/ABSTAIN with confidence level
3. **Aggregated Decision**: Votes combined using configurable method
4. **Dissent Reporting**: Minority opinions preserved for transparency

## Default Experts

- **Security**: Vulnerabilities, attack vectors, security best practices
- **Performance**: Speed, scalability, resource efficiency
- **Simplicity**: Minimal complexity, maintainability, clarity

## Aggregation Methods

- **Simple Majority**: Count votes, majority wins (default)
- **Weighted by Confidence**: High-confidence votes carry more weight
- **Unanimous**: All experts must agree (for security-critical code)

## Common Patterns

### Code Review Gate

Use expert panel to gate PR merges. Require simple majority for standard code, unanimous for security-critical changes.

### Security Audit

Define security-specific experts (authentication, authorization, cryptography, input validation) with unanimous requirement.

### Design Review Board

Multi-stakeholder experts (architecture, security, operations, product, compliance) with weighted voting.

## Comparison with Other Patterns

- **vs N-Version**: N-Version creates diversity in SOLUTIONS, Expert Panel creates diversity in EVALUATION
- **vs Debate**: Debate is interactive discussion, Expert Panel is independent review with mechanical aggregation
- **Use Together**: N-Version generates alternatives, Expert Panel selects best
