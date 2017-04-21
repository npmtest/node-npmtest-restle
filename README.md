# npmtest-restle

#### basic test coverage for  [restle (v0.6.0)](http://restle.io)  [![npm package](https://img.shields.io/npm/v/npmtest-restle.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-restle) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-restle.svg)](https://travis-ci.org/npmtest/node-npmtest-restle)

#### JSON API engine.

[![NPM](https://nodei.co/npm/restle.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/restle)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-restle/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-restle/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-restle/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-restle/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-restle/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-restle/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-restle/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-restle/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-restle/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-restle/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-restle/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-restle/build/test-report.html](https://npmtest.github.io/node-npmtest-restle/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-restle/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-restle/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-restle/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-restle/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-restle/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-restle/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-restle/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-restle/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "restle",
    "version": "0.6.0",
    "description": "JSON API engine.",
    "main": "dist/lib/index.js",
    "repository": {
        "type": "git",
        "url": "https://github.com/dylnslck/restle.git"
    },
    "keywords": [
        "rest",
        "api",
        "express",
        "node",
        "ember-data"
    ],
    "author": "Dylan Slack <dylanslack@gmail.com> (http://dylanslack.com/)",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/dylnslck/restle/issues"
    },
    "homepage": "http://restle.io",
    "dependencies": {
        "babel": "^5.6.14",
        "bluebird": "^2.9.34",
        "body-parser": "^1.10.1",
        "commander": "^2.8.1",
        "cors": "^2.7.1",
        "error-class": "^2.0.0",
        "express": "^4.7.2",
        "i": "^0.3.3",
        "lodash": "^3.10.1",
        "prompt": "^0.2.14",
        "restle-error": "0.0.5",
        "restle-memory": "^0.1.0",
        "string-template": "^0.2.1"
    },
    "bin": {
        "restle": "./bin/restle"
    },
    "devDependencies": {
        "babel-eslint": "^4.0.5",
        "coveralls": "^2.11.3",
        "documentation": "^3.0.4",
        "eslint": "^0.24.1",
        "faker": "^3.0.1",
        "mkdirp": "^0.5.1",
        "rimraf": "^2.4.0",
        "superagent-as-promised": "^3.2.1",
        "supertest": "^1.0.1",
        "tap-spec": "^4.0.2",
        "tape": "^4.2.1"
    },
    "scripts": {
        "clean": "rimraf dist coverage",
        "prepublish": "npm run clean && npm run build",
        "build": "npm run build:lib && npm run build:test",
        "build:lib": "mkdirp dist/lib && babel lib --out-dir dist/lib",
        "build:test": "mkdirp dist/test && babel test --out-dir dist/test",
        "test": "npm run test:lint && npm run test:server",
        "test:lint": "eslint lib test",
        "test:server": "npm run clean && npm run build && tape dist/test | tap-spec",
        "test:coverage": "istanbul cover dist/test"
    },
    "files": [
        "dist/lib",
        "dist/test",
        "lib/",
        "test/",
        "bin/",
        "LICENSE"
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
