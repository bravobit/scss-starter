# `@bravobit/scss-starter`

<p align="center">
  <img height="46px" width="411px" src="https://raw.githubusercontent.com/bravobit/scss-starter/master/logo.png">
  <p align="center">Simply CSS-resets, standard variables and it also contains mixins to help you develop your web project.</p>
</p>

- Use <kbd>command</kbd> + <kbd>F</kbd> or <kbd>ctrl</kbd> + <kbd>F</kbd> to search for a keyword.
- Contributions welcome, please see [contribution guide](CONTRIBUTING.md).

## Contents
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Usage](#usage)
- [Mixins](#mixins)
  - [Device](#mixins-device)
  - [Z-index](#mixins-z-index)
  - [Positioning](#mixins-positioning)
  - [Prefixing](#mixins-prefixing)
- [Elements](#elements)
  - [Grid](#elements-grid)
  - [Container](#elements-container)
- [Build](#build)
  - [Once](#build-once)
  - [Watch](#build-watch)
- [License](#license)

## <a name="getting-started"></a> Getting Started
### <a name="installation"></a> Installation

You can install this package locally with npm or yarn. You should install the latest stable version in the `devDependencies` section in your `package.json`.

```bash
# To get the latest stable version in devDependencies

npm install @bravobit/scss-starter --save-dev

# or

yarn add @bravobit/scss-starter --dev
```

### <a name="usage"></a> Usage

If you want to use the mixins and are working in a `.scss` file You should import our `styles.scss` file into your project to get the full product.

```scss
@import '~@bravobit/scss-starter/src/styles.scss';
```

If you want to include our default styling in your HTML you can use the compiled (and minified) version.

```html
<link rel="stylesheet" href="%RELATIVE_NODE_MODULES%/@bravobit/scss-starter/dist/styles.css">
```

## <a name="mixins"></a> Mixins
### <a name="mixins-device"></a> Device

Do you want to use media queries for different device-sizes in your project, use the `device` mixin.

```scss
.content {
    max-width: 100%;
    
    @include device(tablet) { max-width: 800px; }
}
```

### <a name="mixins-z-index"></a> Z-index

You should add your z-index items to the `$z-indexes` list to keep the layers organized, then use the `z-index` mixin.

```scss
$z-indexes: (
    'header',
    'footer'
);

.header { @include z-index('header'); }
.footer { @include z-index('footer'); }
```

### <a name="mixins-positioning"></a> Positioning

If you want an easy way to set the position of the element use the `position` mixin.

```scss
.cube {
    @include position(absolute, top 100% left 0);
}
```

Or you can use one of the helper mixins (`relative`, `absolute`, `fixed`).

```scss
.cube {
    @include relative(top 100% left 0);
    @include absolute(left 0 right 50px);
    @include fixed(top 0 bottom 0);
}
```

### <a name="mixins-prefixing"></a> Prefixing

Do you want your animations and/or placeholder to work on every browser, use the `prefix` mixins.

```scss
@include placeholder { color: red; };
@include keyframes(slide) { color: red; };
@include animation('slide 5s 3');
```

## <a name="elements"></a> Elements
### <a name="elements-grid"></a> Grid

You can use the 12-column grid system by using the following classes:

```html
<div class="row">
    <div class="column--8"></div>
    <div class="column--4"></div>
</div>

<div class="row">
    <div class="column--2"></div>
    <div class="column--2"></div>
    <div class="column--2"></div>
    <div class="column--2"></div>
    <div class="column--2"></div>
    <div class="column--2"></div>
</div>
```

### <a name="elements-container"></a> Container

You should use the container element if you want to center some content with a fixed width (max: 1000px).

```html
<div class="container"></div>
```

## <a name="build"></a> Build
### <a name="build-once"></a> Once

If you want to create the CSS file yourself you can run one simple command to build the project.

```bash
npm run build
```

### <a name="build-watch"></a> Watch

If you want to make modifications to the project you can use the watch command to constantly watch all the `.scss` files.

```bash
npm run build:watch
```

## License
[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)