# React iFrame [![CircleCI Status](https://circleci.com/gh/nicholasadamou/react-iframe.svg?style=svg)](https://circleci.com/gh/nicholasadamou/react-iframe) [![NPM](https://img.shields.io/npm/v/react-iframe.svg)](https://www.npmjs.com/package/react-iframe) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

_Have you ever needed to add headers to an iframe? You've come to the right place!_

## Getting Started

React iFrame is a simple react component that lets you add headers to an iframe. It's super light-weight and requires no external dependencies!

**No dependencies!**

**Much 🔥!**

**Only ~700b!**

## Installation

You can download the package using `npm` with:

```bash
npm install --save @nicholasadamou/react-iframe
```

## Usage (Simple)

To use, simply import the component and specify your `src` and `headers`:

```js
import Iframe from "@nicholasadamou/react-iframe";

const token = localStorage.getItem("token") || new Cookies().get("token");

<Iframe
 src="/chatbot?mode=embedded"
 headers={{
  Authorization: `Bearer ${token}`,
  type: "text/html",
 }}
/>;
```

## Development

Local development is broken into two parts (ideally using two tabs).

First, run rollup to watch your `src/` module and automatically recompile it into `dist/` whenever you make changes.

```bash
npm start # runs rollup with watch flag
```

The second part will be running the `example/` create-react-app that's linked to the local version of your module.

```bash
# (in another tab)
cd example
npm start # runs create-react-app dev server
```

Now, anytime you make a change to your library in `src/` or to the example app's `example/src`, `create-react-app` will live-reload your local dev server so you can iterate on your component in real-time.

## Publishing to npm

```bash
npm publish
```

This builds `commonjs` and `es` versions of your module to `dist/` and then publishes your module to `npm`.

Make sure that any npm modules you want as peer dependencies are properly marked as `peerDependencies` in `package.json`. The rollup config will automatically recognize them as peers and not try to bundle them in your module.

## License

© Nicholas Adamou.

It is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE
