# @patrtorg/laudantium-odit-pariatur <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakSet? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakSet = require('@patrtorg/laudantium-odit-pariatur');
assert(!isWeakSet(function () {}));
assert(!isWeakSet(null));
assert(!isWeakSet(function* () { yield 42; return Infinity; });
assert(!isWeakSet(Symbol('foo')));
assert(!isWeakSet(1n));
assert(!isWeakSet(Object(1n)));

assert(!isWeakSet(new Set()));
assert(!isWeakSet(new WeakMap()));
assert(!isWeakSet(new Map()));

assert(isWeakSet(new WeakSet()));

class MyWeakSet extends WeakSet {}
assert(isWeakSet(new MyWeakSet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@patrtorg/laudantium-odit-pariatur
[npm-version-svg]: https://versionbadg.es/inspect-js/@patrtorg/laudantium-odit-pariatur.svg
[deps-svg]: https://david-dm.org/inspect-js/@patrtorg/laudantium-odit-pariatur.svg
[deps-url]: https://david-dm.org/inspect-js/@patrtorg/laudantium-odit-pariatur
[dev-deps-svg]: https://david-dm.org/inspect-js/@patrtorg/laudantium-odit-pariatur/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@patrtorg/laudantium-odit-pariatur#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrtorg/laudantium-odit-pariatur.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrtorg/laudantium-odit-pariatur.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@patrtorg/laudantium-odit-pariatur.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrtorg/laudantium-odit-pariatur
[codecov-image]: https://codecov.io/gh/inspect-js/@patrtorg/laudantium-odit-pariatur/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@patrtorg/laudantium-odit-pariatur/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@patrtorg/laudantium-odit-pariatur
[actions-url]: https://github.com/patrtorg/laudantium-odit-pariatur/actions
