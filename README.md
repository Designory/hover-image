# Hover Image

A generic library to swap out an image on hover.

<img src="https://raw.githubusercontent.com/Designory/hover-image/master/docs/dog.gif" width="250">

[Photos by Daniel Brubaker on Unsplash](https://unsplash.com/@dpmb87?utm_medium=referral)

## Install

```
$ npm install @designory/hover-image
# or
$ yarn global add @designory/hover-image
```

## Usage

Place your configured `hoverSrcAttribute` (which defaults to `data-hover-src`)
on an `<img>` tag.

```html
<img src="original.jpg" data-hover-src="hover.jpg">
```

```javascript
import initializeHoverImage from '@designory/hover-image';
// Or, if non-transpiled:
// const initializeHoverImage = require('@designory/hover-image').default;

initializeHoverImage({
    hoverSrcAttribute,
    orginalSrcAttribute,
    classToggle,
    preloadHoverImages,
});
```

### Options

#### `hoverSrcAttribute`

The data attribute the library will attach its delegated events to.

Defaults to `'data-hover-src'`.

#### `orginalSrcAttribute`

The name of the data attribute the library will save the original source URL while the image is swapped out.

Defaults to `'data-original-src'`.

#### `classToggle`

The class that will get toggled while the image is swapped out on hover.

Defaults to `'is-hovered'`.

#### `preloadHoverImages`

When true, will make a network request for all images specified within the `hoverSrcAttribute` before the initial `mouseover` event has fired. If the browser is caching network requests, this should help eliminate the slight empty flash the user sees when hovering over the image for the first time.

Defaults to `true`.

### License

[MIT](./LICENSE)

### Author

[Matt Wade](https://github.com/romellem/)
