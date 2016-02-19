# unpack-content

Extract header data and body from plaintext (Markdown-ish) markup source.

## Install

```sh
$ npm install --save unpack-content
```

## Usage

Given content in file `content.md`:

```
---
tags: foo bar baz
---

# Content

Hi there!
```

Unpack the metadata from the rest using:

```js
import fs from 'fs';
import unpackContent from 'unpack-content';

const contentString = fs.readFileSync('content.md').toString();
const {text, tags, ...metadata} = unpackContent(contentString);
```

## Development

### Interesting `gulp` targets

- `flow`: Check types.
- `lint`: Run linter.
- `test`: Run tests.
- `babel`: Transform ES2015 JS (in `src/`) to ES5 (in `dist/`).
- `build`: All of the above.

## Links

- Source: [github.com/wincent/unpack-content](https://github.com/wincent/unpack-content)
- Package: [www.npmjs.com/package/unpack-content](https://www.npmjs.com/package/unpack-content)

## License

### The MIT License (MIT)

Copyright (c) 2015-present Greg Hurrell

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
