# INIT report

- Generated: 2026-11-26 23:19 UTC
- Run: `138014d65bc7`
- Repository: https://github.com/shira-ozana/angular-realworld-example-app
- Base commit: `2c8c837809b5877b0f3759a57a454ac52c4b207e` (ref `main`) · branch `shipAI`

## Start here

Requirements and Architect start with these files:

- [AGENTS.md](../../AGENTS.md): Primary entry for agent-assisted work: component map, links to ARCHITECTURE.md and RULES.md, npm/Bun scripts, and pointers to skills under skills/*/SKILL.md plus local realworld/AGENTS.md and src/app/AGENTS.md.
- [ARCHITECTURE.md](../../ARCHITECTURE.md): Describe system components (root toolchain, realworld conformance pack, src/app Angular SPA), entry points, interfaces, dependencies, and data flow with path citations for Requirements and Architect.
- [RULES.md](../../RULES.md): Binding agent constraints for this repo: harness-only edits, preserve human guidance, cite evidence, verification command expectations, and alignment with RealWorld UI/API contracts.

> This repository is an Angular Conduit (RealWorld) single-page application under src/app that implements the social blogging spec against a REST backend. The root uses Bun as the package manager, Angular 21 for the UI, Vitest for unit tests, and Playwright for shared E2E specs vendored from the realworld conformance pack. Structure splits the runnable SPA (src/app) from realworld (OpenAPI, Playwright suite, Bruno/Hurl API tests, and Astro documentation).

## Scan scope

- Files scanned: 175 · components: 13 · analyzed: 13
- Include: all · exclude: none
- Files not sent to the model (context budget): 18
- Files sent truncated: 9

## Harness map

| File | Scope | Purpose | Result |
|---|---|---|---|
| [AGENTS.md](../../AGENTS.md) | Repository root | Primary entry for agent-assisted work: component map, links to ARCHITECTURE.md and RULES.md, npm/Bun scripts, and pointers to skills under skills/*/SKILL.md plus local realworld/AGENTS.md and src/app/AGENTS.md. | updated (replaced the generated block; human content kept) |
| [ARCHITECTURE.md](../../ARCHITECTURE.md) | Repository root | Describe system components (root toolchain, realworld conformance pack, src/app Angular SPA), entry points, interfaces, dependencies, and data flow with path citations for Requirements and Architect. | updated (replaced the generated block; human content kept) |
| [RULES.md](../../RULES.md) | Repository root | Binding agent constraints for this repo: harness-only edits, preserve human guidance, cite evidence, verification command expectations, and alignment with RealWorld UI/API contracts. | updated (replaced the generated block; human content kept) |
| [GUIDELINES.md](../../GUIDELINES.md) | Repository root | Document multiple valid patterns where evidence shows branches: E2E BROWSER_API vs EXTERNAL_API (realworld/specs/e2e/helpers/config.ts), shared Playwright specs vs local Vitest, and Angular feature layout under src/app. | updated (replaced the generated block; human content kept) |
| [CONTRACTS.md](../../CONTRACTS.md) | Repository root | Summarize REST contract (OpenAPI) and frontend selector/routing contract for Conduit conformance; link to canonical files rather than duplicating schemas. | updated (replaced the generated block; human content kept) |
| [DOMAIN.md](../../DOMAIN.md) | Repository root | RealWorld / Conduit business vocabulary (articles, profiles, favorites, feed, tags) for Requirements agents. | kept |
| [TESTING.md](../../TESTING.md) | Repository root | Verification commands and when to use them: bun run test (Vitest), test:e2e, test:e2e:security, format:check, build; link to skills and note CI coverage gaps. | updated (replaced the generated block; human content kept) |
| [realworld/AGENTS.md](../../realworld/AGENTS.md) | realworld | Local contract for the conformance pack: docs dev, API tests (Bruno/Hurl), bruno-check, E2E spec layout; when to read SELECTORS.md and skills run-realworld-docs-dev. | updated (replaced the generated block; human content kept) |
| [src/app/AGENTS.md](../../src/app/AGENTS.md) | src/app | Angular SPA local guidance: routing, features (article, profile, settings), core auth/interceptors, unit test locations, and conformance checks via shared Playwright suite. | updated (replaced the generated block; human content kept) |
| [skills/run-vitest-unit-tests/SKILL.md](../../skills/run-vitest-unit-tests/SKILL.md) | src/app/**/*.spec.ts, package.json, vitest.config.ts | Skill: Run Angular service and component unit tests under src/app with Vitest from the repository root. | updated (replaced the generated block; human content kept) |
| [skills/run-realworld-docs-dev/SKILL.md](../../skills/run-realworld-docs-dev/SKILL.md) | realworld/docs, realworld/docs/package.json, realworld/docs/astro.config.mjs | Skill: Start the Starlight documentation site for RealWorld specifications and community content in realworld/docs. | updated (replaced the generated block; human content kept) |
| [skills/run-playwright-e2e-tests/SKILL.md](../../skills/run-playwright-e2e-tests/SKILL.md) | realworld/specs/e2e, playwright.config.ts, package.json | Skill: Run the shared RealWorld Playwright suite against the SPA implementation, excluding tests tagged @security. | updated (replaced the generated block; human content kept) |
| [skills/run-playwright-security-e2e-tests/SKILL.md](../../skills/run-playwright-security-e2e-tests/SKILL.md) | realworld/specs/e2e, package.json | Skill: Run only Playwright specs tagged @security (for example xss-security.spec.ts). | updated (replaced the generated block; human content kept) |
| [skills/add-e2e-domain-spec/SKILL.md](../../skills/add-e2e-domain-spec/SKILL.md) | realworld/specs/e2e/*.spec.ts, realworld/specs/e2e/helpers, realworld/specs/e2e/SELECTORS.md | Skill: Add or extend end-to-end coverage for a Conduit feature area (articles, authentication, comments) using shared helpers a | updated (replaced the generated block; human content kept) |
| [skills/add-spa-route-mock-test/SKILL.md](../../skills/add-spa-route-mock-test/SKILL.md) | realworld/specs/e2e/articles.spec.ts, realworld/specs/e2e/comments.spec.ts, realworld/specs/e2e/helpers/config.ts | Skill: Verify the frontend treats any 2xx DELETE response as success by mocking the browser response while still hitting the re | updated (replaced the generated block; human content kept) |
| [skills/add-e2e-api-error-test/SKILL.md](../../skills/add-e2e-api-error-test/SKILL.md) | realworld/specs/e2e/error-handling.spec.ts, realworld/specs/e2e/helpers/config.ts | Skill: Add Playwright cases that assert the SPA shows .error-messages and remains usable when API returns 400, 401, 403, 404, o | created |
| [skills/add-e2e-navigation-social-spec/SKILL.md](../../skills/add-e2e-navigation-social-spec/SKILL.md) | realworld/specs/e2e/navigation.spec.ts, realworld/specs/e2e/social.spec.ts, realworld/specs/e2e/settings.spec.ts, realworld/specs/e2e/helpers/api.ts, realworld/specs/e2e/helpers/setup.ts, realworld/specs/e2e/helpers/profile.ts | Skill: Add E2E tests for feeds, tag filters, pagination, follow/unfollow, and settings flows that branch on EXTERNAL_API vs UI  | created |
| [skills/run-hurl-api-tests/SKILL.md](../../skills/run-hurl-api-tests/SKILL.md) | realworld/specs/api/run-api-tests-hurl.sh, realworld/specs/api/hurl, realworld/specs/api/openapi.yml | Skill: Verify a Conduit REST backend against the canonical Hurl suite in realworld/specs/api/hurl. | created |
| [skills/run-bruno-api-tests/SKILL.md](../../skills/run-bruno-api-tests/SKILL.md) | realworld/specs/api/run-api-tests-bruno.sh, realworld/specs/api/bruno | Skill: Run the generated Bruno API collection against a configurable Conduit backend host. | created |
| [skills/check-bruno-hurl-sync/SKILL.md](../../skills/check-bruno-hurl-sync/SKILL.md) | realworld/specs/api/hurl-to-bruno.js, realworld/specs/api/bruno, realworld/specs/api/hurl, realworld/Makefile | Skill: Regenerate or verify the Bruno collection stays synchronized with Hurl sources before commit or in CI. | created |
| [skills/run-playwright-single-spec/SKILL.md](../../skills/run-playwright-single-spec/SKILL.md) | realworld/specs/e2e, package.json | Skill: Run one Playwright spec file or a filtered subset during iterative E2E development. | created |
| [HOOKS.md](../../HOOKS.md) | repository | Active and proposed hooks, verification commands | updated (replaced the generated block; human content kept) |

## Files written

Markdown files created or updated: **21** (this report is not counted).

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
│   ├── add-e2e-api-error-test/
│   │   └── SKILL.md
│   ├── add-e2e-domain-spec/
│   │   └── SKILL.md
│   ├── add-e2e-navigation-social-spec/
│   │   └── SKILL.md
│   ├── add-spa-route-mock-test/
│   │   └── SKILL.md
│   ├── check-bruno-hurl-sync/
│   │   └── SKILL.md
│   ├── run-bruno-api-tests/
│   │   └── SKILL.md
│   ├── run-hurl-api-tests/
│   │   └── SKILL.md
│   ├── run-playwright-e2e-tests/
│   │   └── SKILL.md
│   ├── run-playwright-security-e2e-tests/
│   │   └── SKILL.md
│   ├── run-playwright-single-spec/
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

- [run-vitest-unit-tests](../../skills/run-vitest-unit-tests/SKILL.md) (local): Run Angular service and component unit tests under src/app with Vitest from the repository root.
- [run-realworld-docs-dev](../../skills/run-realworld-docs-dev/SKILL.md) (local): Start the Starlight documentation site for RealWorld specifications and community content in realworld/docs.
- [run-playwright-e2e-tests](../../skills/run-playwright-e2e-tests/SKILL.md) (local): Run the shared RealWorld Playwright suite against the SPA implementation, excluding tests tagged @security.
- [run-playwright-security-e2e-tests](../../skills/run-playwright-security-e2e-tests/SKILL.md) (local): Run only Playwright specs tagged @security (for example xss-security.spec.ts).
- [add-e2e-domain-spec](../../skills/add-e2e-domain-spec/SKILL.md) (local): Add or extend end-to-end coverage for a Conduit feature area (articles, authentication, comments) using shared helpers and SELECTORS.md contracts.
- [add-spa-route-mock-test](../../skills/add-spa-route-mock-test/SKILL.md) (local): Verify the frontend treats any 2xx DELETE response as success by mocking the browser response while still hitting the real backend (BROWSER_API mode only).
- [add-e2e-api-error-test](../../skills/add-e2e-api-error-test/SKILL.md) (local): Add Playwright cases that assert the SPA shows .error-messages and remains usable when API returns 400, 401, 403, 404, or malformed JSON via page.route() (BROWSER_API mode).
- [add-e2e-navigation-social-spec](../../skills/add-e2e-navigation-social-spec/SKILL.md) (local): Add E2E tests for feeds, tag filters, pagination, follow/unfollow, and settings flows that branch on EXTERNAL_API vs UI or setup helpers.
- [run-hurl-api-tests](../../skills/run-hurl-api-tests/SKILL.md) (local): Verify a Conduit REST backend against the canonical Hurl suite in realworld/specs/api/hurl.
- [run-bruno-api-tests](../../skills/run-bruno-api-tests/SKILL.md) (local): Run the generated Bruno API collection against a configurable Conduit backend host.
- [check-bruno-hurl-sync](../../skills/check-bruno-hurl-sync/SKILL.md) (local): Regenerate or verify the Bruno collection stays synchronized with Hurl sources before commit or in CI.
- [run-playwright-single-spec](../../skills/run-playwright-single-spec/SKILL.md) (local): Run one Playwright spec file or a filtered subset during iterative E2E development.
- `add-vitest-service-spec` (needs evidence): missing No Vitest spec file excerpt in evidence for step-by-step structure (imports, providers, assertions)., vitest.config.ts path and focused-test CLI conventions not quoted in inventory.

## Hooks

| Hook | Status | Trigger | Command | Failure behavior |
|---|---|---|---|---|
| husky-pre-commit-lint-staged | active | pre-commit | `npx lint-staged` | block |
| pre-push-format-check | proposed | pre-push | `bun run format:check` | block |
| pre-push-unit-tests | proposed | pre-push | `bun run test` | block |
| agent-after-edit-format-check | proposed | agent: after edit | `bun run format:check` | report |

## Commands

| Command | Status | Source |
|---|---|---|
| `bun run format:check` | documented | `package.json, .github/workflows/lint.yml` |
| `bun run test` | documented | `package.json` |
| `bun run test:coverage` | documented | `package.json` |
| `bun run build` | documented | `package.json, .github/workflows/deploy.yml` |
| `bun run test:e2e` | documented | `package.json, .github/workflows/playwright.yml` |
| `bun run test:e2e:security` | documented | `package.json, .github/workflows/security-tests.yml` |
| `bun run setup` | documented | `README.md, package.json` |

## ASD-STE100

- Architecture prose was written with ASD-STE100 Issue 9 descriptive writing rules in the prompt.
- Automated check: sentence length (max 25 words) on ARCHITECTURE.md, realworld/AGENTS.md, src/app/AGENTS.md: 2 long sentence(s).
- A separate standards conformance review was **not** performed.
  - `src/app/AGENTS.md`: 32 words: It defines the root shell (X), routing in app.routes.ts, HTTP interceptors and auth bootst...
  - `src/app/AGENTS.md`: 33 words: Routes from app.routes.ts: X and X → home; X, X → auth (guest-only); X → settings (X); X →...

## RAG alert

- **Affected scope:** .github, realworld, realworld/specs/api, realworld/specs/e2e, skills, src/app
- **Reason:** evidence the model asked for stayed outside the context budget after the split by component; Conduit conformance is spread across OpenAPI, SELECTORS.md, Playwright helpers, and Angular feature folders; post-split harness files reduce duplication but agents still need retrieval for selector contracts, API shapes, and test-mode flags.
- **Missing for:** Requirements, Architect
- **Index or provide:** realworld/specs/e2e/helpers/setup.ts — global E2E setup (excluded file) for Architect, realworld/specs/e2e/helpers/debug.ts — Requirements: ConduitDebug implementation contract for SPA., realworld/specs/e2e/helpers/setup.ts — Architect: global test setup and storageState., realworld/specs/e2e/url-navigation.spec.ts, realworld/specs/e2e/user-fetch-errors.spec.ts, realworld/specs/e2e/xss-security.spec.ts, realworld/specs/e2e/helpers/debug.ts, realworld/specs/e2e/helpers/profile.ts, realworld/specs/e2e/helpers/setup.ts, skills/run-playwright-e2e-tests/SKILL.md, realworld/specs/e2e/helpers/profile.ts for E2E contracts aligned with this UI, .github/workflows/deploy.yml — deploy entry and artifacts, realworld/specs/e2e/SELECTORS.md, realworld/specs/api/openapi.yml, realworld/specs/e2e/helpers/config.ts, realworld/specs/e2e/helpers/api.ts, realworld/specs/e2e/helpers/auth.ts, realworld/specs/e2e/helpers/articles.ts, realworld/specs/e2e/error-handling.spec.ts
- The run continued with the available evidence. Building an index is the operator's decision.


## Failures, conflicts and limits

- Coverage gap: realworld: Part 1/3 excludes realworld/specs/e2e/url-navigation.spec.ts, user-fetch-errors.spec.ts, xss-security.spec.ts and helpers debug.ts, profile.ts, setup.ts — E2E behavior and setup flow not fully evidenced here.
- Coverage gap: realworld: realworld/specs/api/openapi.yml excerpt is truncated; remaining paths (favorites, tags, delete comment) and full response schemas not shown in evidence.
- Coverage gap: realworld: realworld/Makefile targets beyond bruno-check (e.g. hurl, bruno generation) not quoted in evidence.
- Coverage gap: realworld: realworld/specs/api/hurl-to-bruno.js and Bruno collection layout under realworld/specs/api/bruno/ not included in evidence blocks.
- Coverage gap: realworld: realworld/specs/e2e/playwright.base.ts and SELECTORS.md not in evidence — Playwright base URL and selector contract gaps for Architect.
- Coverage gap: realworld: realworld/AGENTS.md, realworld/README.md, realworld/CONTRIBUTING.md listed in inventory but body not supplied in evidence.
- Coverage gap: realworld: Deploy workflow paths reference docs/** at repo root in deploy-docs.yml while inventory places docs under realworld/docs — workflow path alignment unclear without full monorepo layout evidence.
- Coverage gap: realworld: Evidence for part 2/3 does not include OpenAPI endpoint definitions (realworld/specs/api/openapi.yml content).
- Coverage gap: realworld: E2E specs url-navigation, user-fetch-errors, xss-security and helpers debug.ts, profile.ts, setup.ts were excluded from all analysis parts per caller list.
- Coverage gap: realworld: playwright.base.ts, Makefile targets, and shell wrappers run-api-tests-bruno.sh / run-api-tests-hurl.sh are listed in inventory but not excerpted.
- Coverage gap: realworld: realworld/assets/generator and theme/styles.css behavior not shown in evidence blocks.
- Coverage gap: realworld: Astro content pages under realworld/docs/src/content not excerpted; docs information architecture is inventory-only.
- Coverage gap: realworld: No source excerpts for `realworld/specs/e2e/url-navigation.spec.ts`, `user-fetch-errors.spec.ts`, or `xss-security.spec.ts` in this part.
- Coverage gap: realworld: No source for `realworld/specs/e2e/helpers/debug.ts`, `profile.ts`, or `setup.ts` despite references from settings, social, and navigation specs.
- Coverage gap: realworld: Full root `playwright.config.ts` merge with `baseConfig`, `baseURL`, and `webServer` command not shown in evidence.
- Coverage gap: realworld: OpenAPI, Bruno/Hurl API test runners, and Astro docs behavior not covered in part 3 evidence.
- Coverage gap: realworld: Truncated middle of `error-handling.spec.ts` hides complete 403 comment-delete and additional forbidden-case assertions.
- Coverage gap: src/app/features/article: Exact route paths and lazy-load wiring for HomeComponent, ArticleComponent, and EditorComponent in src/app/app.routes.ts are not evidenced in this part.
- Coverage gap: src/app/features/article: No page-level Vitest or Playwright tests for article components appear in the supplied excerpts (only ArticlesService and CommentsService unit specs).
- Coverage gap: src/app/features/article: Profile-scoped list configs (author or favorited filters on ArticleListConfig) are defined in the model but no page in this evidence passes those filters.
- Coverage gap: src/app/features/article: Error interceptor shape for err.errors versus err in editor submit versus article load is not documented in feature code.
- Coverage gap: src/app/features/article: tags.service.spec.ts is listed in inventory but not included in evidence.
- Coverage gap: src/app/features/article: tags.service.ts implementation (mapping operators, providedIn, error mapping) is not in the part 2 evidence block.
- Coverage gap: src/app/features/article: No excerpt shows which article pages or components inject TagsService or bind tags to the template.
- Coverage gap: src/app/features/article: ArticlesService, CommentsService, and article route components are not excerpted in part 2.
- Coverage gap: src/app/features/article: Relationship between tag list and ArticleListConfig / home feed filters is not documented in supplied excerpts.
- Coverage gap: src/app/features/profile: No excerpt for how profile.routes.ts is imported or path prefix in src/app/app.routes.ts
- Coverage gap: src/app/features/profile: No component-level unit tests for ProfileComponent, FollowButtonComponent, ProfileArticlesComponent, or ProfileFavoritesComponent in inventory
- Coverage gap: src/app/features/profile: ArticleListComponent internal HTTP behavior for author and favorited filters not shown in profile excerpts
- Coverage gap: src/app/features/profile: Duplicate FollowButtonComponent entry in ProfileComponent imports array in source may affect build; not validated in evidence

## Recommendations

- Link HOOKS.md from AGENTS.md after the caller renders hooks; active husky pre-commit uses npx lint-staged but lint-staged path rules are not evidenced—document them in HOOKS.md or package.json when found.
- Consider gating bun run test in CI; automation notes Vitest is documented locally but no workflow in supplied evidence runs unit tests.
- Render skills/add-e2e-api-error-test/SKILL.md from the truncated skill draft in analysis if that workflow is in scope; it is not in the existing harness skills list.
- Preserve CLAUDE.md and realworld/CLAUDE.md as human-authored companions; AGENTS.md should link with one-line summaries per G3.

## Project context

| Key | Value |
|---|---|
| application | Conduit (RealWorld) social blogging SPA |
| language | TypeScript |
| framework | Angular 21 |
| package_manager | Bun |
| entry_point | src/main.ts |
| routing | src/app/app.routes.ts |
| api_client | Angular HttpClient with token, API, and error interceptors under src/app/core/interceptors |
| test_runner | Vitest (src/**/*.spec.ts, vitest.config.ts) |
| e2e_runner | Playwright (realworld/specs/e2e, root playwright.config.ts) |
| setup_hint | Requires Bun; run bun run setup after clone (README.md) |
| start_hint | bun run start; dev URL http://localhost:4200 (playwright.config.ts) |
| build_hint | bun run build; output dist/angular-conduit (angular.json) |
| test_hint | bun run test for unit; bun run test:e2e for conformance E2E (TESTING.md, AGENTS.md) |
| conformance_pack | realworld/ (OpenAPI, shared E2E, docs, API runners) |
| agent_entry | AGENTS.md |
| node_engine | >=20.11.1 (package.json engines) |

## Publication

- Branch: `shipAI` · pushed: after this report
