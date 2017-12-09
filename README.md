# 🌀 eslint-config-netzkern-base

> This package provides netzkern base JS .eslintrc as an extensible shared config.

- Extends [babel-preset-airbnb](https://github.com/airbnb/babel-preset-airbnb) for babel settings 

## Usage

We export two ESLint configurations for your usage.

### eslint-config-netzkern-base

Our default export contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

1. Install the correct versions of each package, which are listed by the command:

```sh
  npm install --save-dev eslint-config-netzkern-base eslint eslint-plugin-import
```

2. Add `"extends": "netzkern-base"` to your .eslintrc.

### eslint-config-netzkern-base/legacy

Lints ES5 and below. Requires `eslint`.

1. Install the correct versions of each package, which are listed by the command:

```sh
  npm install --save-dev eslint-config-netzkern-base eslint
```

2. Add `"extends": "netzkern-base/legacy"` to your .eslintrc.

## Targeting Environments

[Details](https://github.com/airbnb/babel-preset-airbnb#targeting-environments)

## Improving this config

Consider adding test cases if you're making complicated rules changes, like anything involving regexes. Perhaps in a distant future, we could use literate programming to structure our README as test cases for our .eslintrc?

You can run tests with `npm test`.

You can make sure this module lints with itself using `npm run lint`.

## Significant changes from airbnb-base

```js
{
  'brace-style': ['error', '1tbs', { allowSingleLine: false }], // disallow single line
  indent: ['error', 4] // 4 spaces
  curly: ['error', 'all'], // always enforce braces
}
```

## Tooling
- Visual Studio Code [link](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

## Credits

- [eslint-airbnb-config](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb-base)
