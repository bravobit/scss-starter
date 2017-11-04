# `@bravobit/scss-starter`

> CSS-resets, standard variables and it also contains mixins to help you develop your web project.

- Use <kbd>command</kbd> + <kbd>F</kbd> or <kbd>ctrl</kbd> + <kbd>F</kbd> to search for a keyword.
- Contributions welcome, please see [contribution guide](CONTRIBUTING.md).

## Contents
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Usage](#usage)
- [Mixins](#mixins)
  - [Device](#mixins-device)
  - [Positioning](#mixins-positioning)
  - [Prefixing](#mixins-prefixing)
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