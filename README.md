Reproduce import error for [json-url](https://github.com/masotime/json-url)

Issue: https://github.com/masotime/json-url/issues/17

## Reproduce

* `npm install` or `yarn`
* `node index.js`

```
➜  json-url-import-repro git:(master) ✗ node index.js
internal/modules/cjs/loader.js:895
  throw err;
  ^

Error: Cannot find module '@babel/runtime/helpers/interopRequireDefault'
Require stack:
- /Users/kellymiyashiro/Projects/json-url-import-repro/node_modules/json-url/dist/node/index.js
- /Users/kellymiyashiro/Projects/json-url-import-repro/index.js
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:892:15)
    at Function.Module._load (internal/modules/cjs/loader.js:742:27)
    at Module.require (internal/modules/cjs/loader.js:964:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (/Users/kellymiyashiro/Projects/json-url-import-repro/node_modules/json-url/dist/node/index.js:3:30)
    at Module._compile (internal/modules/cjs/loader.js:1075:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1096:10)
    at Module.load (internal/modules/cjs/loader.js:940:32)
    at Function.Module._load (internal/modules/cjs/loader.js:781:14)
    at Module.require (internal/modules/cjs/loader.js:964:19) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    '/Users/kellymiyashiro/Projects/json-url-import-repro/node_modules/json-url/dist/node/index.js',
    '/Users/kellymiyashiro/Projects/json-url-import-repro/index.js'
  ]
}
```
