# CLAUDE.md - AI Assistant Guidelines

This document provides guidance for AI assistants working with this repository.

## Repository Overview

**Repository:** Test
**Current State:** Newly initialized test repository
**Primary Branch:** main
**Last Updated:** 2025-11-17

### Current Structure

```
/
├── TestFile          # Simple test file
└── CLAUDE.md         # This file - AI assistant guidelines
```

## Project Context

This is a minimal test repository currently in its initial setup phase. The repository is intended for experimentation and testing purposes.

## Development Workflows

### Git Workflow

1. **Branch Naming:**
   - Feature branches: `feature/<description>`
   - Bug fixes: `fix/<description>`
   - AI-assisted work: `claude/<session-id>` (auto-generated)

2. **Commit Guidelines:**
   - Write clear, descriptive commit messages
   - Use present tense ("Add feature" not "Added feature")
   - Keep commits focused and atomic

3. **Push Protocol:**
   - Always use `git push -u origin <branch-name>`
   - Retry failed pushes with exponential backoff (2s, 4s, 8s, 16s)
   - Maximum 4 retry attempts for network failures

## Code Conventions

### General Guidelines

- **No unnecessary file creation** - Prefer editing existing files over creating new ones
- **Security first** - Never introduce vulnerabilities (XSS, SQL injection, command injection, etc.)
- **Clean code** - Follow consistent formatting and naming conventions
- **Documentation** - Comment complex logic, maintain up-to-date docs

### When Adding New Features

1. Plan the implementation using structured task lists
2. Research existing codebase patterns first
3. Follow established conventions in the repository
4. Test changes thoroughly before committing
5. Update documentation as needed

## Testing

Currently no testing framework is configured. When adding tests:

- Place test files alongside source code or in a dedicated `tests/` directory
- Use descriptive test names that explain the expected behavior
- Ensure tests are deterministic and isolated

## Build & Development Commands

No build system is currently configured. As the project grows, document commands here:

```bash
# Example structure for future commands:
# npm install      - Install dependencies
# npm run build    - Build the project
# npm test         - Run tests
# npm run lint     - Check code style
```

## Configuration Files

No configuration files present yet. Common files to add:

- `package.json` - Node.js project configuration
- `.gitignore` - Git ignore patterns
- `tsconfig.json` - TypeScript configuration (if using TS)
- `.editorconfig` - Editor settings consistency

## AI Assistant Best Practices

### Before Making Changes

1. **Understand the context** - Read relevant files and understand the current state
2. **Plan first** - Use task lists to organize multi-step work
3. **Check for patterns** - Follow existing code conventions and patterns
4. **Verify assumptions** - Don't guess about project requirements

### During Development

1. **Incremental progress** - Make small, focused changes
2. **Track tasks** - Update task status as you complete work
3. **Test as you go** - Verify changes work as expected
4. **Document decisions** - Explain non-obvious implementation choices

### After Completing Work

1. **Review changes** - Check git diff before committing
2. **Write clear commits** - Summarize what changed and why
3. **Update docs** - Keep CLAUDE.md and other docs current
4. **Push changes** - Push to the designated branch

## Common Tasks

### Adding a New File

```bash
# 1. Create the file with appropriate content
# 2. Stage the changes: git add <filename>
# 3. Commit: git commit -m "Add <filename> for <purpose>"
# 4. Push: git push -u origin <branch-name>
```

### Modifying Existing Files

1. Read the file first to understand current state
2. Make targeted edits preserving existing structure
3. Verify changes don't break existing functionality
4. Commit with descriptive message

## Security Considerations

- Never commit sensitive data (passwords, API keys, tokens)
- Avoid committing `.env` files or credentials
- Sanitize user inputs in any code
- Follow OWASP security guidelines

## Repository Maintenance

### Keeping CLAUDE.md Updated

This file should be updated when:
- New development patterns are established
- Build/test commands are added
- Project structure changes significantly
- New conventions are adopted

### Version Control

- Keep the repository clean and organized
- Remove unused files and dependencies
- Maintain consistent file structure
- Document architectural decisions

---

## Quick Reference

| Task | Action |
|------|--------|
| Explore codebase | Use Task tool with Explore agent |
| Find files | Use Glob tool with patterns |
| Search content | Use Grep tool |
| Read files | Use Read tool |
| Edit files | Use Edit tool (read first!) |
| Create files | Use Write tool (avoid unless necessary) |
| Run commands | Use Bash tool |
| Track progress | Use TodoWrite tool |

---

*This document is maintained by AI assistants and should be updated as the project evolves.*
