# Checkpoint Defence

This document provides a *framework* on which I build my checkpoint reviews for the fellows at Andela.

## System Functions

### To Meet Specification
> * The application should implement all server and client side requirements.
> * The application should not throw console errors.
> * The application should use production build of libraries, frameworks, ... (eg. production build of React, not development)
> * The browser page should not refresh (for single-page applications).

### To Exceed Specification
> * The application should add more functionality. For instance, the app could have more server endpoints.

## Task Runner

### To Meet Specification
> * Keep the task runner simple, without unnecessary imports or tasks.
> * There should be at least one form of minification of static content.
> * Set up testing task with code coverage file generator.
> * Set the project up to use ES6+, and transpile back to ES5 using Babel.
> * Set up the project to use ESLint, and ensure it extends `airbnb-base`.
> * Configure continuous integration (CI) to run the required tasks, tests, and then deploy to a cloud-based server.
>> Elements of the CI should include:
>> * Heroku-Github connection
>> * Travis CI
>> * Hound CI
> * Make task runner production-ready.
>> * https://moduscreate.com/blog/optimizing-react-es6-webpack-production-build/
>> * https://webpack.js.org/guides/production/
>> * https://webpack.js.org/configuration/devtool/
>> * Consider having 2 different Webpack configs, one for development and 1 for production. Let this reflect in your npm scripts `start` and `build`.

### To Exceed Specification
> * Minify all 3 static content types (HTML, CSS, Javascript)
> * Use tasks to automate conversion and the building of Jade, SCSS/SASS, Webpack (for Javascript file importation and concatenation using `require(...)`).

## Project Management and Workflow

### To Meet Specification
> * Stories should be adequately broken down.
> * Stories should be adequately fleshed out, and in accordance with the appropriate conventions/guidelines.
> * Stories that are marked as done on Pivotal Tracker (PT) should actually be done in the app.
> * All features in the app should be represented on the PT board.
> * The README file should be well prepared. There should also be a “contributing” section.
> * Commit (and PR) messages should be in accordance with the appropriate conventions/guidelines.

## Test Coverage

### To Meet Specification
> * There should be 80% coverage of unit, integration and e2e tests, for both server and client side code.
> * Test coverage should be hooked up with the continuous integration (CI) for deployment.
> * The Test Coverage should report to CodeClimate/Coveralls or other coverage reporters.
> * The necessary badges (TravisCI, CodeClimate, Coveralls) should be visible on the README.

### To Exceed Specification
> * There should be a test environment setup so no Mocks are used throughout the application's tests.
> * Test Coverage should be at 100% for server and client side tests.
