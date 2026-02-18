# Contributing to DBA Bridge

Thank you for your interest in contributing. DBA Bridge is in early development and every contribution — even just a migration horror story — makes the tool better.

---

## The Most Valuable Contributions Right Now

We are not yet at the stage where code PRs are the most useful thing. The product is more valuable if we get these first:

### 1. Share What Broke in Your Migration

Open an issue using the **Migration Bug Report** template.  
Tell us:
- What source and target database you were migrating between
- What broke after migration (stored procedures? data types? constraints? queries?)
- What tool you were using when it broke

This is the raw material the audit engine is built from. Every real edge case we learn about before shipping means one fewer user who hits a silent failure.

### 2. Share an Anonymised Schema Dump

If you have done an Oracle → Postgres or SQL Server → Supabase migration, we would love to test the audit engine against a real schema.

- Replace all real table names, column names, and data with fictional equivalents
- Remove any proprietary stored procedure logic — even the structure (number of procedures, types of statements used) is useful
- Open an issue with the **Schema Dump Contribution** template or email us at info@ai2innovate.io

Even a 10-table schema with 2–3 stored procedures is useful.

### 3. Report Problems You Hit With Existing Tools

We track common failure patterns across AWS DMS, Azure Migrate, ora2pg, and pgloader.  
If you have a specific documented failure from one of these tools, open an issue describing it.  
This helps us build test cases for the validation engine.

---

## Code Contributions

The codebase is not yet public. We are building in private until Phase 1 is complete.

When the repo goes public:

### What we will accept
- Bug fixes with a clear reproduction case
- New data type mappings with test coverage
- Connector improvements for supported databases
- Documentation improvements
- Translation / localisation

### What we will not accept without prior discussion
- New database connectors (wait for the connector SDK in Phase 3)
- UI changes without an agreed design direction
- New features not on the roadmap

**Before opening a large PR:** open an issue first and describe what you want to build. This avoids wasted effort if it doesn't fit the current phase.

---

## Opening Issues

Use the provided issue templates:

- **Migration Bug Report** — something broke during or after a migration
- **Schema Dump Contribution** — you have a schema you're willing to share for testing
- **Feature Request** — something you want that isn't on the roadmap

For general questions and discussion, use the [Discord server](https://discord.gg/K64U65je7h) rather than GitHub issues.

---

## Code Style (for when the repo is open)

- Python: follow [PEP 8](https://pep8.org), use `ruff` for linting
- TypeScript / React: follow the existing ESLint config
- Rust (Tauri): follow `rustfmt` defaults
- All new functions need a docstring
- All new features need at least one unit test
- Do not add comments that explain what the code does — only explain *why* if it's not obvious

---

## Commit Message Format

```
type: short description (under 72 chars)

Longer explanation if needed. What changed, why it changed.
Reference any related issue: closes #123
```

Types: `feat` · `fix` · `docs` · `test` · `refactor` · `chore`

---

## Licence

By contributing to DBA Bridge, you agree that your contributions will be licensed under the [Apache 2.0 License](./LICENSE).

---

*Questions? Join the [Discord](https://discord.gg/K64U65je7h) or email info@ai2innovate.io*
