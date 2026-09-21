# Contributing to MuviDate

Thank you for contributing to MuviDate.

## Development workflow

1. Fork the repository and create a focused branch.
2. Install dependencies with `npm install` or `bun install`.
3. Configure local variables from `.env.example`.
4. Run the app with `npm run dev`.
5. Before submitting a pull request, run:
   - `npm run lint`
   - `npm run build`

## Pull requests

Please include:

- What changed and why
- Screenshots or a recording for UI changes
- Testing performed
- Any Firebase, configuration or security-rule impact

Keep pull requests focused and avoid unrelated refactors.

## Commit messages

Use clear action-oriented messages, for example:

- `feat: add participant limit`
- `fix: recover playback after reconnect`
- `docs: improve firebase setup`
- `refactor: simplify movie filtering`

## Code style

Prefer TypeScript types over `any` where practical, reusable components, existing project conventions, accessible controls and defensive handling of Firebase/network failures.

## Security

Never commit secrets, tokens, credentials, private user data or production database exports.
