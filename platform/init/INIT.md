# INIT report

- Generated: 2026-11-27 00:11 UTC
- Run: `65b47dbe58c1`
- Repository: https://github.com/shira-ozana/angular-realworld-example-app
- Base commit: `2c8c837809b5877b0f3759a57a454ac52c4b207e` (ref `main`) · branch `shipAI`

## Start here

Requirements and Architect start with these files:

- [AGENTS.md](../../AGENTS.md): Primary entry for Requirements and Architect: product summary, component index, verification commands (bun run test, test:e2e, build, format:check), links to ARCHITECTURE.md, RULES.md, TESTING.md, realworld/AGENTS.md, src/AGENTS.md, and existing realworld/skills without duplicating CLAUDE.md or README.
- [ARCHITECTURE.md](../../ARCHITECTURE.md): System map: Angular Conduit SPA under src/, conformance subtree realworld/, REST JWT API contract, data flow from UI through interceptors to API_BASE, E2E at localhost:4200 extending realworld/specs/e2e/playwright.base.ts; cite paths and label gaps.
- [RULES.md](../../RULES.md): Binding constraints for agents: harness-only edits, no secrets, match existing Angular and TypeScript conventions, preserve human-authored guidance.

> This repository is an Angular single-page application that implements the Conduit (RealWorld) social blogging product: JWT auth, articles, comments, profiles, feeds, and favorites against a REST API. TypeScript sources live under src/ with feature folders under src/app; Bun is the package manager. Shared conformance assets in realworld/ supply OpenAPI, Playwright E2E under realworld/specs/e2e, and API test runners. Unit tests use Vitest on src/**/*.spec.ts; the root Playwright config extends realworld/specs/e2e/playwright.base.ts and serves the app at http://localhost:4200.

## Scan scope

- Files scanned: 175 · components: 13 · analyzed: 13
- Include: all · exclude: none
- Files not sent to the model (context budget): 21
- Files sent truncated: 10

## Harness map

| File | Scope | Purpose | Result |
|---|---|---|---|
| [AGENTS.md](../../AGENTS.md) | Repository root | Primary entry for Requirements and Architect: product summary, component index, verification commands (bun run test, test:e2e, build, format:check), links to ARCHITECTURE.md, RULES.md, TESTING.md, realworld/AGENTS.md, src/AGENTS.md, and existing realworld/skills without duplicating CLAUDE.md or README. | updated (replaced the generated block; human content kept) |
| [ARCHITECTURE.md](../../ARCHITECTURE.md) | Repository root | System map: Angular Conduit SPA under src/, conformance subtree realworld/, REST JWT API contract, data flow from UI through interceptors to API_BASE, E2E at localhost:4200 extending realworld/specs/e2e/playwright.base.ts; cite paths and label gaps. | updated (replaced the generated block; human content kept) |
| [RULES.md](../../RULES.md) | Repository root | Binding constraints for agents: harness-only edits, no secrets, match existing Angular and TypeScript conventions, preserve human-authored guidance. | kept |
| [GUIDELINES.md](../../GUIDELINES.md) | Repository root | Document multiple valid patterns: Vitest unit vs Playwright E2E, BROWSER_API/EXTERNAL_API/TEST_MODE from realworld/specs/e2e/helpers/config.ts, when to use realworld skills vs src feature work; link CONTRACTS.md and SELECTORS.md. | updated (replaced the generated block; human content kept) |
| [CONTRACTS.md](../../CONTRACTS.md) | Repository root | External interfaces: OpenAPI at realworld/specs/api/openapi.yml, E2E UI contract realworld/specs/e2e/SELECTORS.md, Token auth header, demo API_BASE https://api.realworld.show/api. | updated (replaced the generated block; human content kept) |
| [DOMAIN.md](../../DOMAIN.md) | Repository root | Conduit/RealWorld vocabulary: articles, slugs, favorites, feeds, profiles, jwtToken, conforming frontend behaviors referenced by specs. | updated (replaced the generated block; human content kept) |
| [TESTING.md](../../TESTING.md) | Repository root | Verification matrix: bun run test (Vitest), bunx vitest run <path>, bun run test:e2e, test:e2e:security, focused spec via bun run test:e2e -- <path>; CI documented in .github/workflows; status documented not executed. | updated (replaced the generated block; human content kept) |
| [realworld/AGENTS.md](../../realworld/AGENTS.md) | realworld | Route agents to OpenAPI, Hurl/Bruno runners, Playwright specs and helpers, SELECTORS.md, and local skills (add-e2e-health-spec, add-e2e-null-fields-spec, add-e2e-spa-invalid-token-spec); link realworld/CLAUDE.md and CONTRIBUTING.md. | updated (replaced the generated block; human content kept) |
| [src/AGENTS.md](../../src/AGENTS.md) | src | Map ten src components (app, core/*, features/*, shared/*); point to src/app/AGENTS.md for application structure and unit-test check via Vitest on src/**/*.spec.ts. | updated (replaced the generated block; human content kept) |
| [src/app/AGENTS.md](../../src/app/AGENTS.md) | src/app | Nine-component index under app: core versus features versus shared; routing and feature ownership; link src/app/core/AGENTS.md and src/app/features/AGENTS.md. | updated (replaced the generated block; human content kept) |
| [src/app/core/AGENTS.md](../../src/app/core/AGENTS.md) | src/app/core | Auth, interceptors, layout, models: JWT flow, HTTP interceptors, shell layout; where API calls attach Token header per openapi and app patterns. | updated (replaced the generated block; human content kept) |
| [src/app/features/AGENTS.md](../../src/app/features/AGENTS.md) | src/app/features | Feature areas article, profile, settings: routes aligned with realworld E2E (/editor, /article/{slug}, /profile, /settings); which E2E specs exercise each feature. | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-health-spec/SKILL.md](../../realworld/skills/add-e2e-health-spec/SKILL.md) | realworld/specs/e2e/health.spec.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright smoke checks that the Conduit SPA loads, exposes core routes, and optionally reaches the public | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-null-fields-spec/SKILL.md](../../realworld/skills/add-e2e-null-fields-spec/SKILL.md) | realworld/specs/e2e/null-fields.spec.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add E2E coverage that null API image and bio fields render default-avatar.svg, empty bio (not the string "null"), and co | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md](../../realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md) | realworld/specs/e2e/auth.spec.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add Playwright cases that set localStorage jwtToken to an invalid value, reload, and assert unauthenticated UI plus clea | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-auth-flow-spec/SKILL.md](../../realworld/skills/add-e2e-auth-flow-spec/SKILL.md) | realworld/specs/e2e/auth.spec.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright authentication tests for register, login, logout, validation errors, session persistence, and e | created |
| [realworld/skills/add-e2e-article-crud-spec/SKILL.md](../../realworld/skills/add-e2e-article-crud-spec/SKILL.md) | realworld/specs/e2e/articles.spec.ts, realworld/specs/e2e/helpers/articles.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright article tests for create, edit, delete, favorite, author-only actions, and optional SPA-only HT | created |
| [skills/run-focused-e2e-spec/SKILL.md](../../skills/run-focused-e2e-spec/SKILL.md) | package.json, playwright.config.ts, realworld/specs/e2e | Skill: Run one Playwright E2E spec file or narrow subset via root package script without executing the full grep-filtered suite | created |
| [HOOKS.md](../../HOOKS.md) | repository | Active and proposed hooks, verification commands | updated (replaced the generated block; human content kept) |

## Files written

Markdown files created or updated: **18** (this report is not counted).

