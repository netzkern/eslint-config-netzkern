# eslint-config-netzkern-base

This package provides netzkern base JS .eslintrc as an extensible shared config.

## Usage

We export two ESLint configurations for your usage.

### eslint-config-netzkern-base

Our default export contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

If you use yarn, run `npm info "eslint-config-netzkern-base@latest" peerDependencies` to list the peer dependencies and versions, then run `yarn add --dev <dependency>@<version>` for each listed peer dependency. See below for npm instructions.

1. Install the correct versions of each package, which are listed by the command:

  ```sh
  npm info "eslint-config-netzkern-base@latest" peerDependencies
  ```

  Linux/OSX users can run
  ```sh
  (
    export PKG=eslint-config-netzkern-base;
    npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
  )
  ```

  Which produces and runs a command like:

  ```sh
    npm install --save-dev eslint-config-netzkern-base eslint@^#.#.# eslint-plugin-import@^#.#.#
  ```

  Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

  ```sh
  npm install -g install-peerdeps
  install-peerdeps --dev eslint-config-netzkern-base
  ```

  The cli will produce and run a command like:

  ```sh
  npm install --save-dev eslint-config-netzkern-base eslint@^#.#.# eslint-plugin-import@^#.#.#
  ```

2. Add `"extends": "netzkern-base"` to your .eslintrc.

### eslint-config-netzkern-base/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

1. Install the correct versions of each package, which are listed by the command:

  ```sh
  npm info "eslint-config-netzkern-base@latest" peerDependencies
  ```

  Linux/OSX users can run
  ```sh
  (
    export PKG=eslint-config-netzkern-base;
    npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
  )
  ```

  Which produces and runs a command like:

  ```sh
  npm install --save-dev eslint-config-netzkern-base eslint@^3.0.1 eslint-plugin-import@^1.10.3
  ```

2. Add `"extends": "netzkern-base/legacy"` to your .eslintrc

See [ESlint config docs](http://eslint.org/docs/user-guide/configuring#extending-configuration-files) for more information.

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

## Credits

- [eslint-airbnb-config](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb-base)