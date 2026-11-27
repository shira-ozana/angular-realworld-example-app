# INIT report

- Generated: 2026-11-27 03:33 UTC
- Run: `2a93c4d6106a` · feature `1897094f-7783-48f3-b713-6d94fa5d508c`
- Repository: https://github.com/shira-ozana/angular-realworld-example-app
- Base commit: `2c8c837809b5877b0f3759a57a454ac52c4b207e` (ref `main`) · branch `shipAI`

## Start here

Requirements and Architect start with these files:

- [AGENTS.md](../../AGENTS.md): Primary agent entry: repository layout (Angular app under src/, vendored realworld/), verification commands (bun run test, test:e2e, build, format:check), links to ARCHITECTURE.md, RULES.md, TESTING.md, src/AGENTS.md, realworld/AGENTS.md, and skills (skills/run-focused-e2e-spec, realworld/skills/*).
- [ARCHITECTURE.md](../../ARCHITECTURE.md): System map: root Angular Conduit SPA, component routes under src/app (core, features, shared), Playwright E2E extending realworld/specs/e2e/playwright.base.ts, API contract in realworld/specs/api/openapi.yml; entry points, data flow JWT via interceptors to RealWorld API, and dependency between app and vendored conformance bundle.
- [RULES.md](../../RULES.md): Binding constraints for agent edits: harness-only changes outside application code unless tasked; match existing Angular/Vitest/Playwright conventions; preserve human-authored realworld and CLAUDE guidance; cite SELECTORS.md and openapi for contract changes.

> This repository is an Angular single-page application that implements the Conduit (RealWorld) social blogging product: JWT auth, articles, comments, profiles, feeds, and favorites. Application code lives under `src/`; a vendored `realworld` tree supplies OpenAPI contracts, shared Playwright E2E specs, Bruno/Hurl API tests, and Starlight documentation. The root uses Bun as the package manager, Vitest for colocated unit tests under `src/app`, and Playwright (extending `realworld/specs/e2e/playwright.base.ts`) against `http://localhost:4200`.

## Scan scope

- Files scanned: 178 · components: 13 · analyzed: 13
- Include: all · exclude: none
- Files not sent to the model (context budget): 23
- Files sent truncated: 9

## Harness map

| File | Scope | Purpose | Result |
|---|---|---|---|
| [AGENTS.md](../../AGENTS.md) | (root) | Primary agent entry: repository layout (Angular app under src/, vendored realworld/), verification commands (bun run test, test:e2e, build, format:check), links to ARCHITECTURE.md, RULES.md, TESTING.md, src/AGENTS.md, realworld/AGENTS.md, and skills (skills/run-focused-e2e-spec, realworld/skills/*). | updated (replaced the generated block; human content kept) |
| [ARCHITECTURE.md](../../ARCHITECTURE.md) | (root) | System map: root Angular Conduit SPA, component routes under src/app (core, features, shared), Playwright E2E extending realworld/specs/e2e/playwright.base.ts, API contract in realworld/specs/api/openapi.yml; entry points, data flow JWT via interceptors to RealWorld API, and dependency between app and vendored conformance bundle. | updated (replaced the generated block; human content kept) |
| [RULES.md](../../RULES.md) | (root) | Binding constraints for agent edits: harness-only changes outside application code unless tasked; match existing Angular/Vitest/Playwright conventions; preserve human-authored realworld and CLAUDE guidance; cite SELECTORS.md and openapi for contract changes. | updated (replaced the generated block; human content kept) |
| [GUIDELINES.md](../../GUIDELINES.md) | (root) | Multiple valid patterns: Vitest colocated tests under src/app, Playwright modes (BROWSER_API, EXTERNAL_API, TEST_MODE) per realworld/specs/e2e/helpers/config.ts, and feature-folder layout; when to use which skill without duplicating SKILL.md bodies. | kept |
| [CONTRACTS.md](../../CONTRACTS.md) | (root) | REST and UI contracts: OpenAPI paths and Token security scheme, SPA routes and DOM selectors for shared E2E; pointers to realworld/specs/api/openapi.yml and realworld/specs/e2e/SELECTORS.md. | kept |
| [DOMAIN.md](../../DOMAIN.md) | (root) | Conduit (RealWorld) vocabulary: articles, slugs, favorites, follows, feeds, jwtToken, profiles, tags for Requirements and Architect alignment with product behavior. | kept |
| [TESTING.md](../../TESTING.md) | (root) | Verification matrix: bun run test (Vitest), bun run test:e2e / test:e2e:security (Playwright, realworld/specs/e2e), format:check; prerequisite bun run start or webServer; link skill run-focused-e2e-spec. | kept |
| [realworld/AGENTS.md](../../realworld/AGENTS.md) | realworld | Vendored RealWorld bundle: API runners (run-api-tests-bruno.sh, run-api-tests-hurl.sh), E2E specs and helpers, docs (realworld/docs), Makefile/bruno-check; routes agents to realworld/skills for adding E2E patterns and CLAUDE.md/CONTRIBUTING.md for upstream norms. | updated (replaced the generated block; human content kept) |
| [src/AGENTS.md](../../src/AGENTS.md) | src | Map ten components under src/app (core/auth, interceptors, layout, models; features/article, profile, settings; shared/components, pipes); entry app bootstrap; how to verify (bun run test, build); link src/app/AGENTS.md. | updated (replaced the generated block; human content kept) |
| [src/app/AGENTS.md](../../src/app/AGENTS.md) | src/app | Angular application shell: routing among core, features, shared; which local AGENTS.md covers auth vs features; conventions for colocated *.spec.ts Vitest files. | updated (replaced the generated block; human content kept) |
| [src/app/core/AGENTS.md](../../src/app/core/AGENTS.md) | src/app/core | Core cross-cutting components: auth, HTTP interceptors (JWT), layout, shared models; interfaces to RealWorld API base URL and token storage per app patterns. | updated (replaced the generated block; human content kept) |
| [src/app/features/AGENTS.md](../../src/app/features/AGENTS.md) | src/app/features | Feature modules article, profile, settings: routes (/editor, /article/:slug, /profile/:username, /settings), UI contract alignment with E2E selectors; per-feature file locations. | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-article-crud-spec/SKILL.md](../../realworld/skills/add-e2e-article-crud-spec/SKILL.md) | realworld/specs/e2e/articles.spec.ts, realworld/specs/e2e/helpers/articles.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright article tests for create, edit, delete, favorite, author-only actions, and optional SPA-only HT | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-auth-flow-spec/SKILL.md](../../realworld/skills/add-e2e-auth-flow-spec/SKILL.md) | realworld/specs/e2e/auth.spec.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright authentication tests for register, login, logout, validation errors, session persistence, and e | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-health-spec/SKILL.md](../../realworld/skills/add-e2e-health-spec/SKILL.md) | realworld/specs/e2e/health.spec.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend Playwright smoke checks that the Conduit SPA loads, exposes core routes, and optionally reaches the public | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-null-fields-spec/SKILL.md](../../realworld/skills/add-e2e-null-fields-spec/SKILL.md) | realworld/specs/e2e/null-fields.spec.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add E2E coverage that null API image and bio fields render default-avatar.svg, empty bio (not the string "null"), and co | updated (replaced the generated block; human content kept) |
| [realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md](../../realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md) | realworld/specs/e2e/auth.spec.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend SPA tests that an invalid or stale jwtToken in localStorage is cleared, the UI shows unauthenticated navig | updated (replaced the generated block; human content kept) |
| [skills/run-focused-e2e-spec/SKILL.md](../../skills/run-focused-e2e-spec/SKILL.md) | playwright.config.ts, realworld/specs/e2e, package.json | Skill: Run one Playwright E2E spec file or a narrow subset during development instead of the full suite (test:e2e excludes @sec | updated (replaced the generated block; human content kept) |
| [HOOKS.md](../../HOOKS.md) | repository | Active and proposed hooks, verification commands | updated (replaced the generated block; human content kept) |

## Files written

Markdown files created or updated: **15** (this report is not counted).

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

- [add-e2e-article-crud-spec](../../realworld/skills/add-e2e-article-crud-spec/SKILL.md) (local, `realworld`): Add or extend Playwright article tests for create, edit, delete, favorite, author-only actions, and optional SPA-only HTTP mocks via page.route when BROWSER_API is enabled.
- [add-e2e-auth-flow-spec](../../realworld/skills/add-e2e-auth-flow-spec/SKILL.md) (local, `realworld`): Add or extend Playwright authentication tests for register, login, logout, validation errors, session persistence, and editor access guards using UI helpers.
- [add-e2e-health-spec](../../realworld/skills/add-e2e-health-spec/SKILL.md) (local, `realworld`): Add or extend Playwright smoke checks that the Conduit SPA loads, exposes core routes, and optionally reaches the public demo API when EXTERNAL_API is enabled.
- [add-e2e-null-fields-spec](../../realworld/skills/add-e2e-null-fields-spec/SKILL.md) (local, `realworld`): Add E2E coverage that null API image and bio fields render default-avatar.svg, empty bio (not the string "null"), and correct /settings form values.
- [add-e2e-spa-invalid-token-spec](../../realworld/skills/add-e2e-spa-invalid-token-spec/SKILL.md) (local, `realworld`): Add or extend SPA tests that an invalid or stale jwtToken in localStorage is cleared, the UI shows unauthenticated navigation, and window.__conduit_debug__.getToken returns null after reload.
- [run-focused-e2e-spec](../../skills/run-focused-e2e-spec/SKILL.md) (local, `repository root`): Run one Playwright E2E spec file or a narrow subset during development instead of the full suite (test:e2e excludes @security by default).

## Hooks

| Hook | Status | Trigger | Command | Failure behavior |
|---|---|---|---|---|
| husky-pre-commit | active | pre-commit | `npx lint-staged` | block |
| pre-push-unit-tests | proposed | pre-push | `bun run test` | block |
| agent-after-edit-format-check | proposed | agent: after edit | `bun run format:check` | report |
| pre-push-production-build | proposed | pre-push | `bun run build` | block |

## Commands

| Command | Status | Source |
|---|---|---|
| `bun run format` | documented | `package.json` |
| `bun run format:check` | documented | `package.json` |
| `bun run test` | documented | `package.json` |
| `bun run test:coverage` | documented | `package.json` |
| `bun run build` | documented | `package.json` |
| `bun run test:e2e` | documented | `package.json` |
| `bun run test:e2e:security` | documented | `package.json` |
| `bun install` | documented | `package.json` |
| `bun run start` | documented | `README.md` |
| `bun run setup` | documented | `README.md` |

## ASD-STE100

- Architecture prose was written with ASD-STE100 Issue 9 descriptive writing rules in the prompt.
- Automated check: sentence length (max 25 words) on ARCHITECTURE.md, realworld/AGENTS.md, src/AGENTS.md, src/app/AGENTS.md, src/app/core/AGENTS.md, src/app/features/AGENTS.md: 4 long sentence(s).
- A separate standards conformance review was **not** performed.
  - `src/app/AGENTS.md`: 27 words: Follow ../../RULES.md: harness-only agent edits unless tasked on application code; standal...
  - `src/app/core/AGENTS.md`: 35 words: The folder X holds cross-cutting SPA infrastructure: JWT auth and session state (X), HTTP ...
  - `src/app/features/AGENTS.md`: 28 words: The X folder holds three lazy-loaded feature areas: **article** (feeds, editor, detail, co...
  - `src/app/features/AGENTS.md`: 35 words: Examples tied to this folder: X, X, X, X / settings form X attributes (X, X, X, X, X), pro...

## RAG alert

- **Affected scope:** (root) Playwright integration, .github, angular.json, angular.json or asset configuration for default-avatar.svg, realworld, realworld/specs/api, realworld/specs/e2e
- **Reason:** evidence the model asked for stayed outside the context budget after the split by component; Large vendored realworld tree (OpenAPI, SELECTORS.md, many spec and helper modules) is only partially captured in ARCHITECTURE split; repeated retrieval helps Requirements and Architect for E2E/API conformance without inventing paths.
- **Missing for:** Requirements, Architect
- **Index or provide:** realworld/Makefile, realworld/AGENTS.md, realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/url-navigation.spec.ts, realworld/specs/e2e/user-fetch-errors.spec.ts, realworld/specs/e2e/xss-security.spec.ts, realworld/specs/e2e/helpers/profile.ts, angular.json, .github/workflows/lint.yml, .github/workflows/playwright.yml, angular.json or asset configuration for default-avatar.svg, realworld/specs/api/openapi.yml, realworld/specs/e2e/SELECTORS.md, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/helpers/api.ts, realworld/specs/e2e/*.spec.ts, realworld/docs/src/content/docs
- The run continued with the available evidence. Building an index is the operator's decision.


## Failures, conflicts and limits

- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts, user-fetch-errors.spec.ts, xss-security.spec.ts not included in part 1/3
- Coverage gap: realworld: realworld/specs/e2e/helpers/debug.ts, profile.ts, setup.ts not included in part 1/3
- Coverage gap: realworld: realworld/Makefile targets beyond bruno-check not shown in evidence
- Coverage gap: realworld: realworld/specs/api/bruno/ collection layout and individual .bru requests not excerpted
- Coverage gap: realworld: realworld/specs/e2e/playwright.base.ts body not excerpted in this part
- Coverage gap: realworld: realworld/AGENTS.md, realworld/README.md, realworld/CONTRIBUTING.md content not excerpted
- Coverage gap: realworld: realworld/.github/workflows/deploy-docs.yml paths filter docs/** may not match monorepo layout where docs live under realworld/docs (workflow file uses ./docs working-directory in steps)
- Coverage gap: realworld: Excerpts for realworld/specs/e2e/url-navigation.spec.ts, user-fetch-errors.spec.ts, xss-security.spec.ts not supplied in any analysis part.
- Coverage gap: realworld: Excerpts for realworld/specs/e2e/helpers/debug.ts, profile.ts, setup.ts not supplied; auth.spec imports debug helpers without full contract source in evidence.
- Coverage gap: realworld: hurl-to-bruno.js body truncated mid assertToJs; full assert mapping and generateBruFile behavior not verified.
- Coverage gap: realworld: No evidence content for realworld/specs/api/openapi.yml, Hurl .hurl files, run-api-tests-bruno.sh, run-api-tests-hurl.sh.
- Coverage gap: realworld: No excerpt for realworld/specs/e2e/playwright.base.ts, navigation.spec.ts, error-handling.spec.ts, health.spec.ts, social.spec.ts, settings.spec.ts, null-fields.spec.ts.
- Coverage gap: realworld: CI workflows realworld/.github/workflows/bruno-check.yml interaction with hurl-to-bruno --check not excerpted.
- Coverage gap: realworld: Starlight docs site under realworld/docs/ not covered in this part.
- Coverage gap: realworld: Content of realworld/specs/e2e/url-navigation.spec.ts not in part 3 evidence.
- Coverage gap: realworld: Content of realworld/specs/e2e/user-fetch-errors.spec.ts not in part 3 evidence (error-handling.spec.ts references 401 on page load tested there).
- Coverage gap: realworld: Content of realworld/specs/e2e/xss-security.spec.ts not in part 3 evidence (root test:e2e:security targets @security).
- Coverage gap: realworld: Full implementations of realworld/specs/e2e/helpers/debug.ts, profile.ts, and setup.ts not included in excerpts.
- Coverage gap: realworld: realworld/specs/e2e/helpers/config.ts definition of BROWSER_API and EXTERNAL_API not shown in evidence.
- Coverage gap: realworld: Root playwright.config.ts merge of baseConfig, testDir path to realworld specs, and webServer command not excerpted.
- Coverage gap: realworld: realworld/specs/e2e/SELECTORS.md content not excerpted.
- Coverage gap: realworld: API test scripts (Bruno/Hurl) and openapi.yml behavior not analyzed in part 3 E2E-focused evidence.
- Coverage gap: realworld: realworld/docs Astro site and Makefile targets not described from source excerpts in this part.
- Coverage gap: src/app/features/article: Exact route paths and lazy-loading for HomeComponent, ArticleComponent, and EditorComponent are not evidenced (src/app/app.routes.ts not supplied).
- Coverage gap: src/app/features/article: ArticleListConfig filters author and favorited are defined but no article-feature page excerpt shows setting those filters (may live in profile feature).
- Coverage gap: src/app/features/article: tags.service.spec.ts and full tags.service unit behavior not included in evidence excerpts.
- Coverage gap: src/app/features/article: HTTP error shaping (Errors model) on article load depends on interceptors or catchError patterns not shown in service files.
- Coverage gap: src/app/features/article: E2E selectors and flows for articles live under realworld/specs/e2e/articles.spec.ts but were not excerpted for this component.
- Coverage gap: src/app/features/article: src/app/features/article/services/tags.service.ts implementation body is not in the supplied excerpt (only tags.service.spec.ts).
- Coverage gap: src/app/features/article: Route paths and guards for home, article/:slug, and editor are not excerpted from src/app/app.routes.ts.

## Recommendations

- Root AGENTS.md should link skills/run-focused-e2e-spec/SKILL.md and realworld/skills/* without duplicating step lists (per G3).
- Document lint-staged task definitions in TESTING.md or DEVELOPMENT.md once .lintstagedrc or equivalent is indexed; pre-commit husky hook is active but tasks are unknown (Architect).
- Consider wiring bun run test into a GitHub Actions job; automation notes indicate Vitest is package-documented only, not CI-excerpted.
- Proposed hooks pre-push-unit-tests, agent-after-edit-format-check, and pre-push-production-build belong in existing HOOKS.md; operator enables proposed hooks separately.
- For realworld API work, index hurl-to-bruno.js --check and make bruno-check in realworld/AGENTS.md verification section.
- src/app/shared has two subcomponents only; no local AGENTS.md required unless shared gains a distinct workflow (G2).

## Project context

| Key | Value |
|---|---|
| application | Conduit (RealWorld) Angular SPA |
| language | TypeScript |
| framework | Angular 21 |
| package_manager | Bun |
| entry_point | src/main.ts |
| routing | src/app/app.routes.ts |
| api_client | HttpClient via interceptors in src/app/core; API base configurable; reference https://api.realworld.show/api per realworld/specs/api/openapi.yml |
| test_runner | Vitest (src/**/*.spec.ts, vitest.config.ts) |
| e2e_runner | Playwright (realworld/specs/e2e, playwright.config.ts) |
| setup_hint | Requires Bun; run bun run setup after clone |
| start_hint | bun run start serves at http://localhost:4200 |
| build_hint | bun run build; artifacts in dist/ |
| test_hint | bun run test for unit; bun run test:e2e for conformance E2E; focused E2E per skills/run-focused-e2e-spec/SKILL.md |

## Publication

- Branch: `shipAI` · pushed: after this report
