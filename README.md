# workspace playground

Trying to test out how to use eslint-plugin-import in a monorepo

Tries to test the following scenario

- `packages/app1` has `is-even` in it's `package.json`
- `packages/app2` does not have `is-even` in its `package.json`
- `packages/app2` tries to use `is-even`

In this case we should want to get a warning about this, but
eslint-plugin-import does not warn about it (BY DEFAULT)

You have to add `import/no-extraneous-dependencies` to the eslint rules to get the right behavior

Thanks to @ljharb https://github.com/import-js/eslint-plugin-import/issues/2247
