
<p align="center"><img src="./docs/assets/images/logo.png" width="50"></p>
<h1 align="center">lyt</h1>
<div align="center">

  [![NPM](https://img.shields.io/npm/v/lyt-css?style=flat-square)](https://www.npmjs.com/package/lyt-css)
  [![MIT License](https://img.shields.io/github/license/Spiderpig86/Cirrus.svg?style=flat-square)](https://github.com/ColinEspinas/lyt/blob/master/LICENSE)
  [![Issues](https://img.shields.io/github/issues/ColinEspinas/lyt?style=flat-square)](https://github.com/ColinEspinas/lyt/issues)

</div>

<p align="center">
A flexible and highly configurable CSS layout library. Designed to be tweaked.
<br />
<!-- <a href=""><strong>Check out the docs »</strong></a> -->
<br>
<a href="https://github.com/ColinEspinas/lyt/issues" target="_blank">Request Feature</a>
/
<a href="https://github.com/ColinEspinas/lyt/issues" target="_blank">Report a Bug</a>
</p>

## ▶️ Getting started

### 🚀 Import using a CDN

Just link the `lyt.css` file or it minified version.

```html
<!-- Use normal or minified -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ColinEspinas/lyt/dist/lyt.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ColinEspinas/lyt/dist/lyt.min.css">
```

You can also use each modules individually.

```html
<!-- Use normal or minified -->
<link rel="stylesheet" href="path/to/lyt/dist/grid/flex.css">
<link rel="stylesheet" href="path/to/lyt/dist/grid/flex.min.css">
```

### 📦 Install with a package manager

```sh
npm install lyt-css
```

### ⚙️ Configure

Lyt is designed to be easily configurable using SASS/SCSS.

When using a CDN or local download, you can import the `scss` files by loading them from the `/scss` directory.

```scss
@import "path/to/lyt/scss/lyt.scss";
/* Or import individual modules */
@import "path/to/lyt/scss/grid/flex.scss";
```

Then you just need to import your configuration file before you import the lyt module files.

```scss
@import "path/to/config";
@import "path/to/lyt/scss/lyt.scss";
```

You can find a template config file where all variables are commented with the default values in `/scss/_config.scss`. This configuration file is the default configuration, it is imported by default when building the library.

## 📚 Documentation

**This documentation will be moved in the future when the documentation website will open.**

Lyt is build from multiple modules:

- [Grid](#grid)
  - [Flex](#flex)
- [Utilities](#utilities)
  - [Display](#display)
  - [Float](#float)
  - [Margin](#margin)
  - [Padding](#padding)
  - [Width](#width)

**All the documentation uses the default configuration.**

### Grid

#### Flex

Used to manage the layout easily, the flex grid uses a classic system of row and columns and can be fully customized.

Create rows and columns using `row` and `column`.

By default columns take 100% of the available width. You can constraint a column width by using the `-<n>` class (`<n>` being the amount of space out of 12 taken by the column).

Add the `gap` class to a row to add gaps between columns.

```html
<div class="row gap">
    <div class="column -6">
        <p class="padding-m box">6 of 12</p>
    </div>
    <div class="column -6">
        <p class="padding-m box">6 of 12</p>
    </div>
</div>
```
[See example live](https://jsfiddle.net/hpax1ksL/)

You can also specify a breakpoint to a column by using the `<breakpoint>-<n>` class instead (e.g. `sm-5`).

| Breakpoint | Value  |
|------------|--------|
| sm         | 544p   |
| md         | 768px  |
| lg         | 1012px |
| xl         | 1280px |

By specifying multiple breakpoints to a column, the column will adapt automatically.

```html
<div class="row gap">
    <div class="column sm-10 md-2">
        <p class="padding-m box"></p>
    </div>
    <div class="column sm-2 md-10">
        <p class="padding-m box"></p>
    </div>
</div>
```
[See example live](https://jsfiddle.net/ogarwz7v/)

You can offset columns by using the `offset-<n>` class. You can also specify breakpoints by using the `offset-<breakpoint>-<n>` class.

```html
<div class="row ">
	<div class="column sm-10 offset-sm-1 md-6 offset-md-3">
		<p class="padding-m box">Centered column</p>
	</div>
</div>
```
[See example live](https://jsfiddle.net/sr2c0w96/)

### Utilities

#### Display

Use the `display-<mode>` class to change the display of an element. 

```html
<p class="display-ib">...</p>
```

| Syntax | Mode         |
|--------|--------------|
| b      | block        |
| i      | inline       |
| ib     | inline-block |
| none   | none         |

#### Float

Use the `float` classes to add float to an element.

```html
<p class="float-l">...</p>
```

| Syntax | Value |
|--------|-------|
| l      | left  |
| r      | right |

Clear after using floats with the `float-clear` class on an element.

```html
<p class="float-l">...</p>
<div class="float-clear"></div>
```

#### Margin

Use the `margin-<size>` class to add a margin to an element (`<size>` being the name of the value to the margin).

```html
<p class="margin-m">...</p>
```

Default configuration uses the following values for margin:
| Syntax | Value |
|--------|-------|
| a      | auto  |
| xs     | 4px   |
| s      | 8px   |
| m      | 16px  |
| l      | 24px  |
| xl     | 32px  |
| xxl    | 40px  |

By default, the margin value is applied to all sides. You can specify sides with `margin-<side>-<size>` (e.g. `margin-t-xl`).

```html
<p class="margin-tb-m">...</p>
```

| Syntax | Sides          |
|--------|----------------|
| t      | top            |
| l      | left           |
| b      | bottom         |
| r      | right          |
| tb     | top and bottom |
| lr     | left and right |

#### Padding

Padding classes are used like margin classes but add padding instead.

```html
<p class="padding-t-xxl">...<p>
```

#### Width

You can use the `width-<value>` class to change the width of an element.

```html
<p class="width-33">...<p>
```

| Syntax | Values          |
|--------|-----------------|
| 25      | 25%            |
| 33      | calc(100% / 3) |
| 50      | 50%            |
| 75      | 75%            |
| 100     | 100%           |

You can also use the `min-width-<value>` or `max-width-<value>`.

```html
<p class="max-width-50">...<p>
```

#### Mixins

Mixins can only be used in SASS/SCSS.

##### Breakpoint

The breakpoint mixin can be used to declare classes/properties applied at specific breakpoints.

```scss
.my-text {
  font-size: 16px;
  @include breakpoint(md) {
    font-size: 24px;
  }
}
```

## Contributing

Any help and contribution is always welcome, feel free to submit issues and/or contribute to the project.

1. Fork the project
2. Create your feature or fix Branch (`git checkout -b feature/feature-name` or `git checkout -b fix/fix-name`)
3. Commit your changes using [semantic messages](https://www.conventionalcommits.org/) (`git commit -m "feat/fix: Add some feature or fix"`)
4. Push to the branch (`git push origin feature/feature-name` or `git push origin fix/fix-name`)
5. Open a pull request

## License

Lyt is distributed under the MIT License. See `LICENSE` for more information.

## Contact
[![Buy me a coffee badge](https://img.shields.io/badge/-Buy%20me%20a%20coffee-important?logo=buy%20me%20a%20coffee&logoColor=white&style=flat-square)](https://www.buymeacoffee.com/ColinEspinas)
[![LinkedIn badge](https://img.shields.io/badge/-LinkedIn-black.svg?logo=linkedin&colorB=555&style=flat-square)](https://www.linkedin.com/in/colin-espinas-9739b8178/l)

Colin Espinas - [Website](https://colinespinas.com) - contact@colinespinas.com

Project link: [https://github.com/ColinEspinas/lyt](https://github.com/ColinEspinas/lyt)