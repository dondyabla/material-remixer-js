# <img align="center" src="docs/assets/remixer_logo_32x32.png"> Remixer for JavaScript

[![Build Status](https://travis-ci.org/material-foundation/material-remixer-js.svg?branch=develop)](https://travis-ci.org/material-foundation/material-remixer-js) [![codecov](https://codecov.io/gh/material-foundation/material-remixer-js/branch/develop/graph/badge.svg)](https://codecov.io/gh/material-foundation/material-remixer-js) [![npm version](https://badge.fury.io/js/material-remixer.svg)](https://badge.fury.io/js/material-remixer)

Remixer is a framework to iterate quickly on UI changes by allowing you to adjust UI variables without needing to rebuild (or even restart) your app. You can adjust Numbers, Colors, Booleans, and Strings. To see it in action check out the [example app](https://github.com/material-foundation/material-remixer-js/tree/develop/examples).

If you are interested in using Remixer in another platform, you may want to check out the [iOS](https://github.com/material-foundation/material-remixer-ios) and [Android](https://github.com/material-foundation/material-remixer-android) repos. With any of the three platforms you can use the [Remote Controller](https://github.com/material-foundation/material-remixer-remote-web) to change the variables from a web dashboard.

**New to Remixer?** Visit our [main repo](https://github.com/material-foundation/material-remixer) to get a full description of what it is and how it works.
- - -

## Quickstart

### 1. Use [`npm`](https://www.npmjs.com/) to install as dependency.

`npm install material-remixer --save`

This will install the Remixer files in your project's `node_modules` folder.

### 2. Include the `remixer.js` script in your app.

```html
<script src="./node_modules/material-remixer/dist/remixer.js"></script>
```

### 3. Begin by starting Remixer.

```javascript
remixer.start();
```

### 4. Add variables.
Now you can add any desired variables and use the callback method to assign the `selectedValue` property.

```javascript
// Add a boolean variable to generate a toggle switch in the overlay.
remixer.addBooleanVariable("show", true, function(variable) {
  document.getElementById("box").style.display = variable.selectedValue ? "block" : "none";
});
```

## Is material-foundation affiliated with Google?

Yes, the [material-foundation](https://github.com/material-foundation) organization is one of Google's new homes for tools and frameworks related to our [Material Design](https://material.io) system. Please check out our blog post [Design is Never Done](https://design.google.com/articles/design-is-never-done/) for more information regarding Material Design and how Remixer integrates with the system.

## Contributing

We gladly welcome contributions! If you have found a bug, have questions, or wish to contribute, please follow our [Contributing Guidelines](https://github.com/material-foundation/material-remixer-js/blob/develop/CONTRIBUTING.md).

## License

© Google, 2016. Licensed under an [Apache-2](https://github.com/material-foundation/material-remixer-js/blob/develop/LICENSE) license.
