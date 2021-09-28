# workspace playground

Trying to test out how to use eslint-plugin-import in a monorepo

Currently tests that 'wibble', a non-exitant package trying to be used, is
caught by eslint-plugin-import

Also tests that if `packages/app1` has `is-even` in it's `package.json`, and
that `packages/app2` does not have is-even in its `package.json`, but tries to
use it, then eslint-plugin-import warns about it

This works in this context but not in a different project

Current eslint output

```

yarn run v1.22.10
$ eslint .

/home/cdiesh/testing/packages/app2/src/index.js
  1:20  error  Unable to resolve path to module 'is-even'  import/no-unresolved
  2:8   error  'wibble' is defined but never used          no-unused-vars
  2:20  error  Unable to resolve path to module 'wibble'   import/no-unresolved

✖ 3 problems (3 errors, 0 warnings)


```
