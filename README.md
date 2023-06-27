# @coldboy002/pug-lint-config

[![NPM version](https://img.shields.io/npm/v/@coldboy002/pug-lint-config.svg)](https://www.npmjs.org/package/@coldboy002/pug-lint-config)

> A sharable [pug-lint](https://github.com/pugjs/pug-lint) config for linting `pug` files.

## Installation

The peer dependencies [pug-lint](https://www.npmjs.com/package/pug-lint) must be installed alongside this package.

> install with npm:

```bash
npm install -D @coldboy002/pug-lint-config pug-lint
```

> install with yarn:

```bash
yarn add -D @coldboy002/pug-lint-config pug-lint
```

## Usage

Add the `pugLintConfig` field to your `package.json` file:

```json
"pugLintConfig": {
  "extends": "@coldboy002/pug-lint-config"
}
```

Or create a pug-lint config file type of your choice in the root folder of your project:

`.pug-lintrc` or `.pug-lintrc.json`

```json
{
  "extends": "@coldboy002/pug-lint-config"
}
```

`.pug-lintrc.js`

```javascript
module.exports = {
  extends: '@coldboy002/pug-lint-config',
};
```

Check out [this page](https://github.com/pugjs/pug-lint#extends) for more details about configuring pug-lint.

## Scripts

Add a script to your `package.json` file:

```json
"scripts": {
  "lint:pug": "glob-exec \"./**/*.pug\" -- \"pug-lint {{files.join(' ')}}\"",
}
```

## FAQ

- [List of available rules](https://github.com/pugjs/pug-lint/blob/master/docs/rules.md)

- [How to check multiple files?](https://github.com/pugjs/pug-lint/issues/144)

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
