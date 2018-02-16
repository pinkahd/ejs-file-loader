# Webpack EJS Template Loader

[![Build Status](https://travis-ci.org/pinkahd/ejs-file-loader.svg?branch=master)](https://travis-ci.org/pinkahd/ejs-file-loader)

> EJS loader for [webpack](http://webpack.github.io/). Uses [ejs](https://github.com/mde/ejs) function to compile templates.

## :cloud: Installation

`npm i -D ejs-file-loader`

## :clipboard: Example

### JavaScript

``` javascript
var template = require("ejs-file-loader!./file.ejs");
// => returns the template function compiled with ejs templating engine.

// And then use it somewhere in your code
template(data) // Pass object with data

// Child Templates
// path is relative to where webpack is being run
<%- include templates/child -%>
```

## :memo: Documentation

[Documentation: Using loaders](http://webpack.github.io/docs/using-loaders.html)

Following options can be specified in query:

`beautify` — enable or disable uglify-js beautify of template ast

`compileDebug` — see ejs compileDebug option

`htmlmin` — see [htmlminify section](#htmlminify)

## htmlminify

```javascript
module: {
  loaders: [
    {test: /\.ejs$/, loader: 'ejs-file-loader?htmlmin'} // enable here
  ]
},
'ejs-compiled-loader': {
  'htmlmin': true, // or enable here
  'htmlminOptions': {
    removeComments: true
  }
}
```

See [all options reference](https://github.com/kangax/html-minifier#options-quick-reference)

## :scroll: License

[MIT](http://www.opensource.org/licenses/mit-license.php)



