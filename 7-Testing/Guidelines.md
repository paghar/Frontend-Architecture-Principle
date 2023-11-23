## Non-development time testing

   It’s great also to have Lighthouse tests run on your website . To find easier performance bottlenecks, accessibility issues, and improve web pages quality in general.

   Lighthouse analyzes web apps and web pages, collecting modern performance metrics and insights on developer best practices.

 ### Using Lighthouse in Chrome DevTools   

   Lighthouse is integrated directly into the Chrome DevTools, under the "Lighthouse" panel.

   Installation: install Chrome.

   Run it: open Chrome DevTools, select the Lighthouse panel, and hit "Generate report".

   Run it: follow the [extension quick-start guide.](https://developer.chrome.com/docs/lighthouse/overview/#extension) 

## Using the Node CLI

   The Node CLI provides the most flexibility in how Lighthouse runs can be configured and reported. Users who want more advanced usage, or want to run Lighthouse in an automated fashion should use the Node CLI.

## Using the Node module

   You can also use Lighthouse programmatically with the Node module.

   Read [Using Lighthouse programmatically](https://github.com/GoogleChrome/lighthouse/blob/main/docs/readme.md#using-programmatically) Lighthouse programmatically for help getting started.
   Read [Lighthouse Configuration](https://github.com/GoogleChrome/lighthouse/blob/main/docs/configuration.md) Lighthouse Configuration to learn more about the configuration options available.

## Enhance code quality and performance with ESLint

[Airbnb React/JSX Style Guide](https://github.com/airbnb/javascript/tree/master/react)

## Customize Eslint rules

```bash
module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es2021: true,
    jest: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:@typescript-eslint/recommended",
    // "plugin:storybook/recommended",
    // "airbnb-typescript",
  ],
  parser: "@typescript-eslint/parser",
  parserOptions: {
    project: "./tsconfig.eslint.json",
    ecmaFeatures: {
      "jsx": true,
    },
    ecmaVersion: 12,
  },
  plugins: ["react", "@typescript-eslint"],
  rules: {
    indent: "off",
    "@typescript-eslint/indent": ["error",2],  
    "@typescript-eslint/no-confusing-non-null-assertion": "error",
    "no-empty-function": "off",
    "@typescript-eslint/no-empty-function": ["error"],
    "@typescript-eslint/no-empty-interface": [
      "error",
      {
        "allowSingleExtends": true,
      },
    ],     
    "no-extra-semi": "off",
    "no-plusplus": [2, {allowForLoopAfterthoughts: true}],
    "@typescript-eslint/no-extra-semi": ["error"],
    "@typescript-eslint/no-unnecessary-boolean-literal-compare": ["error"],
    "@typescript-eslint/prefer-enum-initializers": "error",
    "object-curly-spacing": "off",
    "@typescript-eslint/object-curly-spacing": ["error"], 
    "linebreak-style": ["off", "unix"],
    "semi": ["error", "always"],

    "@typescript-eslint/no-unused-expressions": "off",
    "import/extensions" : "off",
    "import/no-extraneous-dependencies" : "off",
    "import/no-unresolved": "off",

    "@typescript-eslint/explicit-module-boundary-types": "off",
    "@typescript-eslint/no-explicit-any": "off",
    "@typescript-eslint/no-inferrable-types": "error",
    "no-case-declarations": "off",
    "@typescript-eslint/ban-ts-comment": "off",
    "@typescript-eslint/ban-types": "off",
    "no-fallthrough": "off",
    "@typescript-eslint/no-var-requires": "off",
    "no-async-promise-executor": "off",
    "no-prototype-builtins": "off",
    "prefer-rest-params": "off",
    "no-useless-escape": "off",
    "no-empty-pattern": "off",
    "prefer-const": "warn",
    "no-useless-catch": "warn",
    "react/no-direct-mutation-state": "warn",
    "react/prop-types": "off",
    "no-var": "warn",
    "no-compare-neg-zero": "warn",
    "react/no-deprecated": "warn",
    "no-extra-boolean-cast": "off",
    "no-irregular-whitespace": "off",
    "@typescript-eslint/no-array-constructor": "off",
    "react/react-in-jsx-scope": "off",
    "max-len": [2, {code: 200, ignoreComments: true}],
    "no-console": "warn",
    "prefer-template": "error",
    "no-unexpected-multiline": "error",  
    "@typescript-eslint/quotes": "off",
    "quotes": ["error", "double", {"allowTemplateLiterals": true}],
    "no-use-before-define":["error", {
      "functions": true,
      "classes": true,
      "variables": true,
    }],
    
  },
  "settings": {
    "react": {
      "version": "detect",
    },
  },
};
```