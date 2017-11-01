# `SCSS-starter`

Simply add SCSS starters to your web project.

## <a name="get-started"></a> Get Started

### <a name="installation"></a> Installation

You can install this package locally with npm or yarn.

```bash
# To get the latest stable version

npm install @bravobit/scss-starter --save

# or

yarn add @bravobit/scss-starter
```

### <a name="usage"></a> Usage

If you want to use the mixins and are working in an `.scss` file You should import our `styles.scss` file into your project to get the full product.

```scss
@import '~@bravobit/scss-starter/src/styles.scss';
```

If you want to include our default styling in your HTML you can use the compiled (and minified) version.

```html
<link rel="stylesheet" href="%RELATIVE_NODE_MODULES%/@bravobit/scss-starter/dist/styles.css">
```