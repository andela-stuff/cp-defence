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
> * Ensure all endpoints have been implemented, and working as expected.
> * Ensure the endpoints recover gracefully when supplied with invalid data.

### To Exceed Expectation
> * The application should add more functionality. For instance, the app could have more server endpoints.

## Task Runner

### To Meet Expectation
> * Keep the task runner simple, without unnecessary imports or tasks.
> * There should be at least one form of minification of static content.
> * Set up testing task with code coverage file generator.
> * Set the project up to use ES6+, and transpile back to ES5 using Babel.
> * Set up the project to use ESLint, and ensure it extends `airbnb-base` (or `airbnb` for React).
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
> * Pivotal Tracker (PT) board should show relevant chores and bug fixes, not just fixtures. For instance, it should show chores that have to be done to set up the project, as well as bug fixes that may be as a result of facilitator feedback.
> * Stories should be adequately broken down.
> * Stories should be adequately fleshed out, and in accordance with the appropriate conventions/guidelines (including well defined acceptance criteria).
> * Sprints should be of appropriate lengths. See http://www.agileadvice.com/2014/06/12/howtoapplyagile/21-tips-on-choosing-a-sprint-length/
> * Stories that are marked as done on PT should actually be done in the app.
> * All features in the app should be represented on the PT board.
> * The README file should be well prepared.
> * There should also be a “contributing” section in README and/or a CONTRIBUTING.md file. It's a great place to let future contributors know what code, PR, commit message conventions & style guide you're using.
> * You should also work on including sections like "Frequently Asked Questions", "Limitations", "Testing", etc. in README.
> * The README should state a particular license for the project, and there should be LICENSE file with the content of that license.
> * Commit messages, branch names and PRs should be in accordance with the appropriate conventions/guidelines.
> * Do not commit auto-generated files, application settings and secret keys to source control.

### To Exceed Expectation
> * Create a wiki for the project on Github. The wiki can contain the following pages:
>> * Home
>> * Branch Naming Convention
>> * Commit Message Convention
>> * Pull Request Naming and Description Convention

## Test Coverage

### To Meet Expectation
> * There should be at least 80% coverage of unit, integration and e2e tests, for both server and client side code.
> * Test coverage should be hooked up with the continuous integration (CI) for deployment.
> * The Test Coverage should report to CodeClimate/Coveralls or other coverage reporters.
> * The necessary badges (TravisCI, CodeClimate, Coveralls) should be visible on the README.
> * While testing, check for the presence of relevant properties in the JSON returned from the endpoint being tested.
> * While testing, check for the values of relevant properties in the JSON returned from the endpoint being tested.
>> * Where applicable, you may want to compare the values of the properties of the object in the request body to the values of the properties of the object in the response JSON.
>> * Where applicable, you may want to check the length of the array in the response JSON.

### To Exceed Expectation
> * There should be a test environment setup so no Mocks are used throughout the application's tests.
> * Test Coverage should be at 100% for server and client side tests.

## Code Organisation

### To Meet Expectation
> * Scripts and files should be placed in the appropriate directories.
> * There should be a consistent and effective folder structure.
> * Pascal case (LikeThis) should be used in class (and the containing file) naming.
> * Camel case (likeThis) should be used in function naming.
> * Upper snake case (LIKE_THIS) should be used in naming constants.
> * File and class names must match.
> * Models representing singular objects should be named in their singular form. A model representing an employee should be named `Employee`, not `Employees`. See example of [model definitions](http://sequelize.readthedocs.io/en/2.0/docs/models-definition/).
> * Use this as a guide: http://airbnb.io/javascript/#naming-conventions

### To Exceed Expectation
> * All static content reference in HTML should be compressed and minified into one file on deployment.

## Code Quality

### To Meet Expectation
> * Code should be formatted with consistent, logical and easy to read formatting as described in the style guide.
>> For instance, a variable name like `message` can be considered easier to read than `msg`.
>> It may be helpful to adjust your editor's settings to support your chosen guidelines and conventions. For VS Code, see https://code.visualstudio.com/docs/getstarted/settings. One good setting to adjust is the editor's vertical rulers to help you know when you have exceeded the recommended maximum number of characters per line. For instance, to make a ruler appear at the 80-character (Andela) and 100-character (Airbnb) limits for Javascript files, you can add the following in your __User Settings__:
```JSON
{
    "[javascript]": {
        "editor.rulers": [80, 100]
    }
}
```
> * Ensure there are no commented-out code snippets in your codebase.
-----
> * Ensure the web API is well designed. See https://www.codeproject.com/Articles/1227505/Top-REST-API-Best-Practices
> * Ensure the appropriate HTTP methods are used, and that HTTP status code is returned for different scenarios. See https://code-maze.com/the-http-reference/ and https://httpstatuses.com/
> * Ensure JSON responses are properly formatted. See http://jsonapi.org/
> * Ensure user inputs are properly validated in both the server and client sides.
>> For instance, if in the action of a controller on the server side you come across the expression `let name = req.body.user.name`,  
>> This assumes that `req.body.user` is not null/undefined.  
>> Now we know `req.body` should never be undefined (because of the various Express middleware that ensure `req` has a `body` property).  
>> So our focus now becomes to ensure that `req.body.user` is not null/undefined.  
>> If, in that controller function, you can't see any expression that ensures that `req.body.user` is not null/undefined, then go through every middleware execution has to pass through before landing in this controller action.  
>> If you still can't find any expression that ensures that `req.body.user` is not null/undefined, then raise this as an issue.
> * Ensure there aren't excessive calls to the server or database.
> * Use constants (enums) to represent an enumerator list (a limited set of values). For insance, instead of `user.gender = 'male';`, consider using `user.gender = UserGender.MALE`.
-----
> * Ensure proper use of React component life cycle methods, especially `componentWillMount`.
>> * https://daveceddia.com/where-fetch-data-componentwillmount-vs-componentdidmount/
>> * https://stackoverflow.com/questions/41612200/in-react-js-should-i-make-my-initial-network-request-in-componentwillmount-or-co/41612993#41612993
>> * https://engineering.musefind.com/react-lifecycle-methods-how-and-when-to-use-them-2111a1b692b1

## UI/UX

### To Meet Expectation
> * It should be easy for a user to understand what to do next.
> * The application should display an appropriate message when the user enters an invalid input.
> * The application should provide appropriate feedback (e.g. dialog) when the user performs an action (like when the user creates a group).
> * The UI elements should be placed in appropriate positions on the page where they are easily accessed without any form of obscurity.
> * The design shouldn’t contain glitches, no weird overflow of DOM elements, no weird scrollbars in awkward positions.
> * The application obeys the [Material Design](http://materializecss.com/) specs.
> * The application uses consistent colors and font styles.
> * The transition between pages should be asynchronous, no page reloads when moving from one route to another (for single-page applications).
> * The application is fully responsive without glitches covering xs, md and lg devices screens.
> * Perfect typography, the appropriate fonts are used to display content based on context (headings, long texts, messages), all language shown in messages are clearly expressed.
> * All information alerts, dialogs and messages are displayed with/as material dialog boxes, toasts messages. No alert, confirm, prompt are used.

### To Exceed Expectation
> * Any of the material design components have custom CSS tweaks to give them a unique feel enhanced from their generic states

## Comments and Documentation

### To Meet Expectation
> * Comments should be sufficiently present in code.
> * Comments should be concise.
> * Comments should effectively explain the code segments they apply to. Similarly, API docs should accurately describe the operations of their endpoints.
> * JSDoc comments should be properly formatted. See https://github.com/shri/JSDoc-Style-Guide
> * The API should be well documented.
