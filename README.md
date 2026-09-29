# Playwright QA Automation Framework

![Playwright Tests](https://github.com/YOUR-USERNAME/playwright-qa-automation/actions/workflows/playwright.yml/badge.svg)

UI and API test automation built with **Playwright + TypeScript** using the **Page Object Model (POM)**, custom fixtures, and CI through **GitHub Actions**.

## What is tested

| Area | Site | Coverage |
|---|---|---|
| UI | [SauceDemo](https://www.saucedemo.com) (public practice site) | Login (valid, invalid, locked-out, empty fields), inventory sorting, cart add/remove, end-to-end checkout with validation |
| API | [JSONPlaceholder](https://jsonplaceholder.typicode.com) (public fake API) | GET, POST, PUT, DELETE, schema checks, query filtering, negative case (404) |

**21 automated tests**: 14 UI tests across 4 spec files and 7 API tests.

## Framework design

- `pages/` : Page Object classes. Locators and actions live here, tests stay readable.
- `fixtures/` : Custom Playwright fixtures that inject page objects and a pre-logged-in session.
- `test-data/` : Test data kept in JSON, separate from test logic.
- `tests/ui`, `tests/api` : Test specs, separated into two Playwright projects.
- `.github/workflows/` : CI pipeline that runs all tests on every push and uploads the HTML report.

Reports include screenshots and video on failure, and traces on retry.

## Run locally

```bash
npm install
npx playwright install chromium
npm test                # all tests
npm run test:ui         # UI only
npm run test:api        # API only
npm run test:headed     # watch the browser
npm run report          # open the HTML report
```

## Tech stack

Playwright, TypeScript, Node.js, GitHub Actions, JSON test data.

## Author

Deena Nandha Kumar V | QA Engineer | [LinkedIn](https://linkedin.com/in/deena-nandha-kumar-827119185)
