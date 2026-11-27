# INIT report

- Generated: 2026-11-27 00:02 UTC
- Run: `f18f023209c3`
- Repository: https://github.com/shira-ozana/angular-realworld-example-app
- Base commit: `2c8c837809b5877b0f3759a57a454ac52c4b207e` (ref `main`) · branch `shipAI`

## Start here

Requirements and Architect start with these files:

- [AGENTS.md](../../AGENTS.md): Primary agent router: component map, where to read next, linked skills, verification commands, and links to human-authored CLAUDE.md and README without duplicating them
- [ARCHITECTURE.md](../../ARCHITECTURE.md): Component behavior, entry points, interfaces, dependencies, and data flow with path citations; gaps labeled for Requirements and Architect
- [RULES.md](../../RULES.md): Preserve harness-only edits, cite evidence paths, explicit command status, and alignment with existing user or project rules

> This repository is an Angular 21 Conduit (RealWorld) single-page application under `src/app`, bundled with a vendored `realworld` conformance pack (shared Playwright E2E, OpenAPI, Bruno/Hurl API tests, and Starlight docs). TypeScript is used throughout; Bun is the package manager. The SPA implements auth, articles, comments, profiles, and feeds against a configurable REST API; the root wires Vitest unit tests and Playwright that extends `realworld/specs/e2e/playwright.base.ts` with a local dev server at `http://localhost:4200`.

## Scan scope

- Files scanned: 181 · components: 13 · analyzed: 13
- Include: all · exclude: none
- Files not sent to the model (context budget): 20
- Files sent truncated: 9

## Harness map

| File | Scope | Purpose | Result |
|---|---|---|---|
| [AGENTS.md](../../AGENTS.md) | Repository root; Angular SPA, realworld pack, scripts, and verification entry points | Primary agent router: component map, where to read next, linked skills, verification commands, and links to human-authored CLAUDE.md and README without duplicating them | updated (replaced the generated block; human content kept) |
| [ARCHITECTURE.md](../../ARCHITECTURE.md) | Whole system: src/app SPA, realworld conformance pack, test runners, data flow | Component behavior, entry points, interfaces, dependencies, and data flow with path citations; gaps labeled for Requirements and Architect | updated (replaced the generated block; human content kept) |
| [RULES.md](../../RULES.md) | Agent binding rules for this repository | Preserve harness-only edits, cite evidence paths, explicit command status, and alignment with existing user or project rules | updated (replaced the generated block; human content kept) |
| [GUIDELINES.md](../../GUIDELINES.md) | Multiple valid patterns (E2E TEST_MODE, API mocks, formatting, feature layout) | Document when to use which pattern without contradicting GUIDELINES or realworld specs | updated (links repaired) |
| [CONTRACTS.md](../../CONTRACTS.md) | REST API, E2E DOM and routes, debug surface | Link OpenAPI, SELECTORS.md, and Token header contract for Requirements and implementers | updated (links repaired) |
| [DOMAIN.md](../../DOMAIN.md) | Conduit / RealWorld business vocabulary | Articles, profiles, feeds, auth terms shared by SPA and conformance specs | updated (links repaired) |
| [TESTING.md](../../TESTING.md) | Vitest, Playwright, Bruno, Hurl, and CI-relevant commands | Centralize verification commands and skill references; statuses documented per package.json and workflows | updated (links repaired) |
| [src/AGENTS.md](../../src/AGENTS.md) | src tree: app and all listed subcomponents | Map ten components under src; route to src/app/AGENTS.md and core/features/shared areas | created |
| [src/app/AGENTS.md](../../src/app/AGENTS.md) | Angular application: core, features, shared | Nine-component map, local conventions, skills run-vitest-unit-tests and E2E skills that touch SPA routes and services | updated (replaced the generated block; human content kept) |
| [src/app/core/AGENTS.md](../../src/app/core/AGENTS.md) | auth, interceptors, layout, models | Route agents to auth JWT flow, HTTP interceptors, shell layout, and shared models; link RULES and unit-test skill | created |
| [src/app/features/AGENTS.md](../../src/app/features/AGENTS.md) | article, profile, settings feature areas | Map three feature modules to routes and services; link domain E2E skills and CONTRACTS | created |
| [realworld/AGENTS.md](../../realworld/AGENTS.md) | Vendored conformance pack: API, E2E, docs, assets | Preserve human content; point to realworld skills (Bruno, Hurl, Playwright pack, docs dev) without replacing CONTRIBUTING or CLAUDE | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-health-spec/SKILL.md](../../realworld/skills/add-e2e-health-spec/SKILL.md) | realworld/specs/e2e/health.spec.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright smoke checks that the Conduit SPA loads, exposes core routes, and optionally reaches the public | created |
| [realworld/skills/add-e2e-null-fields-spec/SKILL.md](../../realworld/skills/add-e2e-null-fields-spec/SKILL.md) | realworld/specs/e2e/null-fields.spec.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add E2E coverage that null API image and bio fields render default-avatar.svg, empty bio (not the string "null"), and co | created |
| [realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md](../../realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md) | realworld/specs/e2e/auth.spec.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add Playwright cases that set localStorage jwtToken to an invalid value, reload, and assert unauthenticated UI plus clea | created |
| [HOOKS.md](../../HOOKS.md) | repository | Active and proposed hooks, verification commands | updated (replaced the generated block; human content kept) |
| `skills/add-e2e-api-error-test/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/add-e2e-domain-spec/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/add-e2e-navigation-social-spec/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/add-spa-route-mock-test/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/check-bruno-hurl-sync/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-bruno-api-tests/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-hurl-api-tests/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-playwright-e2e-tests/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-playwright-security-e2e-tests/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-playwright-single-spec/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-realworld-docs-dev/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |
| `skills/run-vitest-unit-tests/SKILL.md` | - | - | removed (INIT skill moved or no longer derived) |

## Files written

Markdown files created or updated: **16** (this report is not counted).

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
│       ├── add-e2e-health-spec/
│       │   └── SKILL.md
│       ├── add-e2e-null-fields-spec/
│       │   └── SKILL.md
│       └── add-e2e-spa-invalid-token-spec/
│           └── SKILL.md
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
- `add-e2e-api-error-test` (shared, by reference): 
- `add-e2e-domain-spec` (shared, by reference): 
- `add-e2e-navigation-social-spec` (shared, by reference): 
- `add-spa-route-mock-test` (shared, by reference): 
- `check-bruno-hurl-sync` (shared, by reference): 
- `run-bruno-api-tests` (shared, by reference): 
- `run-hurl-api-tests` (shared, by reference): 
- `run-playwright-e2e-tests` (shared, by reference): 
- `run-playwright-security-e2e-tests` (shared, by reference): 
- `run-playwright-single-spec` (shared, by reference): 
- `run-realworld-docs-dev` (shared, by reference): 
- `run-vitest-unit-tests` (shared, by reference): 
- `add-vitest-service-unit-test` (needs evidence): missing Excerpts of src/app/**/*.service.spec.ts showing describe/it structure, TestBed or inject patterns, and mocks, vitest.config path and Angular test provider setup
- `add-e2e-url-navigation-spec` (needs evidence): missing realworld/specs/e2e/url-navigation.spec.ts file content
- `add-e2e-user-fetch-errors-spec` (needs evidence): missing realworld/specs/e2e/user-fetch-errors.spec.ts file content
- `add-e2e-xss-security-spec` (needs evidence): missing realworld/specs/e2e/xss-security.spec.ts content and @security tag usage pattern
- `implement-conduit-debug-interface` (needs evidence): missing src/app implementation of window.__conduit_debug__, realworld/specs/e2e/helpers/debug.ts source

## Hooks

| Hook | Status | Trigger | Command | Failure behavior |
|---|---|---|---|---|
| husky-pre-commit-lint-staged | active | pre-commit | `npx lint-staged` | block |
| pre-push-format-check | proposed | pre-push | `bun run format:check` | block |
| pre-push-unit-tests | proposed | pre-push | `bun run test` | block |
| agent-after-edit-format-check | proposed | agent: after edit | `bun run format:check` | warn |

## Commands

| Command | Status | Source |
|---|---|---|
| `bun run format` | documented | `package.json` |
| `bun run test` | documented | `package.json` |
| `bun run format:check` | documented | `.github/workflows/lint.yml` |
| `bun run test:coverage` | documented | `package.json` |
| `bun run test:e2e` | documented | `.github/workflows/playwright.yml` |
| `bun run test:e2e:security` | documented | `.github/workflows/security-tests.yml` |
| `bun run build` | documented | `.github/workflows/deploy.yml` |

## ASD-STE100

- Architecture prose was written with ASD-STE100 Issue 9 descriptive writing rules in the prompt.
- Automated check: sentence length (max 25 words) on ARCHITECTURE.md, src/AGENTS.md, src/app/AGENTS.md, src/app/core/AGENTS.md, src/app/features/AGENTS.md, realworld/AGENTS.md: 5 long sentence(s).
- A separate standards conformance review was **not** performed.
  - `src/app/AGENTS.md`: 29 words: It contains the root shell (X), routing in X, bootstrap and HTTP wiring in X, X (auth, int...
  - `src/app/AGENTS.md`: 27 words: Routes in X: X and X → home; X, X → guest-only auth; X, X, X → X; X → lazy profile routes;...
  - `src/app/core/AGENTS.md`: 35 words: The folder X holds cross-cutting SPA infrastructure: JWT auth and session state (X), HTTP ...
  - `src/app/core/AGENTS.md`: 29 words: Auth bootstrap and mid-session 401 handling are split: X errors are handled in X; other en...
  - `src/app/features/AGENTS.md`: 28 words: The X folder holds three lazy-loaded feature areas: **article** (feeds, editor, detail, co...

## RAG alert

- **Affected scope:** .github, realworld, realworld/docs/src/content, realworld/specs/api, realworld/specs/e2e, skills, src/app
- **Reason:** evidence the model asked for stayed outside the context budget after the split by component; Conformance contract is split across SELECTORS.md, OpenAPI, many Playwright specs and helpers, and Starlight docs; agents repeatedly need retrieval across paths after component-scoped AGENTS.md routing.
- **Missing for:** Architect, Requirements
- **Index or provide:** skills/check-bruno-hurl-sync/SKILL.md and skills/run-* referencing realworld — alignment with scripts (Requirements)., realworld/specs/e2e/helpers/debug.ts (Requirements for debug hook implementation)., realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/url-navigation.spec.ts, realworld/specs/e2e/user-fetch-errors.spec.ts, realworld/specs/e2e/xss-security.spec.ts, .github/workflows/deploy.yml, .github/workflows/playwright.yml, realworld/specs/e2e/SELECTORS.md, realworld/specs/api/openapi.yml, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/articles.ts, realworld/specs/e2e/helpers/comments.ts, realworld/specs/api/README.md, CLAUDE.md, realworld/CLAUDE.md
- The run continued with the available evidence. Building an index is the operator's decision.


## Failures, conflicts and limits

- Conflict (needs a decision): realworld/.github/workflows/deploy-docs.yml path filter docs/** vs inventory placing documentation under realworld/docs/ — workflow working-directory may not match vendored layout without adaptation (evidence: analysis coverage_gaps; consumers: Architect, CI operator).
- Conflict (needs a decision): Human-authored realworld/CONTRIBUTING.md and realworld/README.md not in evidence — local realworld/AGENTS.md update must not contradict them; operator review if instructions diverge (evidence: analysis coverage_gaps).
- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts, user-fetch-errors.spec.ts, xss-security.spec.ts and helpers debug.ts, profile.ts, setup.ts were excluded from this analysis part (1/3).
- Coverage gap: realworld: realworld/Makefile targets besides bruno-check (e.g. hurl-to-bruno, full api test recipes) are not evidenced in excerpts.
- Coverage gap: realworld: realworld/specs/api/bruno/ collection layout, realworld/specs/api/hurl/*.hurl files, realworld/specs/api/hurl-to-bruno.js, and realworld/specs/api/README.md not provided.
- Coverage gap: realworld: realworld/specs/e2e/playwright.base.ts, helpers (api, auth, articles, etc.), and domain spec files not excerpted in part 1.
- Coverage gap: realworld: realworld/AGENTS.md, realworld/CLAUDE.md, realworld/CONTRIBUTING.md, realworld/README.md content not in evidence.
- Coverage gap: realworld: deploy-docs.yml paths reference docs/** at repo root while inventory places docs under realworld/docs/; workflow working-directory may not match vendored layout without adaptation (Architect).
- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts not included in evidence for part 2/3.
- Coverage gap: realworld: realworld/specs/e2e/user-fetch-errors.spec.ts not included.
- Coverage gap: realworld: realworld/specs/e2e/xss-security.spec.ts not included.
- Coverage gap: realworld: realworld/specs/e2e/helpers/debug.ts not included; only SELECTORS.md and auth.spec imports document the debug contract partially.
- Coverage gap: realworld: realworld/specs/e2e/helpers/profile.ts and setup.ts not included.
- Coverage gap: realworld: realworld/specs/api/openapi.yml not excerpted; OpenAPI as API contract source unverified in this part.
- Coverage gap: realworld: realworld/specs/e2e/playwright.base.ts not excerpted; dev server and project defaults unknown from evidence.
- Coverage gap: realworld: Individual .hurl file contents and bruno .bru requests not shown.
- Coverage gap: realworld: realworld/assets/generator and theme styles behavior not excerpted.
- Coverage gap: realworld: realworld/Makefile targets not excerpted.
- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts not included in evidence; deep-link and URL behavior unverified in this analysis.
- Coverage gap: realworld: realworld/specs/e2e/user-fetch-errors.spec.ts not included; 401-on-page-load handling referenced only by comment in error-handling.spec.ts.
- Coverage gap: realworld: realworld/specs/e2e/xss-security.spec.ts not included; security E2E scope unknown beyond package.json test:e2e:security grep.
- Coverage gap: realworld: realworld/specs/e2e/helpers/config.ts not excerpted; exact BROWSER_API and EXTERNAL_API derivation unknown.
- Coverage gap: realworld: realworld/specs/e2e/helpers/api.ts not excerpted; API helper request shapes and auth headers unknown.
- Coverage gap: realworld: realworld/specs/e2e/helpers/debug.ts, profile.ts, setup.ts not excerpted; implementation of getToken, followUser, createUserInIsolation unknown.
- Coverage gap: realworld: OpenAPI, Bruno, and Hurl API test trees under realworld/specs/api/ are inventory-only for this component slice; no API-pack behavior analyzed here.
- Coverage gap: realworld: realworld/docs Starlight site behavior not covered in supplied E2E evidence.
- Coverage gap: src/app/features/article: Exact route definitions and guards for home, article, editor, and tag paths in src/app/app.routes.ts are not included in part 1 evidence.
- Coverage gap: src/app/features/article: tags.service.spec.ts behavior and tests are not excerpted.
- Coverage gap: src/app/features/article: How error.interceptor maps HTTP failures to Errors objects consumed by article pages is not shown in article feature excerpts.
- Coverage gap: src/app/features/article: RealWorld OpenAPI contract alignment for article endpoints is not cross-checked in this evidence set.
- Coverage gap: src/app/features/article: tags.service.ts implementation (URL base path, map operator, error handling) is not shown in supplied excerpts for part 2.
- Coverage gap: src/app/features/article: ArticlesService and CommentsService endpoints, methods, and response shapes are not evidenced in part 2 excerpts.

## Recommendations

- Complete skills/add-vitest-service-unit-test/SKILL.md after excerpts of src/app/**/*.service.spec.ts and vitest config are available (evidence: skills analysis missing_evidence).
- Link root AGENTS.md and TESTING.md to existing skills at skills/run-playwright-e2e-tests/SKILL.md and skills/run-vitest-unit-tests/SKILL.md rather than duplicating steps (evidence: existing harness files list).
- Document lint-staged configuration in AGENTS.md or DEVELOPMENT only when .lintstagedrc or package.json lint-staged block is evidenced — pre-commit runs npx lint-staged but config was not supplied (evidence: automation notes).
- Proposed hooks pre-push-format-check, pre-push-unit-tests, and agent-after-edit-format-check remain operator-enabled; HOOKS.md already exists and is caller-rendered (evidence: automation.hooks).
- When touching API assertions, prefer skill check-bruno-hurl-sync before committing Bruno tree changes (evidence: realworld/specs/api/hurl-to-bruno.js, skills/check-bruno-hurl-sync/SKILL.md).

## Project context

| Key | Value |
|---|---|
| application | Conduit (RealWorld) social blogging SPA plus embedded RealWorld spec/tests/docs pack |
| language | TypeScript |
| framework | Angular 21 |
| package_manager | Bun |
| entry_point | src/main.ts |
| routing | Angular Router via src/app/app.routes.ts |
| api_client | HTTP to Conduit REST API (default https://api.realworld.show/api; JWT in localStorage key jwtToken) |
| test_runner | Vitest (src/**/*.spec.ts, vitest.config.ts) |
| e2e_runner | Playwright (realworld/specs/e2e, root playwright.config.ts) |
| setup_hint | Requires Bun; run bun run setup after clone (README.md) |
| start_hint | bun run start — dev server at http://localhost:4200 (playwright.config.ts) |
| build_hint | bun run build — output dist/angular-conduit (angular.json) |
| test_hint | bun run test for unit; bun run test:e2e for conformance E2E; bun run test:e2e:security for @security specs |

## Publication

- Branch: `shipAI` · pushed: after this report