```text
├── AGENTS.md
├── ARCHITECTURE.md
├── CONTRACTS.md
├── DOMAIN.md
├── GUIDELINES.md
├── HOOKS.md
├── RULES.md
├── TESTING.md
├── realworld/
│   ├── AGENTS.md
│   └── skills/
│       ├── add-e2e-article-crud-spec/
│       │   └── SKILL.md
│       ├── add-e2e-auth-flow-spec/
│       │   └── SKILL.md
│       ├── add-e2e-health-spec/
│       │   └── SKILL.md
│       ├── add-e2e-null-fields-spec/
│       │   └── SKILL.md
│       └── add-e2e-spa-invalid-token-spec/
│           └── SKILL.md
├── skills/
│   └── run-focused-e2e-spec/
│       └── SKILL.md
└── src/
    ├── AGENTS.md
    └── app/
        ├── AGENTS.md
        ├── core/
        │   └── AGENTS.md
        └── features/
            └── AGENTS.md
```

## Skills

- [add-e2e-health-spec](../../realworld/skills/add-e2e-health-spec/SKILL.md) (local, `realworld`): Add or extend Playwright smoke checks that the Conduit SPA loads, exposes core routes, and optionally reaches the public demo API when EXTERNAL_API is enabled.
- [add-e2e-null-fields-spec](../../realworld/skills/add-e2e-null-fields-spec/SKILL.md) (local, `realworld`): Add E2E coverage that null API image and bio fields render default-avatar.svg, empty bio (not the string "null"), and correct /settings form values.
- [add-e2e-spa-invalid-token-spec](../../realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md) (local, `realworld`): Add Playwright cases that set localStorage jwtToken to an invalid value, reload, and assert unauthenticated UI plus cleared token via window.__conduit_debug__ (BROWSER_API only).
- [add-e2e-auth-flow-spec](../../realworld/skills/add-e2e-auth-flow-spec/SKILL.md) (local, `realworld`): Add or extend Playwright authentication tests for register, login, logout, validation errors, session persistence, and editor access guards using UI helpers.
- [add-e2e-article-crud-spec](../../realworld/skills/add-e2e-article-crud-spec/SKILL.md) (local, `realworld`): Add or extend Playwright article tests for create, edit, delete, favorite, author-only actions, and optional SPA-only HTTP mocks via page.route when BROWSER_API is enabled.
- [run-focused-e2e-spec](../../skills/run-focused-e2e-spec/SKILL.md) (local, `repository root`): Run one Playwright E2E spec file or narrow subset via root package script without executing the full grep-filtered suite.
- `add-e2e-comments-spec` (needs evidence): missing Full body of realworld/specs/e2e/comments.spec.ts not in evidence, Full body of realworld/specs/e2e/helpers/comments.ts not in evidence, Documented single-file run command for comments.spec.ts not separately verified beyond package.json test:e2e
- `add-e2e-error-handling-spec` (needs evidence): missing Full body of realworld/specs/e2e/error-handling.spec.ts not in evidence, setFakeAuthToken and mock fulfill patterns not excerpted
- `add-vitest-service-spec` (needs evidence): missing No excerpt of any src/**/*.spec.ts test structure or Vitest config, bun run test and path-filter usage for a single spec file not documented in provided evidence

## Hooks

| Hook | Status | Trigger | Command | Failure behavior |
|---|---|---|---|---|
| husky-pre-commit | active | pre-commit | `npx lint-staged` | block |
| pre-push-format-check | proposed | pre-push | `bun run format:check` | block |
| pre-push-unit-tests | proposed | pre-push | `bun run test` | block |
| agent-after-edit-format-check | proposed | agent: after edit | `bun run format:check` | report |

## Commands

| Command | Status | Source |
|---|---|---|
| `bunx vitest run <path-to-spec>` | documented | `package.json (test script: vitest)` |
| `bun run test` | documented | `package.json` |
| `bun run format:check` | documented | `.github/workflows/lint.yml, package.json` |
| `bun run test:coverage` | documented | `package.json` |
| `bun run build` | documented | `.github/workflows/deploy.yml, package.json` |
| `bun run test:e2e` | documented | `.github/workflows/playwright.yml, package.json` |
| `bun run test:e2e:security` | documented | `.github/workflows/security-tests.yml, package.json` |
| `bun run setup` | documented | `README.md, package.json` |

