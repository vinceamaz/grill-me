# grill-me

Claude Code plugin that stress-tests a plan or design through relentless, one-at-a-time questioning.

## What it does

- Walks down each branch of the design tree
- Resolves dependencies between decisions one-by-one
- Provides a recommended answer with each question
- Explores the codebase when that answers the question faster than asking you

## Install

### From a local checkout

```bash
/plugin marketplace add /path/to/grill-me
/plugin install grill-me@grill-me
```

### From GitHub (after publishing)

```bash
/plugin marketplace add vinceamaz/grill-me
/plugin install grill-me@grill-me
```

### Dev / test locally

```bash
claude --plugin-dir /path/to/grill-me
```

Then invoke:

```text
/grill-me
```

## Usage

Start a grilling session when you have a plan or design to stress-test:

```text
/grill-me

I want to add a caching layer to our API. Grill me on the design.
```

Or use trigger phrases like "grill me on this plan" — the skill description includes those triggers for model invocation.

## Structure

```
grill-me/
├── .claude-plugin/
│   ├── plugin.json       # Plugin manifest
│   └── marketplace.json  # Marketplace registry (for distribution)
├── SKILL.md              # Skill instructions
└── README.md
```

## Related

- [grill-with-docs](https://github.com/vinceamaz/grill-with-docs) — same grilling flow, plus CONTEXT.md glossary and ADR updates inline

## License

MIT
