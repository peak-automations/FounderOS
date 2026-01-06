# CLAUDE.MD - AI Assistant Guidelines for FounderOS

## Project Overview

FounderOS is a project management and operational system designed for founders and startups.

## Project Structure

```
FounderOS/
├── README.md           # Project documentation
└── CLAUDE.MD          # This file - AI assistant guidelines
```

## Development Guidelines

### General Principles

- Follow established patterns in the codebase
- Prioritize code clarity and maintainability over cleverness
- Keep functions small and focused on a single responsibility
- Write self-documenting code with clear variable and function names

### Code Style

- Use consistent indentation (spaces vs tabs should match existing files)
- Follow naming conventions established in the codebase
- Add comments only when the code's intent is not self-evident
- Avoid over-engineering - implement what's needed, not what might be needed

### Git Workflow

- Write clear, descriptive commit messages
- Keep commits focused on a single logical change
- Branch naming: use `claude/` prefix followed by descriptive name and session ID
- Always push to the designated branch

### Security Considerations

- Never commit secrets, API keys, or credentials
- Validate user input at system boundaries
- Be aware of common vulnerabilities (XSS, SQL injection, command injection, etc.)
- Use secure defaults for configurations

### Testing

- Write tests for new functionality
- Ensure existing tests pass before committing
- Focus on testing behavior, not implementation details

### Documentation

- Keep README.md up to date with setup and usage instructions
- Document complex business logic or non-obvious decisions
- Update this CLAUDE.MD file as project patterns emerge

## Working with Claude

### Preferred Approach

1. Read existing code before making changes
2. Use TodoWrite to plan multi-step tasks
3. Make incremental, testable changes
4. Commit and push when changes are complete

### File Operations

- Always read files before editing them
- Prefer editing existing files over creating new ones
- Use specialized tools (Read, Edit, Write) instead of bash commands

### Communication

- Be concise and technical
- Focus on facts over validation
- Provide direct, objective guidance

## Project-Specific Notes

### Current State

This is a new project in early development stages. As the project grows:

- Update this file with specific architectural decisions
- Document any framework or library choices
- Add sections for domain-specific knowledge
- Include common troubleshooting steps

### Future Considerations

- Define technology stack once chosen
- Establish testing framework and coverage requirements
- Set up CI/CD pipeline guidelines
- Document deployment procedures

## Contact & Resources

- Repository: peak-automations/FounderOS
- Main branch: (to be established)
- Development branches: Use `claude/` prefix

---

**Last Updated:** 2026-01-06
**Version:** 1.0.0
