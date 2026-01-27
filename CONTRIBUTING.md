# Contributing to Eventra

Thank you for your interest in contributing to Eventra! This document provides guidelines for contributing to this project.

## Commit Message Convention

This project follows the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. This leads to more readable messages that are easy to follow when looking through the project history and enables automatic version management and changelog generation.

### Commit Message Format

Each commit message consists of a **header**, a **body**, and a **footer**. The header has a special format that includes a **type**, an optional **scope**, and a **subject**:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

The **header** is mandatory and must conform to the format specified above.

The **body** and **footer** are optional but recommended for non-trivial changes.

### Type

The type must be one of the following:

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing tests or correcting existing tests
- **build**: Changes that affect the build system or external dependencies
- **ci**: Changes to our CI configuration files and scripts
- **chore**: Other changes that don't modify src or test files
- **revert**: Reverts a previous commit

### Scope

The scope is optional and can be anything specifying the place of the commit change. For example:

- `auth`
- `api`
- `ui`
- `database`
- `config`

### Subject

The subject contains a succinct description of the change:

- Use the imperative, present tense: "change" not "changed" nor "changes"
- Don't capitalize the first letter
- No dot (.) at the end
- Limit to 50 characters or less

### Body

The body should include the motivation for the change and contrast this with previous behavior. It should be wrapped at 72 characters.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to reference GitHub issues that this commit closes.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

### Examples

#### Simple commit message
```
feat: add user authentication
```

#### Commit message with scope
```
feat(auth): implement JWT token validation
```

#### Commit message with body
```
fix: prevent race condition in event creation

Add mutex lock to ensure thread-safe event creation
and avoid duplicate event IDs.
```

#### Commit message with breaking change
```
feat(api)!: update API response format

BREAKING CHANGE: The API now returns events in a nested structure.
Previous flat structure is no longer supported. Update your client
code to handle the new format.
```

#### Commit message with multiple footers
```
fix: correct calculation in event duration

The event duration was incorrectly calculated when crossing
midnight boundaries. This fix properly handles timezone
conversions and day changes.

Fixes #123
Reviewed-by: Jane Doe
```

#### Revert commit
```
revert: feat(api): add experimental feature

This reverts commit 1234567890abcdef.
```

## Contribution Workflow

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following the guidelines above
3. **Test your changes** to ensure they work as expected
4. **Commit your changes** using conventional commit messages
5. **Push to your fork** and submit a pull request
6. **Wait for review** - maintainers will review your pull request

## Pull Request Guidelines

- Use a clear and descriptive title following conventional commit format
- Fill in the pull request template with all relevant information
- Link any related issues in the pull request description
- Ensure all tests pass before submitting
- Keep pull requests focused on a single concern
- Update documentation if you're changing functionality

## Questions?

If you have any questions or need help, feel free to open an issue or reach out to the maintainers.

Thank you for contributing to Eventra! 🎉
