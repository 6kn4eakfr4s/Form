# Personal-Harness

This is my personal Harness. It's currently in development.

## Development

Use the Node.js version in `.nvmrc` and the npm version declared in
`package.json#packageManager`.

```sh
npm ci
npm run typecheck
npm run check
npm test
npm run build
```

TypeScript source lives in `src/` and compiles to `dist/`. Biome handles linting
and formatting; use `npm run format` to format code.

Tests use Vitest, with `*.test.ts` files alongside source files.
`npm run test:watch` enables watch mode.

## Continuous integration

GitHub Actions runs type checks, Biome checks, tests, and the build on pull
requests targeting `main` and pushes to `main`, using the project's configured
Node.js and npm versions.
