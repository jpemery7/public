# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working with this repository.

---

## Repository Overview

This is a new, empty Git repository. As the project grows, this file should be updated to reflect the actual codebase structure, conventions, and workflows. The sections below establish baseline expectations and should be expanded with project-specific details.

- **Remote**: `jpemery7/public`
- **Default working branch pattern**: `claude/claude-md-*`
- **Git signing**: SSH-based commit signing is enabled

---

## Development Workflow

### Branching Strategy

- All Claude-driven development uses branches prefixed with `claude/`
- Branch names follow the pattern: `claude/<task-slug>-<session-id>`
- Never push directly to `main` or `master` without explicit permission
- Always push with tracking: `git push -u origin <branch-name>`

### Committing

- Write clear, descriptive commit messages that explain *why*, not just *what*
- Keep commits focused — one logical change per commit
- Do not amend published commits; create new commits instead
- Do not skip hooks (`--no-verify`) unless explicitly instructed

### Making Changes

1. Read and understand existing code before modifying it
2. Edit existing files rather than creating new ones where possible
3. Keep changes minimal and focused on the task
4. Avoid speculative changes, refactoring, or "improvements" beyond what is asked

---

## Code Conventions

*(Update this section once a language/framework is chosen.)*

### General

- Prefer simplicity over cleverness
- No dead code — remove unused variables, imports, and functions
- Validate at system boundaries (user input, external APIs), not internally
- No backwards-compatibility shims for code that has no dependents

### File Organization

- Group related files in clearly named directories
- Keep configuration files at the project root
- Source files belong under a `src/` or equivalent directory

---

## Testing

*(Update with actual test commands once a framework is set up.)*

- Run all tests before committing
- New features should include corresponding tests
- Bug fixes should include a regression test

---

## Environment & Configuration

- Never commit secrets, API keys, or credentials
- Use `.env` files for local secrets; add `.env` to `.gitignore`
- Provide a `.env.example` with placeholder values for all required variables

---

## AI Assistant Guidelines

### Do

- Read files before modifying them
- Use parallel tool calls for independent operations
- Break complex tasks into tracked steps (TodoWrite)
- Ask before taking destructive or irreversible actions
- Commit and push work when a task is complete

### Do Not

- Guess URLs or generate external links unless confident they are correct
- Add unnecessary comments, docstrings, or type annotations to unchanged code
- Create files unless absolutely necessary
- Use `--force`, `--no-verify`, or other safety-bypassing flags without explicit instruction
- Push to a branch other than the one designated for the current task

---

## Updating This File

When the project gains a concrete technology stack, update the relevant sections:

- [ ] Add language/framework to **Repository Overview**
- [ ] Add build commands to **Development Workflow**
- [ ] Fill in **Code Conventions** for the chosen stack
- [ ] Add test run commands to **Testing**
- [ ] Document required environment variables in **Environment & Configuration**
- [ ] Add any CI/CD pipeline notes
