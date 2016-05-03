# Shared ESLint Configs for Coffee and Code

In order to keep eslint configurations synched between projects, we've moved
our configurations to this repository. You can include it in your projects
with `npm install eslint eslint-config-coffeeandcode --save-dev`.

Once installed, you can [extend][1] the following configurations:

## `coffeeandcode`

The base configuration, it extends `eslint:recommended`.


## `coffeeandcode/node`

This builds upon the base `coffeeandcode` configuration by adding the `node`
environment. In a Node project, you would have a root `.eslintrc.json` file
that includes the following:

```json
{
  "extends": "coffeeandcode/node"
}
```


## `coffeeandcode/ci/node`

This builds upon the `coffeeandcode/node` configuration by adding globals
used by [Mocha][2]. In your project's `test/` folder, you would create a `.eslintrc.json`
file with the following:

```json
{
  "extends": "coffeeandcode/ci/node"
}
```


[1]: http://eslint.org/docs/user-guide/configuring#extending-configuration-files
[2]: https://mochajs.org/
