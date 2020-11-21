# React iFrame [![Build Status](https://travis-ci.org/nicholasadamou/react-iframe.svg?branch=master)](https://travis-ci.org/nicholasadamou/react-iframe)

_Have you ever needed to add headers to a iframe? You've come to the right place!_

## Getting Started

React iFrame is a simple react component that lets you add headers to a iframe. It's super light-weight and requires no external dependencies!

## Installation

You can download the package using `npm` with:

`npm install @nicholasadamou/react-iframe --save`

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

## License

© Nicholas Adamou.

It is free software, and may be redistributed under the terms specified in the [LICENSE] file.

[license]: LICENSE
