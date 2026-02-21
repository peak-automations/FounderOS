# CLAUDE.md — FounderOS

This file provides guidance for AI assistants (Claude and others) working on this repository. It describes the project's current state, intended conventions, and development workflows.

---

## Project Overview

**FounderOS** is a project owned by [peak-automations](mailto:info@peakautomations.co.uk).

**Current state**: Early inception. The repository has been initialized with a minimal README and no source code yet. This file will be updated as the project evolves.

---

## Repository Structure

```
FounderOS/
├── CLAUDE.md         # This file — guidance for AI assistants
└── README.md         # Project introduction (stub)
```

As the project grows, this section should be updated to reflect the actual directory tree and the purpose of each major directory.

---

## Git Workflow

### Branch Naming

- Feature branches: `feature/<short-description>`
- Bug fixes: `fix/<short-description>`
- Claude/AI-generated branches: `claude/<task-id>`
- Main integration branch: `master`

### Commit Messages

Use clear, imperative commit messages:

```
Add user authentication module
Fix race condition in job scheduler
Refactor database connection pooling
```

- Present tense, imperative mood ("Add", not "Added" or "Adds")
- First line ≤ 72 characters
- Body (if needed) separated by a blank line, explaining *why* not *what*

### Push Convention

Always push with tracking set:

```bash
git push -u origin <branch-name>
```

Branch names that start with `claude/` must match the session ID suffix exactly, or the push will be rejected with HTTP 403.

---

## Development Setup

> This section will be populated once a tech stack is chosen and scaffolded.

### Prerequisites

_To be defined._

### Installation

```bash
# Clone the repository
git clone <repo-url>
cd FounderOS

# Install dependencies (once package manager is chosen)
# e.g., npm install / pip install -r requirements.txt / cargo build
```

### Environment Variables

No environment variables are currently required. As they are added, document them in a `.env.example` file and list them here with descriptions.

---

## Build & Run

> To be defined once a build system is in place.

Typical commands to document here:

| Command | Purpose |
|---------|---------|
| `npm run dev` | Start development server |
| `npm run build` | Produce production build |
| `npm test` | Run test suite |
| `npm run lint` | Run linter |

---

## Testing

> No test framework is configured yet.

When tests are added:
- Run the full suite before committing
- Do not commit with failing tests
- Document test commands in this section and in `package.json` (or equivalent)

---

## Code Conventions

These conventions apply regardless of the final language/framework chosen:

### General

- Prefer clarity over cleverness
- Keep functions small and single-purpose
- Avoid over-engineering: build what is needed now, not for hypothetical futures
- Delete unused code rather than commenting it out

### Naming

- Use descriptive names; abbreviations only when universally understood
- File names: `kebab-case` for most languages; follow language idioms otherwise
- Constants: `UPPER_SNAKE_CASE`
- Variables and functions: `camelCase` (JS/TS) or `snake_case` (Python/Rust) per language convention

### Comments

- Comment *why*, not *what* — code should be self-explanatory for the *what*
- Remove stale comments when refactoring

### Security

- Never commit secrets, API keys, or credentials — use environment variables
- Validate all external input at system boundaries
- Do not introduce SQL injection, XSS, command injection, or other OWASP Top 10 vulnerabilities
- Sanitize user-supplied data before use

---

## AI Assistant Guidelines

When Claude or another AI assistant works in this repository:

1. **Read before modifying** — always read relevant files before making changes
2. **Minimal changes** — only change what is required by the task; avoid unsolicited refactoring or cleanup
3. **No speculative features** — do not add extra error handling, logging, or abstractions unless requested
4. **No unnecessary files** — prefer editing existing files over creating new ones; never create documentation files unless asked
5. **Test awareness** — if a test suite exists, run it and ensure it passes before committing
6. **Branch discipline** — develop on the designated branch; never push to `master` without explicit permission
7. **Commit often** — small, coherent commits are better than one large commit
8. **Update this file** — if you add a new tool, framework, or significant convention, update the relevant section of CLAUDE.md

---

## Contact

Project owner: peak-automations — info@peakautomations.co.uk

---

*Last updated: 2026-02-21. This file reflects the repository at inception and should be kept current as the project evolves.*
