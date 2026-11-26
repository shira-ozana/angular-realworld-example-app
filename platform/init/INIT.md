# INIT report

- Generated: 2026-11-26 23:12 UTC
- Run: `0ce8a1a3c5af`
- Repository: https://github.com/shira-ozana/angular-realworld-example-app
- Base commit: `2c8c837809b5877b0f3759a57a454ac52c4b207e` (ref `main`) · branch `shipAI`

## Start here

Requirements and Architect start with these files:

- [AGENTS.md](../../AGENTS.md): Primary entry for agent-assisted work: component map (root SPA, realworld conformance pack), links to CLAUDE.md and human guidance, verification commands (format, Vitest, Playwright, build), and pointers to local AGENTS.md and skills.
- [ARCHITECTURE.md](../../ARCHITECTURE.md): System map: Angular implementation under src/app as system under test; realworld tree for OpenAPI, Bruno/Hurl contract tests, shared Playwright E2E, Astro docs, and assets; data flow from SPA to API_BASE and test mode flags.
- [RULES.md](../../RULES.md): Binding agent rules: cite evidence paths, do not change application code when planning harness work, preserve CLAUDE.md and realworld contributor guidance, match existing conventions in src/app and realworld/specs/e2e.

## Scan scope

- Files scanned: 159 · components: 13 · analyzed: 13
- Include: all · exclude: none
- Files not sent to the model (context budget): 6
- Files sent truncated: 9

## Harness map

