# CLAUDE.md — Infinite Knowledge

This file provides guidance for AI assistants (Claude Code and others) working in this repository.

## Project Overview

**Repository:** `infinite-knowledge`
**Status:** Initial setup — this repository is currently empty and awaiting its first implementation.

Update this section as the project evolves to describe what the system does, its purpose, and its intended audience.

---

## Repository Structure

As the project is bootstrapped, update this section to reflect the actual layout. A typical structure to aim for:

```
infinite-knowledge/
├── CLAUDE.md              # This file — AI assistant guidance
├── README.md              # Human-facing project overview
├── .gitignore
├── src/                   # Application source code
│   ├── ...
├── tests/                 # Test suite
│   ├── ...
├── docs/                  # Extended documentation
│   ├── ...
└── scripts/               # Developer utility scripts
    └── ...
```

---

## Development Workflow

### Branch Strategy

- Main/default branch: `main`
- Feature branches: `feature/<short-description>`
- Bug fix branches: `fix/<short-description>`
- AI-driven branches: `claude/<description>-<session-id>`

### Getting Started

```bash
# Clone the repository
git clone <repo-url>
cd infinite-knowledge

# Install dependencies (update this command once the tech stack is chosen)
# e.g. npm install | pip install -r requirements.txt | go mod download

# Run tests
# e.g. npm test | pytest | go test ./...

# Start development server (if applicable)
# e.g. npm run dev | python main.py | go run .
```

### Making Changes

1. Create a branch from `main`
2. Make focused, atomic commits
3. Ensure all tests pass before opening a PR
4. Keep PRs small and reviewable

---

## Commit Message Conventions

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<optional scope>): <short summary>

[optional body]
```

**Types:**
- `feat` — new feature
- `fix` — bug fix
- `docs` — documentation changes
- `refactor` — code restructuring without behavior change
- `test` — adding or updating tests
- `chore` — tooling, dependencies, CI changes

**Examples:**
```
feat(api): add knowledge retrieval endpoint
fix(search): handle empty query strings
docs: update CLAUDE.md with project structure
```

---

## Code Conventions

> Update this section once the tech stack and language(s) are decided.

### General

- Prefer readability over cleverness
- Write self-documenting code; add comments only where logic is non-obvious
- Keep functions small and focused on a single responsibility
- Avoid global mutable state
- Delete unused code rather than commenting it out

### Testing

- All new features must be accompanied by tests
- Tests should be co-located with source (or in `tests/` mirroring `src/` structure)
- Aim for fast, deterministic unit tests; integration tests where boundaries matter
- Test behavior, not implementation details

### Error Handling

- Fail fast and loudly during development
- Return meaningful error messages at system boundaries (user input, external APIs)
- Do not swallow errors silently

---

## AI Assistant Guidelines

When working in this repository, AI assistants should:

### Do

- Read existing files before modifying them
- Make the minimum change required to accomplish the task
- Follow the commit and branch conventions above
- Write tests for new functionality
- Update this `CLAUDE.md` when significant architectural decisions are made
- Ask for clarification rather than guessing at ambiguous requirements

### Do Not

- Push directly to `main`
- Add unnecessary abstraction layers or premature generalization
- Add dependencies without clear justification
- Leave TODO comments without associated issues
- Introduce secrets, credentials, or API keys into source files
- Create new files when editing an existing one suffices

### When in Doubt

- Check git history for context on past decisions
- Read adjacent code for style and pattern guidance
- Prefer the simpler of two equivalent solutions

---

## Environment & Configuration

Document required environment variables here as they are introduced:

```
# Example — replace with actual variables
# APP_ENV=development
# DATABASE_URL=...
# API_KEY=...
```

Use a `.env.example` file (never `.env` itself) to document required variables without committing secrets.

---

## CI/CD

> Describe the CI pipeline here once configured (GitHub Actions, CircleCI, etc.)

Expected checks before merging:
- All tests pass
- Linter / formatter clean
- Build succeeds (if applicable)

---

## Contacts & Resources

- **Repo owner:** sureshram
- **Issues:** Use the GitHub Issues tracker for bugs and feature requests
- **Discussions:** Use GitHub Discussions for design questions and broader conversations
