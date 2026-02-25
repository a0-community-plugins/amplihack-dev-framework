# Amplihack Development Patterns

Proven patterns and solutions for clean design and robust development.

## Core Architecture Patterns

### Pattern: Bricks and Studs Module Design

Design modules as self-contained "bricks" with clear "studs" (public API) defined via `__all__`.

```python
"""Module with clear public API.

Public API (the "studs"):
    MainClass: Primary functionality
    helper_function: Utility function
"""

__all__ = ["MainClass", "helper_function"]
```

Module Structure:

```
module_name/
+-- __init__.py     # Public interface via __all__
+-- README.md       # Contract specification
+-- core.py         # Implementation
+-- tests/          # Test the contract
+-- examples/       # Working examples
```

### Pattern: Zero-BS Implementation

Every function must work or not exist. No stubs, no TODOs, no placeholders.

```python
# BAD - Stub
def process_payment(amount):
    raise NotImplementedError("Coming soon")

# GOOD - Working implementation
def process_payment(amount, payments_file="payments.json"):
    payment = {
        "amount": amount,
        "timestamp": datetime.now().isoformat(),
        "id": str(uuid.uuid4())
    }
    # ... actual working code ...
    return payment
```

## API and Integration Patterns

### Pattern: API Validation Before Implementation

Validate APIs before implementation using official documentation. 5-10 min validation prevents 20-30 min debug cycles.

### Pattern: Safe Subprocess Wrapper

Create subprocess wrappers with user-friendly, actionable error messages. Standard exit codes (127 for command not found), context parameter, no exceptions propagate.

### Pattern: Fail-Fast Prerequisite Checking

Check all prerequisites at startup with clear, actionable error messages. Check all at once to show all issues.

## Testing Patterns

### Pattern: Behavior Testing at Module Boundaries

Test the contract (studs), not implementation details. Focus on module boundaries.

### Pattern: Testing Proportionality

Match test coverage to criticality:

- Config changes: verification only
- Simple functions: basic coverage
- Business logic: comprehensive
- Critical paths: exhaustive

Red flag: test code > 10x implementation code for non-critical paths.

## Error Handling Patterns

### Pattern: Transparent Error Handling

- Handle common errors robustly
- Log detailed information for debugging
- Provide clear error messages to users
- Fail fast and visibly during development
- No swallowed exceptions

## Pattern Curation

Patterns are kept when they solve recurring problems (used 3+ times), apply broadly, represent non-obvious solutions, and prevent costly errors. Patterns are removed when they become project-specific or have not been referenced in 6+ months.
