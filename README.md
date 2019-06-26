# react-clear-cache

> A component to manage application updates.

[![NPM](https://img.shields.io/npm/v/react-clear-cache.svg)](https://www.npmjs.com/package/react-clear-cache) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Demo

See [demo](https://noahjohn9259.github.io/react-clear-cache/)

## Install

```bash
$ npm install --save react-clear-cache
```

## Add script in package.json

This will generate `meta.json` file. This will have the version key with the latest build.

```bash
{
  "prebuild": "npm run generate-build-meta",
  "generate-build-meta": "./node_modules/react-clear-cache/bin/cli.js"
}
```

## Usage

```tsx
import * as React from 'react';

import ClearCache from 'react-clear-cache';

const App: React.FC<{}> = () => {
  return (
    <div>
      <ClearCache>
        {({ loading, latestVersion, isLatestVersion, emptyCacheStorage }) =>
          <div>App works!</div>
        }
      </ClearCache>
    </div>
  );
};

export default App;
```

## Props

### `duration`: number

You can set the duration when to fetch for new updates.

## Render prop function

### `loading`: boolean

A boolean that indicates whether the request is in flight

### `latestVersion`: string

A string containing the latest version number of the build.

### `isLatestVersion`: boolean

A boolean that indicates if the user has the latest version.

### `emptyCacheStorage`: () => void

This function empty the CacheStorage and reloads the page.

## Contributors

1. [noahjohn9259](https://github.com/noahjohn9259)

## License

MIT © [noahjohn9259](https://github.com/noahjohn9259)