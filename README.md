# Checkpoint Defence

This document provides a *framework* on which I build my checkpoint reviews for the fellows at Andela. This document applies
to a very narrow subset of projects -  Javascript projects built with Node and React/Angular.

## System Functions

### To Meet Expectation
> * The application (both server and client sides) should be working.
> * The application should implement all server and client side requirements.
> * The application should not throw console errors.
> * The application should use production build of libraries, frameworks, ... (eg. production build of React, not development)
> * The browser page should not refresh (for single-page applications).

### To Exceed Expectation
> * The application should add more functionality. For instance, the app could have more server endpoints.

## Task Runner

### To Meet Expectation
> * Keep the task runner simple, without unnecessary imports or tasks.
> * There should be at least one form of minification of static content.
> * Set up testing task with code coverage file generator.
> * Set the project up to use ES6+, and transpile back to ES5 using Babel.
> * Set up the project to use ESLint, and ensure it extends `airbnb-base`.
> * Configure continuous integration (CI) to run the required tasks, tests, and then deploy to a cloud-based server. Elements of the CI should include:
>> * Heroku-Github connection
>> * Travis CI
>> * Hound CI
> * Make task runner production-ready.
>> * https://moduscreate.com/blog/optimizing-react-es6-webpack-production-build/
>> * https://webpack.js.org/guides/production/
>> * https://webpack.js.org/configuration/devtool/
>> * Consider having 2 different Webpack configs, one for development and 1 for production. Let this reflect in your npm scripts `start` and `build`.

### To Exceed Expectation
> * Minify all 3 static content types (HTML, CSS, Javascript)
> * Use tasks to automate conversion and the building of Jade, SCSS/SASS, Webpack (for Javascript file importation and concatenation using `require(...)`).

## Project Management and Workflow

### To Meet Expectation
> * Stories should be adequately broken down.
> * Stories should be adequately fleshed out, and in accordance with the appropriate conventions/guidelines.
> * Stories that are marked as done on Pivotal Tracker (PT) should actually be done in the app.
> * All features in the app should be represented on the PT board.
> * The README file should be well prepared. There should also be a “contributing” section.
> * Commit (and PR) messages should be in accordance with the appropriate conventions/guidelines.
> * Do not commit auto-generated files, application settings and secret keys to source control.

## Test Coverage

### To Meet Expectation
> * There should be at least 80% coverage of unit, integration and e2e tests, for both server and client side code.
> * Test coverage should be hooked up with the continuous integration (CI) for deployment.
> * The Test Coverage should report to CodeClimate/Coveralls or other coverage reporters.
> * The necessary badges (TravisCI, CodeClimate, Coveralls) should be visible on the README.

### To Exceed Expectation
> * There should be a test environment setup so no Mocks are used throughout the application's tests.
> * Test Coverage should be at 100% for server and client side tests.

## Code Organisation

### To Meet Expectation
> * Scripts and files should be placed in the appropriate directories.
> * There should be a consistent and effective folder structure.
> * Pascal case (LikeThis) should be used in file and class naming.
> * Camel case (likeThis) should be used in function naming.
> * File and class names must match.
> * Use this as a guide: http://airbnb.io/javascript/#naming-conventions

### To Exceed Expectation
> * All static content reference in HTML should be compressed and minified into one file on deployment.

## Code Quality

### To Meet Expectation
> * Code should be formatted with consistent, logical and easy to read formatting as described in the style guide.
> * Ensure the appropriate HTTP status code is returned for different scenarios.
> * Ensure user inputs are properly validated in both the server and client sides.
> * Ensure there aren't excessive calls to the server or database.

## Comments and Documentation

### To Meet Expectation
> * Comments should be sufficiently present in code.
> * Comments should be concise.
> * Comments should effectively explain the code segments they apply to.
> * JSDoc comments should be properly formatted. See https://github.com/shri/JSDoc-Style-Guide
> * The API should be well documented.