## ASD-STE100

- Architecture prose was written with ASD-STE100 Issue 9 descriptive writing rules in the prompt.
- Automated check: sentence length (max 25 words) on ARCHITECTURE.md, realworld/AGENTS.md, src/AGENTS.md, src/app/AGENTS.md, src/app/core/AGENTS.md, src/app/features/AGENTS.md: 3 long sentence(s).
- A separate standards conformance review was **not** performed.
  - `src/app/AGENTS.md`: 29 words: It contains the root shell (X), routing in X, bootstrap and HTTP wiring in X, X (auth, int...
  - `src/app/core/AGENTS.md`: 35 words: The folder X holds cross-cutting SPA infrastructure: JWT auth and session state (X), HTTP ...
  - `src/app/features/AGENTS.md`: 28 words: The X folder holds three lazy-loaded feature areas: **article** (feeds, editor, detail, co...

## RAG alert

- **Affected scope:** .github, package.json, package.json dependency entry for marked, realworld, realworld/specs/api, realworld/specs/e2e, src, src/app/core, src/app/features
- **Reason:** evidence the model asked for stayed outside the context budget after the split by component; Conformance contracts span openapi.yml, many Playwright specs and helpers, and SELECTORS.md; Angular behavior is split across core interceptors/auth and three feature folders. Agents need repeated retrieval across scattered paths not fully captured in harness Markdown alone.
- **Missing for:** Architect, Requirements
- **Index or provide:** realworld/Makefile, realworld/AGENTS.md, realworld/specs/e2e/helpers/debug.ts for complete ConduitDebug interface and verification steps, realworld/AGENTS.md and realworld/CONTRIBUTING.md for agent workflow alignment with root AGENTS.md, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/url-navigation.spec.ts, realworld/specs/e2e/user-fetch-errors.spec.ts, realworld/specs/e2e/xss-security.spec.ts, src/app/AGENTS.md, src/app/core/AGENTS.md, package.json, .github/workflows/playwright.yml, package.json dependency entry for marked, realworld/specs/e2e/SELECTORS.md, realworld/specs/api/openapi.yml, realworld/specs/e2e/helpers/*.ts, realworld/specs/e2e/*.spec.ts, src/app/**/*.ts, ARCHITECTURE.md, CLAUDE.md
- The run continued with the available evidence. Building an index is the operator's decision.


## Failures, conflicts and limits

- Evidence path not found in the scanned copy: `existing AGENTS.md`
- Evidence path not found in the scanned copy: `required local AGENTS.md list`
- Coverage gap: realworld: realworld/Makefile targets beyond bruno-check (not excerpted)
- Coverage gap: realworld: realworld/specs/api/bruno/ collection layout and environment files
- Coverage gap: realworld: realworld/specs/api/hurl/*.hurl test cases and hurl-to-bruno.js sync flow
- Coverage gap: realworld: Full openapi.yml paths for favorites and tags (excerpt truncated)
- Coverage gap: realworld: realworld/specs/e2e/playwright.base.ts webServer and baseURL configuration
- Coverage gap: realworld: Excluded E2E specs: url-navigation.spec.ts, user-fetch-errors.spec.ts, xss-security.spec.ts and helpers debug.ts, profile.ts, setup.ts
- Coverage gap: realworld: realworld/AGENTS.md, CONTRIBUTING.md, README.md guidance content
- Coverage gap: realworld: realworld/skills/*/SKILL.md workflow details
- Coverage gap: realworld: Whether root angular app imports realworld/assets/theme/styles.css directly
- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts not included in evidence excerpt
- Coverage gap: realworld: realworld/specs/e2e/user-fetch-errors.spec.ts not included in evidence excerpt
- Coverage gap: realworld: realworld/specs/e2e/xss-security.spec.ts not included in evidence excerpt
- Coverage gap: realworld: realworld/specs/e2e/helpers/debug.ts contract referenced in SELECTORS.md and auth.spec.ts but file body not in evidence
- Coverage gap: realworld: realworld/specs/e2e/helpers/profile.ts not included in evidence excerpt
- Coverage gap: realworld: realworld/specs/e2e/helpers/setup.ts not included in evidence excerpt
- Coverage gap: realworld: Contents of realworld/specs/api/hurl/*.hurl files not shown in evidence
- Coverage gap: realworld: Full playwright.base.ts webServer and project configuration not in evidence
- Coverage gap: realworld: realworld/specs/api/openapi.yml endpoints detail not excerpted
- Coverage gap: realworld: navigation.spec.ts, error-handling.spec.ts, health.spec.ts, null-fields.spec.ts, settings.spec.ts, social.spec.ts listed in inventory but not excerpted
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/url-navigation.spec.ts — deep-link and URL behavior unknown to this analysis.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/user-fetch-errors.spec.ts — referenced from error-handling for 401 on page load; behavior not verified here.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/xss-security.spec.ts — security E2E scope undocumented in evidence.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/helpers/debug.ts — getToken/getCurrentUser implementation not shown.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/helpers/profile.ts — followUser/unfollowUser/updateProfile steps not shown.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/helpers/setup.ts — createUserInIsolation/createManyArticles isolation strategy not shown.
- Coverage gap: realworld: helpers/config.ts BROWSER_API and EXTERNAL_API assignment logic not in evidence blocks.
- Coverage gap: realworld: helpers/api.ts request shapes and base URL configuration not in evidence blocks.
- Coverage gap: realworld: Root playwright.config.ts merge of baseConfig (testDir path, webServer command, baseURL) not in evidence.
- Coverage gap: realworld: realworld/specs/api runners (Bruno, Hurl) execution and relation to SPA not described in excerpts.
- Coverage gap: src/app/features/article: Exact route paths and lazy-loading for HomeComponent, ArticleComponent, and EditorComponent are not shown in the supplied excerpts (only src/app/app.routes.ts is listed in inventory).

## Recommendations

- Link from root AGENTS.md to drafted local skills add-e2e-auth-flow-spec, add-e2e-article-crud-spec, and run-focused-e2e-spec once caller renders SKILL.md bodies; do not duplicate realworld/skills content.
- Document lint-staged globs in AGENTS.md or GUIDELINES.md when evidence is added; pre-commit invokes npx lint-staged but configuration was not in supplied evidence.
- Note in TESTING.md that GitHub Actions lint.yml runs format:check and playwright/security workflows run E2E but no workflow in evidence runs bun run test (Vitest) on CI.
- Consider operator approval for proposed hooks pre-push-format-check, pre-push-unit-tests, and agent-after-edit-format-check from automation before enabling.
- Preserve realworld/AGENTS.md and realworld/CLAUDE.md as upstream-oriented guidance; root harness links rather than merges RealWorld subtree policies.

## Project context

| Key | Value |
|---|---|
| application | Conduit (RealWorld) Angular example SPA |
| language | TypeScript |
| framework | Angular (project angular-conduit in angular.json) |
| package_manager | Bun |
| entry_point | src/main.ts |
| routing | src/app/app.routes.ts |
| api_client | HTTP client to RealWorld REST API (default https://api.realworld.show/api in E2E config) |
| test_runner | Vitest (vitest.config.ts, src/**/*.spec.ts) |
| e2e_runner | Playwright (playwright.config.ts, testDir realworld/specs/e2e) |
| setup_hint | bun run setup after clone |
| start_hint | bun run start; baseURL http://localhost:4200 for E2E |
| build_hint | bun run build; output dist/angular-conduit per angular.json |
| test_hint | bun run test for unit; bun run test:e2e for conformance E2E |

## Publication

- Branch: `shipAI` · pushed: after this report
