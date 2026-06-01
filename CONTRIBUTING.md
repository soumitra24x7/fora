# Contributing to Fora

Thanks for your interest in contributing to Fora! This guide covers everything you need to get started.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18+
- [Wrangler CLI](https://developers.cloudflare.com/workers/wrangler/) (`npm install -g wrangler`)
- A Cloudflare account (free tier works for development)

### Project Structure

```
fora/
├── adapters/            # Framework-specific integrations
│   ├── astro-fora/      # Astro adapter
│   ├── jekyll-fora/     # Jekyll adapter
│   ├── emdash-fora/     # EmDash CMS adapter
│   ├── fora-cli/        # `npx create-fora` CLI
│   └── ...
```

## How to Contribute

### Reporting Bugs

Open an issue with:
- Clear title and description
- Steps to reproduce
- Expected vs actual behavior
- Browser/OS info if relevant

### Suggesting Features

Open an issue with the `enhancement` label. Describe:
- The problem you're solving
- Your proposed solution
- Alternatives considered

### Submitting Changes

1. Fork the repo
2. Create a branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Commit with clear messages: `feat: add thread pagination` or `fix: resolve session leak`
5. Push and open a Pull Request

### Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` — new feature
- `fix:` — bug fix
- `docs:` — documentation only
- `perf:` — performance improvement
- `refactor:` — code change that neither fixes a bug nor adds a feature
- `test:` — adding or updating tests
- `chore:` — maintenance tasks

## Adapter Development

Want to build a Fora adapter for a new framework? See [`adapters/README.md`](adapters/README.md) for the adapter API contract.

Each adapter is a standalone npm package. The pattern:
1. Generate the embed snippet with site key
2. Provide framework-specific integration (component, plugin, shortcode)
3. Handle configuration (theme, features, custom CSS variables)

## License

[MIT](LICENSE)
