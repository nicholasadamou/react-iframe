# React iFrame

_Have you ever needed to add headers to an iframe? You've come to the right place!_

## Getting Started

React iFrame is a simple react component that lets you add headers to an iframe. It's super light-weight and requires no external dependencies!

## Installation

Copy the contents of [Iframe.js](Iframe.js) or download the file and place it into your project's components directory.

## Usage (Simple)

To use, simply import the component and specify your `src` and `headers`:

```js
import Iframe from "@components/Iframe"; // Assuming 'Iframe.js' is in your components directory.

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
