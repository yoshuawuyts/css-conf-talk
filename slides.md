# C H O O O
# C H O O O
# C H O O O
# C H O O O
# C H O O O

---

# Hello world!

```js
var html = require('choo/html')
var choo = require('choo')

var app = choo()
app.route(mainView)
app.mount('body')

function mainView () {
  return html`<body>hello world</body>`
}
```

---

# Cool

---

# Thanks
# Thanks
# Thanks
# Thanks
# Thanks

---

# CSS

- reuse between projects
- npm install
- project-specific CSS

---
# npm install
```sh
$ npm install tachyons
```

---

# reuse between projects

```js
var css = require('sheetify')
css('tachyons')
```

---

# reuse between projects

```js
var css = require('sheetify')
css('dat-colors')
```

---

# project specific CSS
```js
var css = require('sheetify')
css`
  .foo { color: blue }
`
```

---

# component specific CSS
```js
var css = require('sheetify')
var myStyle = css`
  :host { color: blue }
`
```

---

# component specific CSS
```js
var html = require('choo/html')
var css = require('sheetify')

var myStyle = css`
  :host { color: blue }
`

var myEl = html`<div class=${myStyle}>hi</div>`
```

---

# benefits

- write JS, HTML and CSS in 1 file
- no runtime overhead

---

# shipping components on npm

Package.json
```js
{
  "browserify": {
    "transform": [
      "sheetify/transform"
    ]
  }
}
```

---

# zero config compiler
```sh
$ npm i -g bankai
$ bankai start
$ bankai build
$ bankai inspect
```

---

# Thanks
# Thanks
# Thanks
# Thanks
# Thanks