| File | Scope | Purpose | Result |
|---|---|---|---|
| [AGENTS.md](../../AGENTS.md) | Repository root | Primary entry for agent-assisted work: component map (root SPA, realworld conformance pack), links to CLAUDE.md and human guidance, verification commands (format, Vitest, Playwright, build), and pointers to local AGENTS.md and skills. | created |
| [ARCHITECTURE.md](../../ARCHITECTURE.md) | Repository root | System map: Angular implementation under src/app as system under test; realworld tree for OpenAPI, Bruno/Hurl contract tests, shared Playwright E2E, Astro docs, and assets; data flow from SPA to API_BASE and test mode flags. | created |
| [RULES.md](../../RULES.md) | Repository root | Binding agent rules: cite evidence paths, do not change application code when planning harness work, preserve CLAUDE.md and realworld contributor guidance, match existing conventions in src/app and realworld/specs/e2e. | created |
| [GUIDELINES.md](../../GUIDELINES.md) | Repository root | Document multiple valid patterns: E2E gating via TEST_MODE, BROWSER_API, and EXTERNAL_API; non-security vs @security Playwright runs; API verification via Bruno vs Hurl; Prettier and lint-staged on commit. | created |
| [TESTING.md](../../TESTING.md) | Repository root | Consolidate verification workflows: bun run test (Vitest), test:e2e and test:e2e:security, production build; link skills run-playwright-e2e-tests, run-vitest-unit-tests, and realworld API/doc skills without duplicating SELECTORS.md. | created |
| [DOMAIN.md](../../DOMAIN.md) | Repository root | Conduit/RealWorld vocabulary for Requirements and Architect: articles, slugs, favorites, profiles, follow, jwtToken, Global Feed vs Your Feed, aligned with docs and E2E flows. | created |
| [CONTRACTS.md](../../CONTRACTS.md) | Repository root | Index REST and UI contracts: OpenAPI base and Token auth, SPA routes and DOM selectors, localStorage jwtToken and window.__conduit_debug__; point implementers to canonical files under realworld/specs. | created |
| [realworld/AGENTS.md](../../realworld/AGENTS.md) | realworld | Local contract for the conformance pack: docs dev/build, API Bruno and Hurl runners, hurl-to-bruno check, E2E spec layout and helpers; link realworld/CLAUDE.md and CONTRIBUTING.md; skills run-realworld-docs-dev, run-api-contract-tests-bruno, add-e2e-domain-spec. | created |
| [src/app/AGENTS.md](../../src/app/AGENTS.md) | src/app | Angular implementation guidance: routes and features (article, profile, settings), colocated Vitest specs, compliance with realworld/specs/e2e/SELECTORS.md; skill run-vitest-unit-tests and run-playwright-e2e-tests for verification. | created |
| [skills/run-playwright-e2e-tests/SKILL.md](../../skills/run-playwright-e2e-tests/SKILL.md) | realworld/specs/e2e, playwright.config.ts, package.json | Skill: Run the shared RealWorld Playwright suite against the SPA implementation, excluding tests tagged for security-only runs. | created |
| [skills/run-playwright-security-e2e-tests/SKILL.md](../../skills/run-playwright-security-e2e-tests/SKILL.md) | realworld/specs/e2e, package.json | Skill: Run only Playwright specs tagged @security (for example xss-security.spec.ts in the test inventory). | created |
| [skills/add-e2e-domain-spec/SKILL.md](../../skills/add-e2e-domain-spec/SKILL.md) | realworld/specs/e2e/*.spec.ts, realworld/specs/e2e/helpers, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend end-to-end coverage for a Conduit feature area (articles, authentication, comments) using shared helpers a | created |
| [skills/add-spa-route-mock-test/SKILL.md](../../skills/add-spa-route-mock-test/SKILL.md) | realworld/specs/e2e/articles.spec.ts, realworld/specs/e2e/comments.spec.ts, realworld/specs/e2e/helpers/config.ts | Skill: Verify the frontend treats any 2xx DELETE response as success by mocking the browser response while still hitting the re | created |
| [skills/run-vitest-unit-tests/SKILL.md](../../skills/run-vitest-unit-tests/SKILL.md) | src/app, package.json | Skill: Run Angular service unit tests colocated under src/app (auth, article, profile services). | created |
| [skills/run-realworld-docs-dev/SKILL.md](../../skills/run-realworld-docs-dev/SKILL.md) | realworld/docs | Skill: Preview or edit the RealWorld Starlight documentation site under realworld/docs. | created |
| [HOOKS.md](../../HOOKS.md) | repository | Active and proposed hooks, verification commands | created |

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
│   └── AGENTS.md
├── skills/
│   ├── add-e2e-domain-spec/
│   │   └── SKILL.md
│   ├── add-spa-route-mock-test/
│   │   └── SKILL.md
│   ├── run-playwright-e2e-tests/
│   │   └── SKILL.md
│   ├── run-playwright-security-e2e-tests/
│   │   └── SKILL.md
│   ├── run-realworld-docs-dev/
│   │   └── SKILL.md
│   └── run-vitest-unit-tests/
│       └── SKILL.md
└── src/
    └── app/
        └── AGENTS.md
```

## Skills

- [run-playwright-e2e-tests](../../skills/run-playwright-e2e-tests/SKILL.md) (local): Run the shared RealWorld Playwright suite against the SPA implementation, excluding tests tagged for security-only runs.
- [run-playwright-security-e2e-tests](../../skills/run-playwright-security-e2e-tests/SKILL.md) (local): Run only Playwright specs tagged @security (for example xss-security.spec.ts in the test inventory).
- [add-e2e-domain-spec](../../skills/add-e2e-domain-spec/SKILL.md) (local): Add or extend end-to-end coverage for a Conduit feature area (articles, authentication, comments) using shared helpers and SELECTORS.md contracts.
- [add-spa-route-mock-test](../../skills/add-spa-route-mock-test/SKILL.md) (local): Verify the frontend treats any 2xx DELETE response as success by mocking the browser response while still hitting the real backend (BROWSER_API mode only).
- [run-vitest-unit-tests](../../skills/run-vitest-unit-tests/SKILL.md) (local): Run Angular service unit tests colocated under src/app (auth, article, profile services).
- [run-realworld-docs-dev](../../skills/run-realworld-docs-dev/SKILL.md) (local): Preview or edit the RealWorld Starlight documentation site under realworld/docs.
- `run-api-contract-tests-bruno` (needs evidence): missing realworld/specs/api/run-api-tests-bruno.sh full script, realworld/specs/api/README.md operator instructions, realworld/Makefile API test targets
- `run-api-contract-tests-hurl` (needs evidence): missing Sample .hurl file contents, realworld/specs/api/run-api-tests-hurl.sh full script
- `sync-hurl-to-bruno` (needs evidence): missing realworld/specs/api/hurl-to-bruno.js full generate and --check implementation, realworld/Makefile bruno-check target
- `add-e2e-helper-module` (needs evidence): missing realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/articles.ts, realworld/specs/e2e/helpers/comments.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/debug.ts
- `add-angular-service-unit-test` (needs evidence): missing Excerpt of any src/app/**/*.service.spec.ts showing imports, TestBed, and assertion style, Vitest config file path and Angular test setup
- `implement-conduit-debug-interface` (needs evidence): missing realworld/specs/e2e/helpers/debug.ts, Application source that sets window.__conduit_debug__

