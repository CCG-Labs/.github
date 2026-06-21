# Contributing to CCG Labs

CCG Labs repositories are primarily maintained by **Brian Reich**. External contributions are welcome on the Golden Template (`one-day-website`) and tooling repos.

## Before You Start

- Open an issue or discussion to describe what you want to change before writing code — this avoids wasted effort.
- For client site repos (`pyle-stone`, etc.), contributions are only accepted from CCG Labs staff and the client.

## Development Setup

Each repo has its own README with setup instructions. In general:

```bash
git clone <repo>
cd <repo>
npm install
npm run dev
```

## Pull Request Guidelines

- Branch from `main`, name your branch `feat/short-description` or `fix/short-description`.
- Keep PRs focused — one concern per PR.
- All CI checks must pass before review.
- The Golden Template requires `npm test` to pass (Vitest).

## Code Style

- TypeScript everywhere. No `any` without a comment explaining why.
- No unnecessary comments — code should be self-explanatory.
- Prefer simple, direct solutions over clever ones.
- Astro components use `.astro`; logic goes in `.ts`.

## Commit Messages

Use the [Conventional Commits](https://www.conventionalcommits.org/) format:

```
feat(component): add dark mode toggle
fix(contact): correct honeypot field name
docs(readme): update deployment instructions
```

## Questions?

Open a GitHub Discussion or email brian@ccglabs.net.
