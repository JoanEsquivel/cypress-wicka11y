
# Cypress + wick-a11y

[wick-a11y](https://github.com/sclavijosuero/wick-a11y) is a Cypress plugin designed for performing configurable accessibility tests. It allows you to easily incorporate accessibility checks into your End-to-End tests, log detailed information in the Cypress log, and generate HTML documents with screenshots of each violation for easier identification and resolution of accessibility issues, all out-of-the-box. 

Check the following article for every single detail: [wick-a11y documentation](https://dev.to/sebastianclavijo/wick-a11y-cypress-plugin-your-unstoppable-ally-for-smashing-accessibility-barriers-cool-as-john-wick-280a)

## How to install it? 
Run the following command: 

``` npm install wick-a11y cypress --save-dev ```

## How to configure it?

- Register the plugin tasks in cypress.config.js:

```
const { defineConfig } = require("cypress");

// Import the accessibility tasks from wick-a11y plugin
const addAccessibilityTasks = require('wick-a11y/accessibility-tasks');

module.exports = defineConfig({
  e2e: {
    setupNodeEvents(on, config) {
      // Add accessibility tasks
      addAccessibilityTasks(on);
    },

    // ... rest of the configuration
  },
});
```

- Import the library in the e2e file

``` import "wick-a11y"; ```

## How to run the project? 

``` npm run headless-execution ```


### Node version used for this demo

``` v21.6.1 ```