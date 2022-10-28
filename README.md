# Cypress Allure Plugin Usage Example

This project demonstrates how to use
(https://github.com/Shelex/cypress-allure-plugin).

## How to run:

-   clone this repo
-   install dependencies: `npm install`
-   run tests: `npm run cy:run`
-   clear previous output `npm run allure:clear`
-   generate allure report: `npm run allure:report`
-   open report: `allure open`


## Commands:
 "cy:open": "npx cypress open --env allure=true --config specPattern=cypress/e2e/examples/** --browser chrome",
        "cy:cucumber:open": "npx cypress open --env allure=true --config specPattern=cypress/e2e/cucumber/*.feature,excludeSpecPattern=*.js --browser chrome",
        "cy:run": "npx cypress run --config specPattern=cypress/e2e/examples/* --env allure=true --browser chrome",
        "cy:cucumber:run": "npx cypress run --config specPattern=cypress/e2e/cucumber/*.feature,excludeSpecPattern=*.js --env allure=true --browser chrome",
        "allure:report": "allure generate allure-results --clean -o allure-report",
        "allure:clear": "rm -r allure-results/ allure-report cypress/screenshots || true",
        "allure:history": "mv -f allure-report/history allure-results/history && rm -r allure-report || true",
        "cypress:run": "npx cypress run --env allure=true ",
        "cy:test": "npx cypress run --env allure=true --config specPattern=cypress/e2e/examples/test.cy.js",
        "cy:cucumber:cucumber": "npx cypress run --config specPattern=cypress/e2e/cucumber/*.feature,excludeSpecPattern=*.js --env allure=true"
