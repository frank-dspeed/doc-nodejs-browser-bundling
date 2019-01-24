# nodejs-browser-bundling
The Current State of bundlers.

## using module esm
- You should always use esm to load your module code like in the browser
- you should bundle all code exempt the loader files that are .js so you should simply only bundle .mjs
- you should write only es6 .mjs code exempt for the loader.js
- you should use rollup with dynamic imports and load systemjs bundles in older browser and directly load es6 bundles with shim and pollyfills if possible

## Extra brave is to don't even load esm
- use --node-experimental-modules flag or the nodejs esm fork 
- use rollup as bundler with systemjs bundels for older browsers.
- use only the .mjs extension if some one whants CJS he needs to convert that in node to stop them from doing so :)
