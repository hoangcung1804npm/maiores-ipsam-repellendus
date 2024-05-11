# @hoangcung1804npm/maiores-ipsam-repellendus <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a DataView, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `DataView.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const dataViewBuffer = require('@hoangcung1804npm/maiores-ipsam-repellendus');
const assert = require('assert');

const ab = new ArrayBuffer(0);
const dv = new DataView(ab);
assert.equal(dataViewBuffer(dv), ab);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@hoangcung1804npm/maiores-ipsam-repellendus
[npm-version-svg]: https://versionbadg.es/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus.svg
[deps-svg]: https://david-dm.org/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus.svg
[deps-url]: https://david-dm.org/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus
[dev-deps-svg]: https://david-dm.org/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@hoangcung1804npm/maiores-ipsam-repellendus.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@hoangcung1804npm/maiores-ipsam-repellendus.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@hoangcung1804npm/maiores-ipsam-repellendus.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@hoangcung1804npm/maiores-ipsam-repellendus
[codecov-image]: https://codecov.io/gh/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus
[actions-url]: https://github.com/inspect-js/@hoangcung1804npm/maiores-ipsam-repellendus/actions
