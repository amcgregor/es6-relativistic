# Relativistic

[![NPM](https://img.shields.io/npm/v/relativistic.svg)](https://www.npmjs.com/package/relativistic)
[![Bower](https://img.shields.io/bower/v/relativistic.svg)](http://bower.io/search/?q=relativistic)

Relativistic is a pure ES6 library to support presentation and automatic update of date elements (à la microformats) within your pages. It transforms the ISO timestamp attribute of the element into a natural language reference, e.g. "4 minutes ago" or "about 1 day ago", then maintains the accuracy of those presentations as long as the page is open.


## Usage

First, load the plugin:

```html
<script src=relativistic.js></script>
```

All `<time>` elements possessing a CSS class of `relative` within the page the script is loaded into will be automatically reformatted. Such elements made relative will have their existing inner text preserved as their `title` attribute, will be updated periodically while the page remains visible and will be automatically refreshed when the page becomes visible once more.

While `<time>` element `datetime` attributes should be formatted according to the [ISO 8601](http://en.wikipedia.org/wiki/ISO_8601) standard, this library accepts any value acceptable for passing to the JavaScript `Date` object constructor.

```html
<time class=relative datetime=2011-12-17T09:24:17Z>December 17, 2011</time>
```

Becomes something like:

```html
<time class="relative live" datetime=2011-12-17T09:24:17Z title="December 17, 2011">about 1 day ago</time>
```

As time passes, the timestamps will automatically update.

**For more usage and examples**: [http://relativistic.webcore.io/](http://relativistic.webcore.io/)

**For different language configurations**: visit the [`locales`](https://github.com/amcgregor/es6-relativistic/tree/master/locales) directory.


## Configuration

TBD


## Changes

TBD

<!--
| Version | Notes                                                                           |
|---------|---------------------------------------------------------------------------------|
|   1.6.x | ([compare][compare-1.6]) Wraped locales in UMD wrappers; locale improvements    |
|   1.5.x | ([compare][compare-1.5]) Added Date as argument to update function; locales     |
|   1.4.x | ([compare][compare-1.4]) Added allowPast setting; locale updates                |
|   1.3.x | ([compare][compare-1.3]) Added updateFromDOM function; bug fixes; bower support |
|   1.2.x | ([compare][compare-1.2]) Added cutoff setting; locale updates                   |
|   1.1.x | ([compare][compare-1.1]) Added update function; locale updates                  |
|   1.0.x | ([compare][compare-1.0]) locale updates; bug fixes; AMD wrapper                 |
|  0.11.x | ([compare][compare-0.11]) natural rounding; locale updates;                     |
|  0.10.x | ([compare][compare-0.10]) locale updates                                        |
|   0.9.x | ([compare][compare-0.9]) microsecond support; bug fixes                         |
|   0.8.x | ([compare][compare-0.8]) `<time>` element support; bug fixes                    |
|   0.0.1 | ([compare][compare-0.7]) locale function overrides; unit tests                  |

[compare-1.6]: https://github.com/rmm5t/jquery-timeago/compare/v1.5.4...v1.6.7
[compare-1.5]: https://github.com/rmm5t/jquery-timeago/compare/v1.4.3...v1.5.4
[compare-1.4]: https://github.com/rmm5t/jquery-timeago/compare/v1.3.2...v1.4.3
[compare-1.3]: https://github.com/rmm5t/jquery-timeago/compare/v1.2.0...v1.3.2
[compare-1.2]: https://github.com/rmm5t/jquery-timeago/compare/v1.1.0...v1.2.0
[compare-1.1]: https://github.com/rmm5t/jquery-timeago/compare/v1.0.2...v1.1.0
[compare-1.0]: https://github.com/rmm5t/jquery-timeago/compare/v0.11.4...v1.0.2
[compare-0.11]: https://github.com/rmm5t/jquery-timeago/compare/v0.10.1...v0.11.4
[compare-0.10]: https://github.com/rmm5t/jquery-timeago/compare/v0.9.3...v0.10.1
[compare-0.9]: https://github.com/rmm5t/jquery-timeago/compare/v0.8.2...v0.9.3
[compare-0.8]: https://github.com/rmm5t/jquery-timeago/compare/v0.7.2...v0.8.2
[compare-0.7]: https://github.com/rmm5t/jquery-timeago/compare/v0.6.2...v0.7.2
-->


## Authors

[Ryan McGeary](http://ryan.mcgeary.org) ([@rmm5t](https://twitter.com/rmm5t))

[Alice Bevan–McGregor](https://github.com/amcgregor/) ([@GothAlice](https://twitter.com/GothAlice))


## License

[MIT License](https://rmm5t.mit-license.org/)