## Hooks

| Hook | Status | Trigger | Command | Failure behavior |
|---|---|---|---|---|
| husky-pre-commit | active | pre-commit | `npx lint-staged` | block |
| pre-push-unit-tests | proposed | pre-push | `bun run test` | block |
| pre-push-format-check | proposed | pre-push | `bun run format:check` | block |
| agent-after-edit-format | proposed | agent: after edit | `bun run format:check` | report |

## Commands

| Command | Status | Source |
|---|---|---|
| `bun run format:check` | documented | `package.json, .github/workflows/lint.yml` |
| `bun run test` | documented | `package.json` |
| `bun run test:coverage` | documented | `package.json` |
| `bun run test:e2e` | documented | `package.json, .github/workflows/playwright.yml` |
| `bun run test:e2e:security` | documented | `package.json, .github/workflows/security-tests.yml` |
| `bun run build` | documented | `package.json, .github/workflows/deploy.yml` |

## ASD-STE100

- Architecture prose was written with ASD-STE100 Issue 9 descriptive writing rules in the prompt.
- Automated check: sentence length (max 25 words) on ARCHITECTURE.md, realworld/AGENTS.md, src/app/AGENTS.md: 2 long sentence(s).
- A separate standards conformance review was **not** performed.
  - `src/app/AGENTS.md`: 32 words: It defines the root shell (X), routing in X, HTTP interceptors and auth bootstrap in X, fe...
  - `src/app/AGENTS.md`: 33 words: Routes from app.routes.ts: X and X → home; X, X → auth (guest-only); X → settings (X); X →...

## RAG alert

