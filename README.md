<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# y1

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Compute the [Bessel function of the second kind][bessel-second-kind] of order one.

<section class="intro">

The [Bessel function of the second kind][bessel-second-kind] of order one is defined as

<!-- <equation class="equation" label="eq:bessel_second_kind_order_one" align="center" raw="Y_1(x) = \frac{1}{\pi} \int_0^\pi \sin(x \sin\theta - \theta) \, d\theta -\frac{1}{\pi} \int_0^\infty  \left[ e^t - e^{-t} \right]  e^{-x \sinh t} \, dt" alt="Bessel function of the second kind of order one"> -->

<div class="equation" align="center" data-raw-text="Y_1(x) = \frac{1}{\pi} \int_0^\pi \sin(x \sin\theta - \theta) \, d\theta -\frac{1}{\pi} \int_0^\infty  \left[ e^t - e^{-t} \right]  e^{-x \sinh t} \, dt" data-equation="eq:bessel_second_kind_order_one">
    <img src="https://cdn.rawgit.com/stdlib-js/stdlib/7e0a95722efd9c771b129597380c63dc6715508b/lib/node_modules/@stdlib/math/base/special/bessely1/docs/img/equation_bessel_second_kind_order_one.svg" alt="Bessel function of the second kind of order one">
    <br>
</div>

<!-- </equation> -->

</section>

<!-- ./intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-bessely1
```

</section>

<section class="usage">

## Usage

```javascript
var y1 = require( '@stdlib/math-base-special-bessely1' );
```

#### y1( x )

Computes the [Bessel function of the second kind][bessel-second-kind] of order one at `x`.

```javascript
var v = y1( 0.0 );
// returns -Infinity

v = y1( 1.0 );
// returns ~-0.781

v = y1( Infinity );
// returns 0.0
```

If `x < 0` or `x` is `NaN`, the function returns `NaN`.

```javascript
var v = y1( -1.0 );
// returns NaN

v = y1( -Infinity );
// returns NaN

v = y1( NaN );
// returns NaN

```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var y1 = require( '@stdlib/math-base-special-bessely1' );

var x;
var i;

for ( i = 0; i < 100; i++ ) {
    x = randu() * 10.0;
    console.log( 'y1(%d) = %d', x, y1( x ) );
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-bessely1.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-bessely1

[test-image]: https://github.com/stdlib-js/math-base-special-bessely1/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/math-base-special-bessely1/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-bessely1/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-bessely1?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-bessely1
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-bessely1/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-bessely1/main/LICENSE

[bessel-second-kind]: https://en.wikipedia.org/wiki/Bessel_function#Bessel_functions_of_the_second_kind:_Y.CE.B1

</section>

<!-- /.links -->
