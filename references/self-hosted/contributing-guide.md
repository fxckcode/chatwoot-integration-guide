## Contributing Guide

Thank you for taking an interest in contributing to Chatwoot! This guide will help you get started with contributing to our open-source customer support platform. Before submitting your contribution, please make sure to take a moment and read through the following guidelines.

## Getting Started

Before starting your work, ensure an issue exists for it. If not, feel free to create one. You can also take a look into the issues tagged [Good first issues](https://github.com/chatwoot/chatwoot/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

### Initial Steps

1. **Check for Existing Issues**: Browse the [GitHub issues](https://github.com/chatwoot/chatwoot/issues) to see if someone is already working on what you want to contribute.
2. **Comment on the Issue**: Add a comment on the issue and wait for the issue to be assigned before you start working on it.
	- This helps to avoid multiple people working on similar issues.
3. **Propose Complex Solutions**: If the solution is complex, propose the solution on the issue and wait for one of the core contributors to approve before going into the implementation.
	- This helps in shorter turn around times in merging PRs.
4. **Justify New Features**: For new feature requests, provide a convincing reason to add this feature. Real-life business use-cases will be super helpful.
5. **Join the Community**: Feel free to join our [Discord community](https://discord.com/invite/cJXdrwS) if you need further discussions with the core team.

## Pull Request Guidelines

We use git-flow branching model. The base branch is `develop`. Please raise your PRs against the `develop` branch.

### Before Submitting

- Please make sure that you have read the [issue triage guidelines](https://www.chatwoot.com/hc/handbook/articles/issue-triage-29) before you make a contribution.
- It’s okay and encouraged to have multiple small commits as you work on the PR - we will squash the commits before merging.
- For other guidelines, see [PR Guidelines](https://www.chatwoot.com/hc/handbook/articles/pull-request-guidelines-32)
- Ensure that all the text copies that you add into the product are i18n translatable. You are only required to add the `English` version of the strings. We pull in other language translations from our contributors on crowdin. See [Translation guidelines](https://developers.chatwoot.com/contributing-guide/translation-guidelines) to learn more.

## Development Workflow

### Developing a New Feature

```shellscript
# Create a branch in the following format:
feature/<issue-id>-<issue-name>

# Example:
feature/235-contact-panel
```

**Requirements:**

- Add accompanying test cases
- Follow our coding standards
- Include proper documentation

### Bug Fixes or Chores

```shellscript
# Branch naming for bug fixes:
fix/<issue-id>-<issue-name>

# Branch naming for chores:
chore/<description>
```

**Requirements:**

- If you are resolving a particular issue, add `fix: Fixes xxxx` (#xxxx is the issue) in your PR title
- Provide a detailed description of the bug in the PR
- Add appropriate test coverage if applicable

## Environment Setup

Choose the guide that matches your operating system:

## macOS Setup

Complete setup guide for macOS developers

## Ubuntu Setup

Step-by-step Ubuntu installation guide

## Windows Setup

Windows 10/11 development environment setup

## Docker Setup

Quick setup using Docker containers

### Speed Up Development

Use our [Make commands](https://developers.chatwoot.com/contributing-guide/environment-setup/make) to speed up your local development workflow.

## Project Setup

Once you have set up the environment, follow these guides to get Chatwoot running locally:

1. **[Quick Setup Guide](https://developers.chatwoot.com/contributing-guide/setup-guide)** - Step-by-step setup instructions
2. **[Environment Variables](https://developers.chatwoot.com/contributing-guide/environment-variables)** - Configuration options
3. **[Common Errors](https://developers.chatwoot.com/contributing-guide/common-errors)** - Troubleshooting guide

### Special App Integrations

If you’re working on specific integrations:

- **[Telegram App Setup](https://developers.chatwoot.com/contributing-guide/telegram-channel-setup)**
- **[Line App Setup](https://developers.chatwoot.com/contributing-guide/line-channel-setup)**
- **[Mobile App Development](https://developers.chatwoot.com/contributing-guide/mobile-app)**

## Testing Your Contributions

We use comprehensive testing to ensure code quality:

### Test Types

- **Unit Tests**: Test individual components and functions
- **Integration Tests**: Test component interactions
- **End-to-End Tests**: Test complete user workflows with [Cypress](https://developers.chatwoot.com/contributing-guide/tests/cypress)

### Running Tests

```shellscript
# Run all tests
bundle exec rspec

# Run specific test file
bundle exec rspec spec/models/user_spec.rb

# Run Cypress tests
npm run cypress:open
```

## Documentation and Translation

### Documentation Guidelines

- Keep documentation clear and concise
- Include code examples where helpful
- Update documentation when changing functionality
- Follow our [translation guidelines](https://developers.chatwoot.com/contributing-guide/translation-guidelines)

### Internationalization

- All user-facing text must be translatable
- Only add English strings - other languages are handled via [Crowdin](https://translate.chatwoot.com/)
- Use proper i18n keys and formatting

## Community Guidelines

We strive to maintain a welcoming and inclusive community:

- **[Code of Conduct](https://developers.chatwoot.com/contributing-guide/code-of-conduct)** - Our community standards
- **[Community Guidelines](https://developers.chatwoot.com/contributing-guide/community-guidelines)** - How we interact
- **[Security Reports](https://developers.chatwoot.com/contributing-guide/security-reports)** - Reporting security issues

## API Development

If you’re working on API-related features:

- **[Chatwoot APIs](https://developers.chatwoot.com/contributing-guide/chatwoot-apis)** - API development guide
- **[API Documentation](https://developers.chatwoot.com/contributing-guide/api-documentation)** - Documenting APIs
- **[Platform APIs](https://developers.chatwoot.com/contributing-guide/chatwoot-platform-apis)** - Platform-level APIs

## Recognition

We value all contributions to Chatwoot. Check out our [Contributors page](https://developers.chatwoot.com/contributing-guide/contributors) to see the amazing people who have helped make Chatwoot better.

## Getting Help

Need assistance? Here are your options:

- **GitHub Issues**: For bug reports and feature requests
- **Discord Community**: For real-time discussions with the core team
- **Documentation**: Comprehensive guides and API references
- **Community Forums**: Connect with other contributors

---

Ready to start contributing? Pick an issue that interests you and follow our guidelines above. Every contribution, no matter how small, helps make Chatwoot better for everyone! 🚀[macOS SetupComplete guide to setting up your macOS development environment for Chatwoot contribution.](https://developers.chatwoot.com/contributing-guide/environment-setup/mac-os)

[Next](https://developers.chatwoot.com/contributing-guide/environment-setup/mac-os)