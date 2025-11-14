# @coldboy002/pug-lint-config

[![NPM version](https://img.shields.io/npm/v/@coldboy002/pug-lint-config.svg)](https://www.npmjs.org/package/@coldboy002/pug-lint-config)

> A sharable [pug-lint](https://github.com/pugjs/pug-lint) config for linting `pug` files.

## Installation

The peer dependencies [pug-lint](https://www.npmjs.com/package/pug-lint) must be installed alongside this package.

```bash
npm install -D @coldboy002/pug-lint-config
```

or

```bash
yarn add -D @coldboy002/pug-lint-config
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

### Extending the config

You can specify additional rules and override or turn off already set ones.

For example, to change the `validateIndentation` rule to specify a different indentation, turn off the `requireStrictEqualityOperators` rule and add the `validateDivTags` rule:

```json
{
  "extends": "@coldboy002/pug-lint-config",
  "requireStrictEqualityOperators": null,
  "validateDivTags": true,
  "validateIndentation": 4
}
```

Check out [this page](https://github.com/pugjs/pug-lint#extends) for more details about configuring pug-lint.

## Integration with VS Code

1. Install the pug-lint [extension](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-puglint) for VS Code.
2. Enable the linter in VS Code [settings](https://code.visualstudio.com/docs/getstarted/settings).
3. Install `pug-lint` and this config in your project following the [Installation](#installation) section.
4. Add a pug-lint configuration file (`.pug-lintrc.*`) and extend it with this shareable config following the [Usage](#usage) section.

## FAQ

- [List of available rules](https://github.com/pugjs/pug-lint/blob/master/docs/rules.md)

- [How to check multiple files?](https://github.com/pugjs/pug-lint/issues/144)

## [Changelog](CHANGELOG.md)

## [License](LICENSE)
