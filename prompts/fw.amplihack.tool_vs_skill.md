# Tool vs Skill Classification Guide

## Definitions

### TOOL = Executable Program

- A standalone program, script, or CLI application
- Runs via `python tool.py`, `node tool.js`, or as installed command

### SKILL = AI Capability

- Markdown documentation that teaches an AI how to do something
- Loaded by the AI agent, invoked conversationally

## Classification Rules

When user says:

- **"create a tool"** -> Build EXECUTABLE code
- **"create a CLI"** -> Build EXECUTABLE code
- **"create a program"** -> Build EXECUTABLE code
- **"create a script"** -> Build EXECUTABLE code
- **"create a skill"** -> Build DOCUMENTATION

### The PREFERRED Pattern: Tool + Skill

Most of the time, build BOTH:

1. **First**: Build the TOOL (executable program)
   - Reusable, testable, version-controlled code
   - Can be run standalone
   - Has tests, documentation, proper structure

2. **Then**: Build a SKILL that uses the tool
   - Provides convenient conversational interface
   - Calls the tool programmatically

### When Tool-Only Is Sufficient

- One-off scripts or utilities
- Batch processing programs
- CI/CD integration points

## Critical Warning

Do NOT look at skill directories for code examples when building tools. Skills contain markdown documentation, not code templates.
