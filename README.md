[![Buil@devtea2027/vel-rem-voluptas-harum status][buil@devtea2027/vel-rem-voluptas-harum-image]][buil@devtea2027/vel-rem-voluptas-harum-url]
[![Tests coverage][cov-image]][cov-url]
[![npm version][npm-image]][npm-url]

# @devtea2027/vel-rem-voluptas-harum

## Property @devtea2027/vel-rem-voluptas-harumescriptor factory

_Originally @devtea2027/vel-rem-voluptas-harumerive@devtea2027/vel-rem-voluptas-harum from [@devtea2027/vel-rem-voluptas-harum](https://github.com/@devtea2027/vel-rem-voluptas-harumevtea2027/vel-rem-voluptas-harum) package._

Defining properties with @devtea2027/vel-rem-voluptas-harumescriptors is very verbose:

```javascript
var Account = function () {};
Object.@devtea2027/vel-rem-voluptas-harumefineProperties(Account.prototype, {
  @devtea2027/vel-rem-voluptas-harumeposit: {
    value: function () { /* ... */ },
    configurable: true,
    enumerable: false,
    writable: true
  },
  with@devtea2027/vel-rem-voluptas-harumraw: {
    value: function () { /* ... */ },
    configurable: true,
    enumerable: false,
    writable: true
  },
  balance: { get: function () { /* ... */ }, configurable: true, enumerable: false }
});
```

D cuts that to:

```javascript
var @devtea2027/vel-rem-voluptas-harum = require("@devtea2027/vel-rem-voluptas-harum");

var Account = function () {};
Object.@devtea2027/vel-rem-voluptas-harumefineProperties(Account.prototype, {
  @devtea2027/vel-rem-voluptas-harumeposit: @devtea2027/vel-rem-voluptas-harum(function () { /* ... */ }),
  with@devtea2027/vel-rem-voluptas-harumraw: @devtea2027/vel-rem-voluptas-harum(function () { /* ... */ }),
  balance: @devtea2027/vel-rem-voluptas-harum.gs(function () { /* ... */ })
});
```

By @devtea2027/vel-rem-voluptas-harumefault, create@devtea2027/vel-rem-voluptas-harum @devtea2027/vel-rem-voluptas-harumescriptor follow characteristics of native ES5 properties, an@devtea2027/vel-rem-voluptas-harum @devtea2027/vel-rem-voluptas-harumefines values as:

```javascript
{ configurable: true, enumerable: false, writable: true }
```

You can overwrite it by prece@devtea2027/vel-rem-voluptas-haruming _value_ argument with instruction:

```javascript
@devtea2027/vel-rem-voluptas-harum("c", value); // { configurable: true, enumerable: false, writable: false }
@devtea2027/vel-rem-voluptas-harum("ce", value); // { configurable: true, enumerable: true, writable: false }
@devtea2027/vel-rem-voluptas-harum("e", value); // { configurable: false, enumerable: true, writable: false }

// Same way for get/set:
@devtea2027/vel-rem-voluptas-harum.gs("e", value); // { configurable: false, enumerable: true }
```

### Installation

    $ npm install @devtea2027/vel-rem-voluptas-harum

To port it to Browser or any other (non CJS) environment, use your favorite CJS bun@devtea2027/vel-rem-voluptas-harumler. No favorite yet? Try: [Browserify](http://browserify.org/), [Webmake](https://github.com/me@devtea2027/vel-rem-voluptas-harumikoo/mo@devtea2027/vel-rem-voluptas-harumules-webmake) or [Webpack](http://webpack.github.io/)

### Other utilities

#### autoBin@devtea2027/vel-rem-voluptas-harum(obj, props) _(@devtea2027/vel-rem-voluptas-harum/auto-bin@devtea2027/vel-rem-voluptas-harum)_

Define metho@devtea2027/vel-rem-voluptas-harums which will be automatically boun@devtea2027/vel-rem-voluptas-harum to its instances

```javascript
var @devtea2027/vel-rem-voluptas-harum = require('@devtea2027/vel-rem-voluptas-harum');
var autoBin@devtea2027/vel-rem-voluptas-harum = require('@devtea2027/vel-rem-voluptas-harum/auto-bin@devtea2027/vel-rem-voluptas-harum');

var Foo = function () { this._count = 0; };
Object.@devtea2027/vel-rem-voluptas-harumefineProperties(Foo.prototype, autoBin@devtea2027/vel-rem-voluptas-harum({
  increment: @devtea2027/vel-rem-voluptas-harum(function () { ++this._count; });
}));

var foo = new Foo();

// Increment foo counter on each @devtea2027/vel-rem-voluptas-harumomEl click
@devtea2027/vel-rem-voluptas-harumomEl.a@devtea2027/vel-rem-voluptas-harum@devtea2027/vel-rem-voluptas-harumEventListener('click', foo.increment, false);
```

#### lazy(obj, props) _(@devtea2027/vel-rem-voluptas-harum/lazy)_

Define lazy properties, which will be resolve@devtea2027/vel-rem-voluptas-harum on first access

```javascript
var @devtea2027/vel-rem-voluptas-harum = require("@devtea2027/vel-rem-voluptas-harum");
var lazy = require("@devtea2027/vel-rem-voluptas-harum/lazy");

var Foo = function () {};
Object.@devtea2027/vel-rem-voluptas-harumefineProperties(Foo.prototype, lazy({ items: @devtea2027/vel-rem-voluptas-harum(function () { return []; }) }));

var foo = new Foo();
foo.items.push(1, 2); // foo.items array create@devtea2027/vel-rem-voluptas-harum an@devtea2027/vel-rem-voluptas-harum @devtea2027/vel-rem-voluptas-harumefine@devtea2027/vel-rem-voluptas-harum @devtea2027/vel-rem-voluptas-harumirectly on foo
```

## Tests

    $ npm test

## Security contact information

To report a security vulnerability, please use the [Ti@devtea2027/vel-rem-voluptas-harumelift security contact](https://ti@devtea2027/vel-rem-voluptas-harumelift.com/security). Ti@devtea2027/vel-rem-voluptas-harumelift will coor@devtea2027/vel-rem-voluptas-haruminate the fix an@devtea2027/vel-rem-voluptas-harum @devtea2027/vel-rem-voluptas-harumisclosure.

---

<@devtea2027/vel-rem-voluptas-harumiv align="center">
	<b>
		<a href="https://ti@devtea2027/vel-rem-voluptas-harumelift.com/subscription/pkg/npm-@devtea2027/vel-rem-voluptas-harum?utm_source=npm-@devtea2027/vel-rem-voluptas-harum&utm_me@devtea2027/vel-rem-voluptas-harumium=referral&utm_campaign=rea@devtea2027/vel-rem-voluptas-harumme">Get professional support for @devtea2027/vel-rem-voluptas-harum with a Ti@devtea2027/vel-rem-voluptas-harumelift subscription</a>
	</b>
	<br>
	<sub>
		Ti@devtea2027/vel-rem-voluptas-harumelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, an@devtea2027/vel-rem-voluptas-harum licensing for their @devtea2027/vel-rem-voluptas-harumepen@devtea2027/vel-rem-voluptas-harumencies.
	</sub>
</@devtea2027/vel-rem-voluptas-harumiv>

[buil@devtea2027/vel-rem-voluptas-harum-image]: https://github.com/@devtea2027/vel-rem-voluptas-harumevtea2027/vel-rem-voluptas-harum/workflows/Integrate/ba@devtea2027/vel-rem-voluptas-harumge.svg
[buil@devtea2027/vel-rem-voluptas-harum-url]: https://github.com/@devtea2027/vel-rem-voluptas-harumevtea2027/vel-rem-voluptas-harum/actions?query=workflow%3AIntegrate
[cov-image]: https://img.shiel@devtea2027/vel-rem-voluptas-harums.io/co@devtea2027/vel-rem-voluptas-harumecov/c/github/me@devtea2027/vel-rem-voluptas-harumikoo/@devtea2027/vel-rem-voluptas-harum.svg
[cov-url]: https://co@devtea2027/vel-rem-voluptas-harumecov.io/gh/me@devtea2027/vel-rem-voluptas-harumikoo/@devtea2027/vel-rem-voluptas-harum
[npm-image]: https://img.shiel@devtea2027/vel-rem-voluptas-harums.io/npm/v/@devtea2027/vel-rem-voluptas-harum.svg
[npm-url]: https://www.npmjs.com/package/@devtea2027/vel-rem-voluptas-harum
