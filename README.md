`prefersContrast()`
==================
> Detects user’s preferences for contrast using the `prefers-contrast` CSS3 level 5 media query.

[![Travis](https://img.shields.io/travis/com/magica11y/prefers-contrast.svg?style=for-the-badge)](https://app.travis-ci.com/github/magica11y/prefers-contrast)
[![NPM](https://img.shields.io/npm/v/@magica11y/prefers-contrast.svg?style=for-the-badge "NPM")](https://www.npmjs.com/package/@magica11y/prefers-contrast)
[![Bundlephobia](https://img.shields.io/bundlephobia/min/@magica11y/prefers-contrast.svg?style=for-the-badge "Bundle size (minified)")](https://bundlephobia.com/result?p=@magica11y/prefers-contrast)
[![Bundlephobia](https://img.shields.io/bundlephobia/minzip/@magica11y/prefers-contrast.svg?style=for-the-badge "Bundle size (minified+gzipped)")](https://bundlephobia.com/result?p=@magica11y/prefers-contrast)
[![Coveralls](https://img.shields.io/coveralls/github/magica11y/prefers-contrast.svg?style=for-the-badge "Test coverage status")](https://coveralls.io/github/magica11y/prefers-contrast)
[![David DM](https://img.shields.io/david/magica11y/prefers-contrast.svg?style=for-the-badge "Dependencies")](https://david-dm.org/magica11y/prefers-contrast)
[![David DM](https://img.shields.io/david/dev/magica11y/prefers-contrast.svg?style=for-the-badge "Dev Dependencies")](https://david-dm.org/magica11y/prefers-contrast?type=dev)
[![NodeJS](https://img.shields.io/node/v/@magica11y/prefers-contrast.svg?style=for-the-badge "Node engine")](https://www.npmjs.com/package/@magica11y/prefers-contrast)
[![License](https://img.shields.io/github/license/magica11y/prefers-contrast.svg?style=for-the-badge "MIT license")](LICENSE.md)
[![Snyk](https://img.shields.io/snyk/vulnerabilities/github/magica11y/prefers-contrast?style=for-the-badge "Snyk vulnerabilities status")](https://snyk.io/test/github/magica11y/prefers-contrast?targetFile=package.json)

[![Magica11y cover](https://cdn.jsdelivr.net/gh/magica11y/cauldron@1.0.7/assets/Magica11y-cover.jpg "Magica11y cover")](https://magica11y.github.io)


# :sparkles: Introduction

Quoting from the [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3) [level 5](https://www.w3.org/TR/mediaqueries-5)
[media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries) specfication…

> The [`'prefers-contrast'`](https://drafts.csswg.org/mediaqueries-5/#prefers-contrast) media feature is used to detect if the user has requested the system increase or decrease the amount of contrast between adjacent colors. For example, many users have difficulty reading text that has a small difference in contrast to the text background and would prefer a larger contrast.

:high_brightness: **`prefersContrast()`** is part of :crystal_ball: [**Magica11y**](https://magica11y.github.io),
which provides a suite of functions to detect “user-preference” and “environment” media features.

[Magica11y](https://magica11y.github.io) functions are awesome because…
  * They have **zero** dependencies
  * They’re **lightweight**; e.g. `prefersContrast()` is just [![Bundlephobia](https://img.shields.io/bundlephobia/min/@magica11y/prefers-contrast.svg?style=flat-square&label "Bundle size (minified)")](https://bundlephobia.com/result?p=@magica11y/prefers-contrast) minified, or [![Bundlephobia](https://img.shields.io/bundlephobia/minzip/@magica11y/prefers-contrast.svg?style=flat-square&label "Bundle size (minified+gzipped)")](https://bundlephobia.com/result?p=@magica11y/prefers-contrast) minified & gzipp’d
  * They use the **[`window.matchMedia`](https://developer.mozilla.org/docs/Web/API/Window/matchMedia)** API underneath
  * They’re optimized for **performance**; all the module functions are designed in such a way that they exit early
  * They provide a **clean**, **well-documented** and **semantic** API to work with

In addition to `prefersContrast()`, [Magica11y](https://magica11y.github.io) also provides…

  * :tv: [`environmentBlending()`](https://github.com/magica11y/environment-blending)
  * :art: [`forcedColors()`](https://github.com/magica11y/forced-colors)
  * :new_moon: [`invertedColors()`](https://github.com/magica11y/inverted-colors)
  * ~:candle: [`lightLevel()`](https://github.com/magica11y/light-level)~
  * :last_quarter_moon: [`prefersColorScheme()`](https://github.com/magica11y/prefers-color-scheme)
  * :roller_coaster: [`prefersReducedMotion()`](https://github.com/magica11y/prefers-reduced-motion)
  * :gem: [`prefersReducedTransparency()`](https://github.com/magica11y/prefers-reduced-transparency)

# :rocket: Getting started

## :building_construction: Installation

You can install `prefersContrast()` using a package manager such as [`yarn`](https://yarnpkg.com/en/package/@magica11y/prefers-contrast) or [`npm`](https://www.npmjs.com/package/@magica11y/prefers-contrast)…

```sh
$ yarn add "@magica11y/prefers-contrast"
# OR
$ npm install --save "@magica11y/prefers-contrast"
```

You can also include `prefersContrast()` from a CDN on your page, such as [jsDelivr](https://www.jsdelivr.com/package/npm/@magica11y/prefers-contrast) or [unpkg](https://unpkg.com/@magica11y/prefers-contrast)…

```html
<script src="https://cdn.jsdelivr.net/npm/@magica11y/prefers-contrast@latest/dist/magica11y.prefersContrast.min.js"></script>
<!-- OR -->
<script src="https://unpkg.com/@magica11y/prefers-contrast@latest/dist/magica11y.prefersContrast.js"></script>
```

## :game_die: Usage

`prefersContrast()` is distributed as a [UMD](https://github.com/umdjs/umd) module, so you can use it as a browser global…

```js
var contrastPreference = window.magica11y.prefersContrast.default();
var useHighContrastColorScheme = (contrastPreference === window.magica11y.prefersContrast.contrastPreferences.MORE);
```

… or as a CommonJS module…

```js
const prefersContrast = require('@magica11y/prefers-contrast');
const contrastPreference = prefersContrast.default();
const useHighContrastColorScheme = (contrastPreference === prefersContrast.contrastPreferences.MORE);
```

… or as an ES module…

```js
import prefersContrast, { contrastPreferences } from '@magica11y/prefersContrast';

const contrastPreference = prefersContrast();
const useHighContrastColorScheme = (contrastPreference === contrastPreferences.MORE);
```

The `contrastPreferences` object contains all the possible values supported by the `'prefers-contrast'` media query…

* `contrastPreferences.NO_PREFERENCE` (spec: [`'no-preference'`](https://www.w3.org/TR/mediaqueries-5/#valdef-media-prefers-contrast-no-preference))
  > Indicates that the user has made no preference known to the system.
* `contrastPreferences.HIGH` (spec: [`'high'`](https://www.w3.org/TR/mediaqueries-5/#valdef-media-prefers-contrast-high))
  > Indicates that user has notified the system that they prefer an interface that has a higher level of contrast.
* `contrastPreferences.LOW` (spec: [`'low'`](https://www.w3.org/TR/mediaqueries-5/#valdef-media-prefers-contrast-low))
  > Indicates that user has notified the system that they prefer an interface that has a lower level of contrast.
* `null`
  > The user’s preference could not be determined.


# :checkered_flag: Typechecking

You can import the [Flow](https://flow.org) types from the provided [libdefs](https://flow.org/en/docs/libdefs)
in `node_modules/@magica11y/prefers-contrast/lib` by configuring them in your `.flowconfig`…

```
[libs]
node_modules/@magica11y/prefers-contrast/lib
```

Now, you can use the Flow types as follows…

```js
// @flow
import prefersContrast, { type ContrastPreference } from '@magica11y/prefers-contrast';

const contrastPreference: ?ContrastPreference = prefersContrast();
```

:tophat: **Note**: `prefersContrast()` returns a [`nullable`](https://flow.org/en/docs/types/primitives/#toc-null-and-void)
type (i.e. `ContrastPreference`). So using the `?` prefix to indicate nullable types is recommended (i.e. `?ContrastPreference`).


# :scroll: License

[![License](https://img.shields.io/github/license/magica11y/magica11y.svg?style=for-the-badge "MIT license")](LICENSE.md)

See [LICENSE.md](LICENSE.md) for more details.

Handcrafted with :heart: by [Rishabh](https://rishabh.ink).

[![Twitter](https://img.shields.io/twitter/follow/rishabh_ink.svg?style=social)](https://twitter.com/rishabh_ink)
