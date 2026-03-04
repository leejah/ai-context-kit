# Contributing to ai-context-kit

Thanks for considering a contribution. Here's how to get involved.

## What's Welcome

- **New lint rules** - Got a pattern that wastes tokens or confuses agents? Add a detector in `src/lint.ts`
- **Format support** - New IDE or tool with its own context file format? Add detection in `src/parse.ts` and a format entry in `src/types.ts`
- **Bug fixes** - Found something broken? Fix it
- **Better tests** - Edge cases, real-world rule files, regression tests

## Setup

```bash
git clone https://github.com/ofershap/ai-context-kit.git
cd ai-context-kit
npm install
npm test
```

## Development

```bash
npm run build          # build with tsup
npm test               # run vitest
npm run typecheck      # tsc --noEmit
npm run lint           # eslint + prettier
```

All code is TypeScript (strict mode). Zero runtime dependencies - keep it that way.

## Adding a Lint Rule

1. Add the detection logic in `src/lint.ts`
2. Add a test case in `tests/lint.test.ts`
3. Update the lint rule table in `README.md`

## Pull Requests

- Keep changes focused. One feature or fix per PR
- Tests must pass (`npm test`)
- Type checking must pass (`npm run typecheck`)
- Describe what the PR does and why

## License

By contributing, you agree that your contributions will be licensed under MIT.
