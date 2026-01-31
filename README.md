# IT23225138 – Playwright E2E Tests (SwiftTranslator)

Automated end-to-end tests for the **SwiftTranslator** website (Singlish to Sinhala translation) using Playwright.

---

## Prerequisites

- **Node.js** (LTS recommended) – [https://nodejs.org](https://nodejs.org)
- **npm** (included with Node.js)

---

## 1. Clone the repository

```bash
git clone <https://github.com/nimashkithmal/ITPM_-Assignment_1.git>
cd IT23225138
```


---

## 2. Install dependencies

From the project root:

```bash
npm install
```

This installs Playwright, the test runner, and other dependencies (including `xlsx` for test data).

---

## 3. Install Playwright browsers (first time only)

Playwright needs browser binaries. Install them with:

```bash
npx playwright install
```

On CI/Linux you may need system dependencies:

```bash
npx playwright install --with-deps
```

---

## 4. Run the tests

| Command | Description |
|--------|-------------|
| `npm test` | Run all Playwright tests (headless) |
| `npm run test:swift` | Run only SwiftTranslator tests |
| `npm run test:chromium` | Run tests in Chromium only |
| `npm run test:headed` | Run tests with browser window visible |
| `npm run test:ui` | Open Playwright UI mode for debugging |
| `npm run test:report` | Open the last HTML test report |

**Examples:**

```bash
# Run all tests
npm test

# Run only SwiftTranslator tests
npm run test:swift

# Run with browser visible
npm run test:headed
```

---

## 5. Test data

Test cases are read from:

- **`test_data/IT23225138 .xlsx`**

Ensure this file exists and contains columns such as **TC ID**, **Test case name**, **Input**, and **Expected output** (or **Expected output **). The SwiftTranslator tests are data-driven from this Excel file.

---

## 6. Repository link

The Git repository URL for this project is provided in the file **`REPOSITORY_LINK.txt`** in the project root. The repository must be **publicly accessible** for evaluation.

---

## Project structure

```
IT23225138/
├── .github/workflows/playwright.yml   # CI: run tests on push/PR
├── playwright.config.js              # Playwright configuration
├── package.json                      # Scripts and dependencies
├── README.md                         # This file
├── REPOSITORY_LINK.txt               # Git repository URL
├── test_data/
│   └── IT23225138 .xlsx              # Test cases (Excel)
└── tests/
    ├── example.spec.js               # Example Playwright test
    └── swift-translator-tests.spec.js # SwiftTranslator E2E tests
```
