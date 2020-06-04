
<p align="center"><img src="./docs/assets/images/logo.png" width="50"></p>
<h1 align="center">lyt</h1>
<div align="center">

  [![v.0.0.1](https://img.shields.io/badge/lyt-0.0.1-blue.svg?style=flat-square)](https://github.com/ColinEspinas/lyt)
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

## Getting started

### 🚀 Using a CDN

Just link the `lyt.css` file or it minified version.

```html
<!-- Use normal or minified -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ColinEspinas/lyt/dist/lyt.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ColinEspinas/lyt/dist/lyt.min.css">
```

You can also use each modules individually.

```html
<!-- Use normal or minified -->
<link rel="stylesheet" href="../dist/grid/flex.css">
<link rel="stylesheet" href="../dist/grid/flex.min.css">
```

## Modules

Lyt is build from multiple modules:
- [Getting started](#getting-started)
	- [🚀 Using a CDN](#-using-a-cdn)
- [Modules](#modules)
	- [Grid](#grid)
		- [Flex](#flex)
		- [Margin](#margin)
		- [Padding -->](#padding---)

**All the documentation use the default configuration**

### Grid

#### Flex

Used to manage the layout easily, the flex grid uses a classic system of row and columns and can be fully customized.

Create rows and columns using `row` and `column`.

By default columns take 100% of the available width. You can constraint a column width by using the `-n` class (n being the amount of space out of 12 taken by the column).

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
[See example live](https://jsfiddle.net/9mdezjr0/)

You can also specify a breakpoint to a column by using the `breakpoint-n` class instead (e.g. `sm-5`).

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
[See example live](https://jsfiddle.net/9mdezjr0/1/)

You can offset columns by using the `offset-n` class. You can also specify breakpoints by using the `offset-breakpoint-n` class.

```html
<div class="row ">
	<div class="column sm-10 offset-sm-1 md-6 offset-md-3">
		<p class="padding-m box">Centered column</p>
	</div>
</div>
```
[See example live](https://jsfiddle.net/9mdezjr0/2/)

<!-- ### Utilities

#### Margin

#### Padding -->