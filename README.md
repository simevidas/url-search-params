url-search-params
=================

[![build status](https://secure.travis-ci.org/WebReflection/url-search-params.png)](http://travis-ci.org/WebReflection/url-search-params)

This is a polyfill for the [URLSearchParams API](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams).

It is possible to simply include [build/url-search-params.js](build/url-search-params.js) or grab it via npm.

```
npm install url-search-params
```

The function is exported directly.
```js
var URLSearchParams = require('url-search-params');
```

MIT Style License

#### About HTMLAnchroElement.prototype.searchParams
This property is already implemented in Firefox and polyfilled here only for browsers that exposes getters and setters
through the `HTMLAnchroElement.prototype`.

In order to know if such property is supported, you **must** do the check as such:
```
if ('searchParams' in HTMLAnchroElement.prototype) {
  // polyfill for <a> links supported
}
```
If you do this check instead:
```js
if (HTMLAnchroElement.prototype.searchParams) {
  // throws a TypeError
}
```
this polyfill will reflect natiive behavior, throwing a type error due access to a property in a non instance of `HTMLAnchroElement`.

Nothing new to learn here, [just a reminder](http://webreflection.blogspot.co.uk/2011/08/please-stop-reassigning-for-no-reason.html).