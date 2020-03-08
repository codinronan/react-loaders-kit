# React Spinners Kit

A simple yet robust and comprehensive collection of loading animations made with React.js based on inspiration from designers and developers on codepen.

This package was made using the [Emotion](https://emotion.sh/docs/introduction) css library.

## Demo Page

All loaders can be found on the demo page 

- [Demo Page](https://seimodei.github.io/react-loaders-kit-examples/)

## Installation

With Yarn:

### `yarn add react-loaders-kit`

With npm:

### `npm install --save react-loaders-kit`

## Usage

All loaders come with their own default properties. You have the option to overwrite these properties by passing in your own props into the loaders.

**IMPORTANT**: All loaders accept a `loading` prop as a boolean that is `required`. Without passing the loading prop, an `error` is thrown. The loader will render `none` if `loading` is `false`.

### Example

```js
import React, {useState} from "react";
import { BarsLoader } from 'react-loaders-kit';

//or

import BarsLoader from 'react-loaders-kit/lib/bars/BarsLoader'; // Recommended to reduce bundle size

const MyWonderfulComponent = () => {
    const [loading, setLoading] = useState(true);

    const loaderProps = {
        loading,
        size: 35,
        duration: 1,
        colors: ['#5e22f0', '#f6b93b']
    }

    return (
        <BarsLoader {...loaderProps} />
    )
}

```

## Available Loaders, PropTypes, and Default Values

Common default props for all loaders:

``js
loading: true;
pause: false;
``

**IMPORTANT**: The `loading` prop is `REQUIRED` and needs to be passed for the loader to display.

### `pause` props

All loaders accept a `pause` prop which is a boolean. If `pause` is `true`, the animation is paused else it deafults to `playing`.

### `color` & `colors` props

Some loaders accept a `color` prop which is a color hash string in the format of `#XXXXXX` or `#XXX`.

Other loaders which have more customization accept a `colors` prop which is a string array of colors in the format of `['#XXXXXX', '#XXXXXX', ...]` or `['#XXX', '#XXX', ...]`.

### All loaders

#### `<AlternatingOrbitsLoader />`

| size: number | colors: string[]     |
| -------------|----------------------|
| 50           |['#5e22f0', '#f6b93b']|

## Contributing

- Pull requests and ⭐ stars are always welcome
- For bugs and feature requests, please create an issue

## License

MIT