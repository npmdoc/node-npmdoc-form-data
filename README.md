# npmdoc-form-data

#### basic api documentation for  [form-data (v2.1.4)](https://github.com/form-data/form-data#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-form-data.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-form-data) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-form-data.svg)](https://travis-ci.org/npmdoc/node-npmdoc-form-data)

#### A library to create readable "multipart/form-data" streams. Can be used to submit forms and file uploads to other web applications.

[![NPM](https://nodei.co/npm/form-data.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/form-data)

- [https://npmdoc.github.io/node-npmdoc-form-data/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-form-data/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-form-data/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Felix Geisendörfer",
        "url": "http://debuggable.com/"
    },
    "browser": "./lib/browser",
    "bugs": {
        "url": "https://github.com/form-data/form-data/issues"
    },
    "dependencies": {
        "asynckit": "^0.4.0",
        "combined-stream": "^1.0.5",
        "mime-types": "^2.1.12"
    },
    "description": "A library to create readable \"multipart/form-data\" streams. Can be used to submit forms and file uploads to other web applications.",
    "devDependencies": {
        "browserify": "^13.1.1",
        "browserify-istanbul": "^2.0.0",
        "coveralls": "^2.11.14",
        "cross-spawn": "^4.0.2",
        "eslint": "^3.9.1",
        "fake": "^0.2.2",
        "far": "^0.0.7",
        "formidable": "^1.0.17",
        "in-publish": "^2.0.0",
        "is-node-modern": "^1.0.0",
        "istanbul": "^0.4.5",
        "obake": "^0.1.2",
        "phantomjs-prebuilt": "^2.1.13",
        "pkgfiles": "^2.3.0",
        "pre-commit": "^1.1.3",
        "request": "2.76.0",
        "rimraf": "^2.5.4",
        "tape": "^4.6.2"
    },
    "directories": {},
    "dist": {
        "shasum": "33c183acf193276ecaa98143a69e94bfee1750d1",
        "tarball": "https://registry.npmjs.org/form-data/-/form-data-2.1.4.tgz"
    },
    "engines": {
        "node": ">= 0.12"
    },
    "gitHead": "d7398c3e7cd81ed12ecc0b84363721bae467db02",
    "homepage": "https://github.com/form-data/form-data#readme",
    "license": "MIT",
    "main": "./lib/form_data",
    "maintainers": [
        {
            "name": "alexindigo"
        },
        {
            "name": "dylanpiercey"
        },
        {
            "name": "felixge"
        },
        {
            "name": "mikeal"
        }
    ],
    "name": "form-data",
    "optionalDependencies": {},
    "pre-commit": [
        "lint",
        "ci-test",
        "check"
    ],
    "repository": {
        "type": "git",
        "url": "git://github.com/form-data/form-data.git"
    },
    "scripts": {
        "browser": "browserify -t browserify-istanbul test/run-browser.js | obake --coverage",
        "check": "istanbul check-coverage coverage/coverage*.json",
        "ci-lint": "is-node-modern 6 && npm run lint || is-node-not-modern 6",
        "ci-test": "npm run test && npm run browser && npm run report",
        "debug": "verbose=1 ./test/run.js",
        "files": "pkgfiles --sort=name",
        "get-version": "node -e \"console.log(require('./package.json').version)\"",
        "lint": "eslint lib/*.js test/*.js test/integration/*.js",
        "postpublish": "npm run restore-readme",
        "posttest": "istanbul report lcov text",
        "predebug": "rimraf coverage test/tmp",
        "prepublish": "in-publish && npm run update-readme || not-in-publish",
        "pretest": "rimraf coverage test/tmp",
        "report": "istanbul report lcov text",
        "restore-readme": "mv README.md.bak README.md",
        "test": "istanbul cover test/run.js",
        "update-readme": "sed -i.bak 's/\\/master\\.svg/\\/v'$(npm --silent run get-version)'.svg/g' README.md"
    },
    "version": "2.1.4",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
