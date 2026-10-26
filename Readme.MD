# Enterprise-Automation-Playwright

A Playwright test-automation project in TypeScript, organised with the page-object model. It contains login page objects and specs for navigation and login flows, with Playwright configuration and a GitHub Actions workflow.

## What it contains

- **Tests (`src/tests/`)** — `goto.spec.ts` (navigation) and `login.spec.ts` (login flow).
- **Page objects (`src/pages/`)** — `login.page.ts` and `loginn.page.ts` (note the double “n” in the second filename, as committed).
- **Configuration** — `playwright.config.ts` at the repo root.
- **CI** — a GitHub Actions workflow under `.github/workflows/`.
- **Notes** — `requirements.md` at the repo root.

## Tech stack

- Playwright Test (`@playwright/test`) with TypeScript (`@types/node`)
- CommonJS package layout (`"type": "commonjs"` in `package.json`)

## How to run

```bash
npm install
npx playwright install
npx playwright test
```

Note: `package.json` defines no test script, so tests are run directly with `npx playwright test` (a single spec can be run with `npx playwright test src/tests/login.spec.ts`).

## Project structure

```
playwright.config.ts   # Playwright configuration
package.json           # Dev dependencies: @playwright/test, @types/node
src/
  pages/
    login.page.ts      # Login page object
    loginn.page.ts     # Second login page object (filename as committed)
  tests/
    goto.spec.ts       # Navigation spec
    login.spec.ts      # Login spec
.github/workflows/     # GitHub Actions CI workflow
requirements.md        # Project notes
Readme.MD              # This file (the repo's readme, on the master branch)
```
