# `@bravobit/scss-starter`

This NPM dependency contains css-resets, standard variables and it also contains mixins to help you develop your web project.

## <a name="get-started"></a> Get Started

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

## <a name="build"></a> Build

### <a name="build-single"></a> Single

If you want to create the CSS file yourself you can run one simple command to build the project.

```bash
npm run build
```

### <a name="build-watch"></a> Watch

If you want to make modifications to the project you can use the watch command to constantly watch all the `.scss` files.

```bash
npm run build:watch
```
