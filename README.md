# E2E test automation portfolio

Public test frameworks by [andepandy](https://github.com/andepandy). Each repository is clone-and-run, with GitHub Actions where the target site or API is still live.

This is the page to share on a CV. GitHub does not group repositories into folders, so this README is the index.

Repo names follow `{stack}-{style}-{target}` so the technology is obvious before you open the project.

## UI end-to-end

| Repository | Stack | Target |
| --- | --- | --- |
| [csharp-reqnroll-selenium-shop](https://github.com/andepandy/csharp-reqnroll-selenium-shop) | C#, Reqnroll (BDD), NUnit, Selenium 4, page objects | [Automation Exercise](https://www.automationexercise.com/) shop: account, basket, category, search, contact |
| [playwright-ts-csharp-shop](https://github.com/andepandy/playwright-ts-csharp-shop) | Playwright TypeScript (fluent API) + Playwright C# (UI) | Same shop journeys over API and UI: products, search, account |
| [cypress-ts-cucumber-duckduckgo](https://github.com/andepandy/cypress-ts-cucumber-duckduckgo) | Cypress, TypeScript, Cucumber | DuckDuckGo search |
| [webdriverio-mocha-sauce-demo](https://github.com/andepandy/webdriverio-mocha-sauce-demo) | WebdriverIO, Mocha | Sauce Demo login and checkout |
| [python-behave-selenium-login](https://github.com/andepandy/python-behave-selenium-login) | Python, Behave (BDD), Selenium 4, page objects | [The Internet](https://the-internet.herokuapp.com/) login (valid + invalid) |
| [csharp-selenium3-specflow-archive](https://github.com/andepandy/csharp-selenium3-specflow-archive) | C#, SpecFlow, Selenium 3 (archive) | Replaced by `csharp-reqnroll-selenium-shop` |

## API and performance

| Repository | Stack | Target |
| --- | --- | --- |
| [cypress-cucumber-docker-users-api](https://github.com/andepandy/cypress-cucumber-docker-users-api) | Cypress, Cucumber, Docker | Public users API: create, list, get, 404 |
| [gatling-maven-docker-users-api](https://github.com/andepandy/gatling-maven-docker-users-api) | Gatling, Maven, Docker | Load test against the same public users API |
| [csharp-specflow-covid-api](https://github.com/andepandy/csharp-specflow-covid-api) | C#, SpecFlow | COVID statistics APIs |

## Take-home tasks

Public demos rewritten without company names.

| Repository | Stack | Target |
| --- | --- | --- |
| [webdriverio-ts-pom-login](https://github.com/andepandy/webdriverio-ts-pom-login) | WebdriverIO 9, TypeScript, Mocha, page objects | [The Internet](https://the-internet.herokuapp.com/) login (valid + invalid) |
| [python-behave-selenium-login](https://github.com/andepandy/python-behave-selenium-login) | Python, Behave, Selenium 4, page objects | Same login target as the WDIO take-home |

## Mobile e2e

| Repository | Stack | Notes |
| --- | --- | --- |
| [detox-typescript-pom-mobile](https://github.com/andepandy/detox-typescript-pom-mobile) | Detox, TypeScript, page objects | Structure template: Matchers / Gestures / Assertions + POM. CI typechecks; no app binary to build. |

## AI SDET

Modern AI-shaped web QA: natural-language intents on Playwright, self-healing locators, optional LLM planning. Same ideas as Stagehand / Midscene, kept clone-and-run without requiring an API key in CI.

| Repository | Stack | Target |
| --- | --- | --- |
| [ai-playwright-web-qa](https://github.com/andepandy/ai-playwright-web-qa) | Playwright, TypeScript, intent agent, self-healing locators | The Internet login + Automation Exercise search via `ai.act(...)` |

## Shared codebases

Product repos worked on jointly. Full collaborator index: [joint-projects](https://github.com/andepandy/joint-projects).

| Repository | Board | Test | Prod |
| --- | --- | --- | --- |
| [car-connect](https://github.com/andepandy/car-connect) | [Issues](https://github.com/andepandy/car-connect/issues) · [Projects](https://github.com/andepandy/car-connect/projects) | Dokploy staging (`Staging` branch; public DNS TBD) | [car-connect.online](https://car-connect.online) (configured; DNS not live yet) |
| [kulimaapp](https://github.com/andepandy/kulimaapp) | [Issues](https://github.com/andepandy/kulimaapp/issues) · [Projects](https://github.com/andepandy/kulimaapp/projects) | — | [kulimaapp.org](https://kulimaapp.org) |
| [fleet-foxx-white](https://github.com/andepandy/fleet-foxx-white) | [Issues](https://github.com/andepandy/fleet-foxx-white/issues) · [Projects](https://github.com/andepandy/fleet-foxx-white/projects) | [staging.fleet-fox.com](https://staging.fleet-fox.com) | [client.fleet-fox.com](https://client.fleet-fox.com) |
| [fleet-fox-web](https://github.com/andepandy/fleet-fox-web) | [Issues](https://github.com/andepandy/fleet-fox-web/issues) · [Projects](https://github.com/andepandy/fleet-fox-web/projects) | — | [fleet-fox.com](https://fleet-fox.com) |

### Mobile e2e open source projects

Contributions to [MetaMask Mobile](https://github.com/MetaMask/metamask-mobile) under [Andepande](https://github.com/Andepande) — Detox-era e2e, API mocking, CI parallelism, and reliability work. The repo has since moved primary smoke coverage toward Appium; the commits below show the Detox and platform work shipped on `main`.

Selected commits:

- [E2E Mocking Setup For Detox Tests](https://github.com/MetaMask/metamask-mobile/commit/2cf43036e96778d1b5a91d01937c984f8a696f11) — Detox API mocking foundation
- [Refining E2E Testing with API Mocking](https://github.com/MetaMask/metamask-mobile/commit/f36d6c91df21ba5a397c94af864122ed5a041b1d) — Mocking refinements for stable e2e
- [Parallel execution support for Android in Bitrise CI](https://github.com/MetaMask/metamask-mobile/commit/dd025c1cfd6f6b409ba34da8b4277239a8fa2e62) — Split smoke across VMs
- [Screenshots on failure implementation](https://github.com/MetaMask/metamask-mobile/commit/c068e9cefe9cdb31887550a1712eab7aea7ea8b9) — Failure artefacts for Detox runs
- [Removing test selector strings within app code](https://github.com/MetaMask/metamask-mobile/commit/89eb8cd63db54ea2ba0efffe948a026989e99aef) — Cleaner testID / selector separation
- [e2e test coverage for solana](https://github.com/MetaMask/metamask-mobile/commit/afd777011c4ca732c3fb6992c56e3d8be4dd72a8) / [snap mobile e2e implementation](https://github.com/MetaMask/metamask-mobile/commit/91a8ce082e25be5e64cd9bb6bb3dcf14caebcaca) — Feature coverage
- [Enable e2e testing for flask builds in CI](https://github.com/MetaMask/metamask-mobile/commit/72e749119b6e255cbddf15c919ac4fc5d8e99b58) — Flask smoke in pipeline

Full history: [commits by Andepande](https://github.com/MetaMask/metamask-mobile/commits/main/?author=Andepande).

## How to review

1. Open **csharp-reqnroll-selenium-shop** for a full BDD UI framework (the Azure DevOps project copied here).
2. Open **playwright-ts-csharp-shop** for fluent Playwright API tests next to the same journeys in Playwright C#.
3. Open **cypress-cucumber-docker-users-api** for API testing in Cypress, including a Dockerfile.
4. Open **gatling-maven-docker-users-api** for Gatling performance tests.
5. Open **detox-typescript-pom-mobile** for mobile Detox + TypeScript page-object structure.
6. Open **ai-playwright-web-qa** for AI-shaped Playwright intents and self-healing locators.
7. Open **webdriverio-ts-pom-login** for a take-home style WDIO + TypeScript login suite.
8. Open **python-behave-selenium-login** for Python Behave + Selenium 4 BDD login tests.
