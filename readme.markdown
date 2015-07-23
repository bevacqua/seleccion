# seleccion

> A `getSelection` polyfill and a `setSelection` ranch dressing

Includes also a `setSelection` method. See also [sell][2] to work with selection within `<input>` and `<textarea>` elements.

# install

```shell
npm install seleccion
```

# `seleccion.getSelection`

Provides a polyfill for `window.getSelection`.

```js
var getSelection = require('seleccion').get;
```

- Defaults to `window.getSelection` if available
- Falls back to `document.selection`
- Falls back to a naïve null object if both are unavailable

# `seleccion.set(range)`

Provides a convenient cross-browser method to set the text selection using a `range` `TextRange`.

```js
var setSelection = require('seleccion').set;
setSelection({
  startContainer: document.querySelector('#some-span'),
  startOffset: 0,
  endContainer: document.querySelector('#another-span'),
  endOffset: 24,
  collapsed: false
});
```

# license

MIT

[1]: https://github.com/bevacqua/sell