- **Affected scope:** realworld, realworld/docs, realworld/specs/api, realworld/specs/e2e, src/app
- **Reason:** evidence the model asked for stayed outside the context budget after the split by component; Conformance knowledge is spread across OpenAPI, SELECTORS.md, many Playwright specs and helpers, Astro docs content, and Bruno/Hurl assets; component split in ARCHITECTURE.md and CONTRACTS.md reduces but does not replace retrieval for endpoint-level and selector-level edits.
- **Missing for:** Requirements, Architect
- **Index or provide:** realworld/specs/e2e/helpers/debug.ts for ConduitDebug contract, realworld/specs/e2e/helpers/setup.ts and profile.ts for test lifecycle and profile flows, realworld/specs/e2e/url-navigation.spec.ts, realworld/specs/e2e/user-fetch-errors.spec.ts, realworld/specs/e2e/xss-security.spec.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/api/openapi.yml, realworld/specs/e2e/SELECTORS.md, realworld/specs/e2e/helpers/*.ts, realworld/docs/src/content/docs, realworld/README.md, realworld/CONTRIBUTING.md
- The run continued with the available evidence. Building an index is the operator's decision.


## Failures, conflicts and limits

- Conflict (needs a decision): realworld/.github/workflows/deploy-docs.yml references working-directory ./docs and artifact path ./docs/dist while the inventory places documentation at realworld/docs; monorepo checkout layout vs workflow paths needs human alignment (analysis coverage_gaps).
- Conflict (needs a decision): Root CI (.github/workflows/lint.yml, playwright.yml) targets the Angular repo root while realworld/.github/workflows (bruno-check, deploy-docs, codeql) target the realworld subtree; agents must not assume a single CI root without checking which tree changed.
- Coverage gap: realworld: realworld/Makefile targets and bruno-check implementation are not excerpted; only the workflow reference exists.
- Coverage gap: realworld: realworld/specs/api/bruno collection layout, bruno.json, and hurl-to-bruno.js behavior are not in evidence.
- Coverage gap: realworld: realworld/CLAUDE.md, realworld/CONTRIBUTING.md, and realworld/README.md content not supplied for part 1.
- Coverage gap: realworld: realworld/specs/e2e/* and listed helper files intentionally excluded from all parts; Playwright e2e architecture belongs to other component parts.
- Coverage gap: realworld: deploy-docs.yml uses working-directory ./docs and path ./docs/dist while inventory places docs at realworld/docs; monorepo versus subtree checkout alignment unclear.
- Coverage gap: realworld: Full openapi.yml paths and schemas are truncated; favorites and tags endpoints may exist beyond excerpt.
- Coverage gap: realworld: realworld/specs/api/README.md not excerpted; operator instructions for API tests unverified.
- Coverage gap: realworld: realworld/specs/e2e/url-navigation.spec.ts not included in any analysis part
- Coverage gap: realworld: realworld/specs/e2e/user-fetch-errors.spec.ts not included
- Coverage gap: realworld: realworld/specs/e2e/xss-security.spec.ts not included
- Coverage gap: realworld: realworld/specs/e2e/helpers/debug.ts not included (ConduitDebug implementation detail)
- Coverage gap: realworld: realworld/specs/e2e/helpers/profile.ts and setup.ts not included
- Coverage gap: realworld: Full hurl-to-bruno.js generateBruFile and assert translation logic truncated in evidence
- Coverage gap: realworld: Hurl .hurl file contents and openapi.yml operations not excerpted in this part
- Coverage gap: realworld: realworld/docs content structure and Astro routing not excerpted in this part
- Coverage gap: realworld: realworld/assets/generator/generate_assets.py behavior not excerpted
- Coverage gap: realworld: Relationship between root .github/workflows/playwright.yml and realworld/specs/e2e path configuration not shown in excerpts
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/url-navigation.spec.ts (URL routing edge cases).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/user-fetch-errors.spec.ts (401 on page load; referenced from error-handling.spec.ts).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/xss-security.spec.ts (security-tagged Playwright suite).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/helpers/config.ts (definition of BROWSER_API and EXTERNAL_API).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/helpers/debug.ts (getToken, getCurrentUser implementation).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/helpers/profile.ts (followUser, unfollowUser, updateProfile).
- Coverage gap: realworld: No source excerpt for realworld/specs/e2e/helpers/setup.ts (createUserInIsolation, createManyArticles).
- Coverage gap: realworld: Part 3 does not include e2e specs from earlier parts: articles.spec.ts, auth.spec.ts, comments.spec.ts, error-handling full file tail, and root playwright.config.ts merge with baseConfig.
- Coverage gap: src/app/features/article: Exact route paths and lazy-load structure for home, article, editor, and /tag/:tag are not confirmed without src/app/app.routes.ts excerpt.
- Coverage gap: src/app/features/article: HTTP interceptors (API base URL, error shape for err.errors) are not shown in supplied excerpts.
- Coverage gap: src/app/features/article: tags.service.spec.ts content and any article-specific route guards are not in evidence.
- Coverage gap: src/app/features/article: Whether profile favorites use ArticleListConfig.filters.favorited is not shown in provided page excerpts (filter exists on model and ArticlesService only).
- Coverage gap: src/app/features/article: tags.service.ts implementation source not included in part 2 evidence; behavior inferred from tags.service.spec.ts.
- llm (error): overview analysis failed: Timed out waiting for bridge discovery

## Recommendations

- Link HOOKS.md (caller-rendered) from AGENTS.md: active husky pre-commit lint-staged; proposed pre-push test and format:check hooks from automation evidence.
- Complete run-api-contract-tests-bruno skill evidence by excerpting realworld/specs/api/run-api-tests-bruno.sh and realworld/Makefile bruno-check target before agents rely on HOST defaults.
- Document in TESTING.md that CI runs format:check, test:e2e, test:e2e:security, and build; Vitest (bun run test) is documented in package.json but not shown in supplied workflow excerpts (inferred gap).
- When editing E2E specs, require reading realworld/specs/e2e/SELECTORS.md and helpers/config.ts for BROWSER_API and EXTERNAL_API gates.
- Preserve realworld/CLAUDE.md and realworld/CONTRIBUTING.md as authoritative for upstream RealWorld contributions; root CLAUDE.md for this implementation fork.

## Publication

- Branch: `shipAI` · pushed: after this report
