---
title: "ESLint"
permalink: /docs/eslint/
excerpt: "ESLint"
last_modified_at: 2018-07-11T15:58:49-04:00
toc: true
---

[ESLint](https://eslint.org/)

Eslint is the dominant tool for linting Node.js packages, and can be configured to enforce multiple coding styles. It is possible to define your own style definitions

Besides checking style, linters are also excellent tools for finding certain classes of bugs, such as those related to variable scope. Assignment to undeclared variables (these leak into the global scope, contaminating it and possibly causing very difficult to find bugs) and use of undefined variables are examples of errors that are detectable at lint time.

Installing and configuring ESLint are easy.

At dinosys, all developers need comply with ESLint standards when creating new code. Before pushing code to a repository on GitHub, you should run ESLint to ensure clean code.

Basic ESLint configuration as below:
```
module.exports = {
  "env": {
    "commonjs": true,
    "es6": true,
    "browser": true
  },
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": 8,
    "sourceType": "module"
  },
  "globals": {
    "arguments": true
  },
  "rules": {
    "indent": [
      "error",
      2
    ],
    "linebreak-style": [
      "error",
      "unix"
    ],
    "quotes": [
      "error",
      "single"
    ],
    "semi": [
      "error",
      "never"
    ],
    "no-trailing-spaces": [
      "error",
      {
        "skipBlankLines": false
      }
    ]
  }
};
```

To learn more about ESLint, see [https://eslint.org/docs/user-guide/configuring](https://eslint.org/docs/user-guide/configuring)
