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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Median

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Uniform][uniform-distribution] distribution [median][median].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [median][median] for a [uniform][uniform-distribution] random variable is

<!-- <equation class="equation" label="eq:uniform_median" align="center" raw="\operatorname{Median}\left[ X \right] = \frac{1}{2} \left( a + b \right)" alt="Median for a uniform distribution."> -->

```math
\mathop{\mathrm{Median}}\left[ X \right] = \frac{1}{2} \left( a + b \right)
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{Median}\left[ X \right] = \frac{1}{2} \left( a + b \right)" data-equation="eq:uniform_median">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@591cf9d5c3a0cd3c1ceec961e5c49d73a68374cb/lib/node_modules/@stdlib/stats/base/dists/uniform/median/docs/img/equation_uniform_median.svg" alt="Median for a uniform distribution.">
    <br>
</div> -->

<!-- </equation> -->

where `a` is the minimum support and `b` the maximum support of the distribution.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/stats-base-dists-uniform-median
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var median = require( '@stdlib/stats-base-dists-uniform-median' );
```

#### median( a, b )

Returns the [median][median] of a [uniform][uniform-distribution] distribution with parameters `a` (minimum support) and `b` (maximum support).

```javascript
var v = median( 0.0, 1.0 );
// returns 0.5

v = median( 4.0, 12.0 );
// returns 8.0

v = median( 2.0, 8.0 );
// returns 5.0
```

If provided `NaN` as any argument, the function returns `NaN`.

```javascript
var v = median( NaN, 2.0 );
// returns NaN

v = median( 2.0, NaN );
// returns NaN
```

If provided `a >= b`, the function returns `NaN`.

```javascript
var y = median( 3.0, 2.0 );
// returns NaN

y = median( 3.0, 3.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var median = require( '@stdlib/stats-base-dists-uniform-median' );

var a;
var b;
var v;
var i;

for ( i = 0; i < 10; i++ ) {
    a = ( randu()*10.0 );
    b = ( randu()*10.0 ) + a;
    v = median( a, b );
    console.log( 'a: %d, b: %d, Median(X;a,b): %d', a.toFixed( 4 ), b.toFixed( 4 ), v.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-uniform-median.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-uniform-median

[test-image]: https://github.com/stdlib-js/stats-base-dists-uniform-median/actions/workflows/test.yml/badge.svg?branch=v0.2.2
[test-url]: https://github.com/stdlib-js/stats-base-dists-uniform-median/actions/workflows/test.yml?query=branch:v0.2.2

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-uniform-median/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-uniform-median?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-uniform-median.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-uniform-median/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-uniform-median/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-base-dists-uniform-median/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-base-dists-uniform-median/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-base-dists-uniform-median/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-base-dists-uniform-median/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-base-dists-uniform-median/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-base-dists-uniform-median/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-uniform-median/main/LICENSE

[uniform-distribution]: https://en.wikipedia.org/wiki/Uniform_distribution_%28continuous%29

[median]: https://en.wikipedia.org/wiki/Median

</section>

<!-- /.links -->
