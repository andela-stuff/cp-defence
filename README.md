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
> * There should be at least one form of minification of static content
> * Set up testing task with code coverage file generator.
> * Configure continuous integration to run the required tasks, tests, and then deploy to a cloud-based server.
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
> * The README file should be well prepared. There should be a “contributing” section.
> * Commit (and PR) messages should be in accordance with the appropriate conventions/guidelines.
