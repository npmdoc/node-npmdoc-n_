# npmdoc-n_

#### api documentation for  [n_ (v1.4.4)](https://github.com/borisdiakur/n_#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-n_.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-n_) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-n_.svg)](https://travis-ci.org/npmdoc/node-npmdoc-n_)

#### lodash REPL

[![NPM](https://nodei.co/npm/n_.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/n_)

- [https://npmdoc.github.io/node-npmdoc-n_/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-n_/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-n_/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Boris Diakur",
        "url": "https://github.com/borisdiakur"
    },
    "bin": {
        "n_": "./bin/n_",
        "n_3": "./bin/n_3"
    },
    "bugs": {
        "url": "https://github.com/borisdiakur/n_/issues"
    },
    "contributors": [
        {
            "name": "Boris Diakur",
            "url": "https://github.com/borisdiakur"
        },
        {
            "name": "John-David Dalton",
            "url": "http://allyoucanleet.com/"
        }
    ],
    "dependencies": {
        "lodash": "^4.0.0",
        "os-homedir": "^1.0.1",
        "repl.history": "^0.1.3",
        "tar.gz": "^1.0.5"
    },
    "description": "lodash REPL",
    "devDependencies": {
        "coveralls": "^2.11.2",
        "istanbul": "^0.4.2",
        "jshint": "^2.7.0",
        "mocha": "^3.2.0",
        "mocha-lcov-reporter": "0.0.2"
    },
    "directories": {},
    "dist": {
        "shasum": "0b7229c02b0740ec13c43edc83dc3cbc428725c7",
        "tarball": "https://registry.npmjs.org/n_/-/n_-1.4.4.tgz"
    },
    "engines": {
        "node": ">=0.8.0"
    },
    "gitHead": "ad79e1fde56da86135bcb11796c12883d06c6b5a",
    "homepage": "https://github.com/borisdiakur/n_#readme",
    "keywords": [
        "_",
        "cli",
        "console",
        "lodash",
        "underscore",
        "repl",
        "shell",
        "terminal"
    ],
    "license": "MIT",
    "main": "./lib/n_",
    "maintainers": [
        {
            "name": "borisdiakur"
        },
        {
            "name": "jdalton"
        }
    ],
    "name": "n_",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/borisdiakur/n_.git"
    },
    "scripts": {
        "coveralls": "rm -rf coverage && istanbul cover ./node_modules/mocha/bin/_mocha --report lcovonly -- -R spec && cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js && rm -rf ./coverage",
        "istanbul": "rm -rf coverage && istanbul cover ./node_modules/mocha/bin/_mocha --report html && open coverage/lib/n_.js.html",
        "jshint": "jshint .",
        "mocha": "mocha --reporter min test",
        "postinstall": "npm pack lodash@^3 ; targz extract lodash-3.*.tgz extraneous/lodash3",
        "test": "npm run postinstall ; mocha test && npm run jshint"
    },
    "version": "1.4.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
