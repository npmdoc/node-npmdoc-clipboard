# npmdoc-clipboard

#### api documentation for  clipboard (v1.6.1)  [![npm package](https://img.shields.io/npm/v/npmdoc-clipboard.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-clipboard) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-clipboard.svg)](https://travis-ci.org/npmdoc/node-npmdoc-clipboard)

#### Modern copy to clipboard. No Flash. Just 2kb

[![NPM](https://nodei.co/npm/clipboard.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/clipboard)

- [https://npmdoc.github.io/node-npmdoc-clipboard/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-clipboard/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-clipboard/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-clipboard/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-clipboard/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-clipboard/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "clipboard",
    "version": "1.6.1",
    "description": "Modern copy to clipboard. No Flash. Just 2kb",
    "repository": "zenorocha/clipboard.js",
    "license": "MIT",
    "main": "lib/clipboard.js",
    "keywords": [
        "clipboard",
        "copy",
        "cut"
    ],
    "dependencies": {
        "good-listener": "^1.2.0",
        "select": "^1.1.2",
        "tiny-emitter": "^1.0.0"
    },
    "devDependencies": {
        "babel-cli": "^6.5.1",
        "babel-core": "^6.5.2",
        "babel-plugin-transform-es2015-modules-umd": "^6.5.0",
        "babel-preset-es2015": "^6.5.0",
        "babelify": "^7.2.0",
        "bannerify": "Vekat/bannerify#feature-option",
        "browserify": "^13.0.0",
        "chai": "^3.4.1",
        "install": "^0.8.1",
        "karma": "^1.3.0",
        "karma-browserify": "^5.0.1",
        "karma-chai": "^0.1.0",
        "karma-mocha": "^1.2.0",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-sinon": "^1.0.4",
        "mocha": "^3.1.2",
        "phantomjs-prebuilt": "^2.1.4",
        "sinon": "^1.17.2",
        "uglify-js": "^2.4.24",
        "watchify": "^3.4.0"
    },
    "scripts": {
        "build": "npm run build-debug && npm run build-min",
        "build-debug": "browserify src/clipboard.js -s Clipboard -t [babelify] -p [bannerify --file .banner ] -o dist/clipboard.js",
        "build-min": "uglifyjs dist/clipboard.js --comments '/!/' -m screw_ie8=true -c screw_ie8=true,unused=false -o dist/clipboard.min.js",
        "build-watch": "watchify src/clipboard.js -s Clipboard -t [babelify] -o dist/clipboard.js -v",
        "test": "karma start --single-run",
        "prepublish": "babel src --out-dir lib"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
