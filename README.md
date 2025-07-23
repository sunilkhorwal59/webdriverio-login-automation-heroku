# WebdriverIO Login Automation Framework

This project is an automation framework for testing login scenarios on the demo site [the-internet.herokuapp.com](https://the-internet.herokuapp.com/login) using WebdriverIO, Mocha, and Allure reporting.

## Features
- Page Object Model structure
- Valid and invalid login test scenarios
- Allure reporting integration
- Chrome browser automation

## Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- npm (comes with Node.js)
- Google Chrome browser

## Setup
1. **Clone the repository**
   ```sh
   git clone <your-repo-url>
   cd Cursor-Automation-Javascript
   ```
2. **Install dependencies**
   ```sh
   npm install
   ```

## Project Structure
```
Cursor-Automation-Javascript/
├── test/
│   ├── pageobjects/
│   │   ├── login.page.js
│   │   ├── page.js
│   │   └── secure.page.js
│   └── specs/
│       └── test.e2e.js
├── wdio.conf.js
├── package.json
└── README.md
```

## Running Tests
To execute all tests:
```sh
npm run wdio
```

## Test Scenarios
- **Valid Login:**
  - Logs in with correct credentials (`tomsmith` / `SuperSecretPassword!`)
  - Verifies success alert
- **Invalid Login:**
  - Attempts login with wrong credentials
  - Verifies error alert

## Allure Reporting
1. **Run tests to generate Allure results:**
   ```sh
   npm run wdio
   ```
2. **Generate the Allure report:**
   ```sh
   npx allure generate allure-results --clean -o allure-report
   ```
3. **Open the Allure report in your browser:**
   ```sh
   npx allure open allure-report
   ```

## Configuration
- **Test runner:** Mocha
- **Browser:** Chrome (configurable in `wdio.conf.js`)
- **Base URL:** `https://the-internet.herokuapp.com/`
- **Reporters:** Spec, Allure

## Customization
- Add more test scenarios in `test/specs/test.e2e.js`
- Add or modify page objects in `test/pageobjects/`
- Update configuration in `wdio.conf.js`

---

Feel free to contribute or raise issues for improvements! 