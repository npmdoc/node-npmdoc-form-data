# api documentation for  [form-data (v2.1.2)](https://github.com/form-data/form-data#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-form-data.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-form-data) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-form-data.svg)](https://travis-ci.org/npmdoc/node-npmdoc-form-data)
#### A library to create readable "multipart/form-data" streams. Can be used to submit forms and file uploads to other web applications.

[![NPM](https://nodei.co/npm/form-data.png?downloads=true)](https://www.npmjs.com/package/form-data)

[![apidoc](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-form-data_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-form-data/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-form-data/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Felix Geisendörfer",
        "email": "felix@debuggable.com",
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
        "shasum": "89c3534008b97eada4cbb157d58f6f5df025eae4",
        "tarball": "https://registry.npmjs.org/form-data/-/form-data-2.1.2.tgz"
    },
    "engines": {
        "node": ">= 0.12"
    },
    "gitHead": "03444d21961a7a44cdc2eae11ee3630f6969023d",
    "homepage": "https://github.com/form-data/form-data#readme",
    "license": "MIT",
    "main": "./lib/form_data",
    "maintainers": [
        {
            "name": "alexindigo",
            "email": "iam@alexindigo.com"
        },
        {
            "name": "dylanpiercey",
            "email": "pierceydylan@gmail.com"
        },
        {
            "name": "felixge",
            "email": "felix@debuggable.com"
        },
        {
            "name": "mikeal",
            "email": "mikeal.rogers@gmail.com"
        }
    ],
    "name": "form-data",
    "optionalDependencies": {},
    "pre-commit": [
        "lint",
        "ci-test",
        "check"
    ],
    "readme": "ERROR: No README data found!",
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
    "version": "2.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module form-data](#apidoc.module.form-data)
1.  [function <span class="apidocSignatureSpan">form-data.</span>super_ ()](#apidoc.element.form-data.super_)
1.  object <span class="apidocSignatureSpan">form-data.</span>super_.prototype
1.  string <span class="apidocSignatureSpan">form-data.</span>DEFAULT_CONTENT_TYPE
1.  string <span class="apidocSignatureSpan">form-data.</span>LINE_BREAK

#### [module form-data.super_](#apidoc.module.form-data.super_)
1.  [function <span class="apidocSignatureSpan">form-data.</span>super_ ()](#apidoc.element.form-data.super_.super_)
1.  [function <span class="apidocSignatureSpan">form-data.super_.</span>create (options)](#apidoc.element.form-data.super_.create)
1.  [function <span class="apidocSignatureSpan">form-data.super_.</span>isStreamLike (stream)](#apidoc.element.form-data.super_.isStreamLike)

#### [module form-data.super_.prototype](#apidoc.module.form-data.super_.prototype)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_checkDataSize ()](#apidoc.element.form-data.super_.prototype._checkDataSize)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_emitError (err)](#apidoc.element.form-data.super_.prototype._emitError)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_getNext ()](#apidoc.element.form-data.super_.prototype._getNext)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_handleErrors (stream)](#apidoc.element.form-data.super_.prototype._handleErrors)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_pipeNext (stream)](#apidoc.element.form-data.super_.prototype._pipeNext)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_reset ()](#apidoc.element.form-data.super_.prototype._reset)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_updateDataSize ()](#apidoc.element.form-data.super_.prototype._updateDataSize)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>append (stream)](#apidoc.element.form-data.super_.prototype.append)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>destroy ()](#apidoc.element.form-data.super_.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>end ()](#apidoc.element.form-data.super_.prototype.end)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>pause ()](#apidoc.element.form-data.super_.prototype.pause)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>pipe (dest, options)](#apidoc.element.form-data.super_.prototype.pipe)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>resume ()](#apidoc.element.form-data.super_.prototype.resume)
1.  [function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>write (data)](#apidoc.element.form-data.super_.prototype.write)



# <a name="apidoc.module.form-data"></a>[module form-data](#apidoc.module.form-data)

#### <a name="apidoc.element.form-data.super_"></a>[function <span class="apidocSignatureSpan">form-data.</span>super_ ()](#apidoc.element.form-data.super_)
- description and source-code
```javascript
function CombinedStream() {
  this.writable = false;
  this.readable = true;
  this.dataSize = 0;
  this.maxDataSize = 2 * 1024 * 1024;
  this.pauseStreams = true;

  this._released = false;
  this._streams = [];
  this._currentStream = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.form-data.super_"></a>[module form-data.super_](#apidoc.module.form-data.super_)

#### <a name="apidoc.element.form-data.super_.super_"></a>[function <span class="apidocSignatureSpan">form-data.</span>super_ ()](#apidoc.element.form-data.super_.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.create"></a>[function <span class="apidocSignatureSpan">form-data.super_.</span>create (options)](#apidoc.element.form-data.super_.create)
- description and source-code
```javascript
create = function (options) {
  var combinedStream = new this();

  options = options || {};
  for (var option in options) {
    combinedStream[option] = options[option];
  }

  return combinedStream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.isStreamLike"></a>[function <span class="apidocSignatureSpan">form-data.super_.</span>isStreamLike (stream)](#apidoc.element.form-data.super_.isStreamLike)
- description and source-code
```javascript
isStreamLike = function (stream) {
  return (typeof stream !== 'function')
    && (typeof stream !== 'string')
    && (typeof stream !== 'boolean')
    && (typeof stream !== 'number')
    && (!Buffer.isBuffer(stream));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.form-data.super_.prototype"></a>[module form-data.super_.prototype](#apidoc.module.form-data.super_.prototype)

#### <a name="apidoc.element.form-data.super_.prototype._checkDataSize"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_checkDataSize ()](#apidoc.element.form-data.super_.prototype._checkDataSize)
- description and source-code
```javascript
_checkDataSize = function () {
  this._updateDataSize();
  if (this.dataSize <= this.maxDataSize) {
    return;
  }

  var message =
    'DelayedStream#maxDataSize of ' + this.maxDataSize + ' bytes exceeded.';
  this._emitError(new Error(message));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._emitError"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_emitError (err)](#apidoc.element.form-data.super_.prototype._emitError)
- description and source-code
```javascript
_emitError = function (err) {
  this._reset();
  this.emit('error', err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._getNext"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_getNext ()](#apidoc.element.form-data.super_.prototype._getNext)
- description and source-code
```javascript
_getNext = function () {
  this._currentStream = null;
  var stream = this._streams.shift();


  if (typeof stream == 'undefined') {
    this.end();
    return;
  }

  if (typeof stream !== 'function') {
    this._pipeNext(stream);
    return;
  }

  var getStream = stream;
  getStream(function(stream) {
    var isStreamLike = CombinedStream.isStreamLike(stream);
    if (isStreamLike) {
      stream.on('data', this._checkDataSize.bind(this));
      this._handleErrors(stream);
    }

    this._pipeNext(stream);
  }.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._handleErrors"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_handleErrors (stream)](#apidoc.element.form-data.super_.prototype._handleErrors)
- description and source-code
```javascript
_handleErrors = function (stream) {
  var self = this;
  stream.on('error', function(err) {
    self._emitError(err);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._pipeNext"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_pipeNext (stream)](#apidoc.element.form-data.super_.prototype._pipeNext)
- description and source-code
```javascript
_pipeNext = function (stream) {
  this._currentStream = stream;

  var isStreamLike = CombinedStream.isStreamLike(stream);
  if (isStreamLike) {
    stream.on('end', this._getNext.bind(this));
    stream.pipe(this, {end: false});
    return;
  }

  var value = stream;
  this.write(value);
  this._getNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._reset"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_reset ()](#apidoc.element.form-data.super_.prototype._reset)
- description and source-code
```javascript
_reset = function () {
  this.writable = false;
  this._streams = [];
  this._currentStream = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype._updateDataSize"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>_updateDataSize ()](#apidoc.element.form-data.super_.prototype._updateDataSize)
- description and source-code
```javascript
_updateDataSize = function () {
  this.dataSize = 0;

  var self = this;
  this._streams.forEach(function(stream) {
    if (!stream.dataSize) {
      return;
    }

    self.dataSize += stream.dataSize;
  });

  if (this._currentStream && this._currentStream.dataSize) {
    this.dataSize += this._currentStream.dataSize;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype.append"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>append (stream)](#apidoc.element.form-data.super_.prototype.append)
- description and source-code
```javascript
append = function (stream) {
  var isStreamLike = CombinedStream.isStreamLike(stream);

  if (isStreamLike) {
    if (!(stream instanceof DelayedStream)) {
      var newStream = DelayedStream.create(stream, {
        maxDataSize: Infinity,
        pauseStream: this.pauseStreams,
      });
      stream.on('data', this._checkDataSize.bind(this));
      stream = newStream;
    }

    this._handleErrors(stream);

    if (this.pauseStreams) {
      stream.pause();
    }
  }

  this._streams.push(stream);
  return this;
}
```
- example usage
```shell
...
a buffer and a file stream.

''' javascript
var FormData = require('form-data');
var fs = require('fs');

var form = new FormData();
form.append('my_field', 'my value');
form.append('my_buffer', new Buffer(10));
form.append('my_file', fs.createReadStream('/foo/bar.jpg'));
'''

Also you can use http-response stream:

''' javascript
...
```

#### <a name="apidoc.element.form-data.super_.prototype.destroy"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>destroy ()](#apidoc.element.form-data.super_.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  this._reset();
  this.emit('close');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype.end"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>end ()](#apidoc.element.form-data.super_.prototype.end)
- description and source-code
```javascript
end = function () {
  this._reset();
  this.emit('end');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype.pause"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>pause ()](#apidoc.element.form-data.super_.prototype.pause)
- description and source-code
```javascript
pause = function () {
  if (!this.pauseStreams) {
    return;
  }

  if(this.pauseStreams && this._currentStream && typeof(this._currentStream.pause) == 'function') this._currentStream.pause();
  this.emit('pause');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.form-data.super_.prototype.pipe"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>pipe (dest, options)](#apidoc.element.form-data.super_.prototype.pipe)
- description and source-code
```javascript
pipe = function (dest, options) {
  Stream.prototype.pipe.call(this, dest, options);
  this.resume();
  return dest;
}
```
- example usage
```shell
...
var request = http.request({
  method: 'post',
  host: 'example.org',
  path: '/upload',
  headers: form.getHeaders()
});

form.pipe(request);

request.on('response', function(res) {
  console.log(res.statusCode);
});
'''

Or if you would prefer the ''Content-Length'' header to be set for you:
...
```

#### <a name="apidoc.element.form-data.super_.prototype.resume"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>resume ()](#apidoc.element.form-data.super_.prototype.resume)
- description and source-code
```javascript
resume = function () {
  if (!this._released) {
    this._released = true;
    this.writable = true;
    this._getNext();
  }

  if(this.pauseStreams && this._currentStream && typeof(this._currentStream.resume) == 'function') this._currentStream.resume();
  this.emit('resume');
}
```
- example usage
```shell
...
'''

In order to submit this form to a web application, call '''submit(url, [callback])''' method:

''' javascript
form.submit('http://example.org/', function(err, res) {
  // res – response object (http.IncomingMessage)  //
  res.resume();
});

'''

For more advanced request manipulations '''submit()''' method returns '''http.ClientRequest''' object, or you can choose from one
 of the alternative submission methods.

### Alternative submission methods
...
```

#### <a name="apidoc.element.form-data.super_.prototype.write"></a>[function <span class="apidocSignatureSpan">form-data.super_.prototype.</span>write (data)](#apidoc.element.form-data.super_.prototype.write)
- description and source-code
```javascript
write = function (data) {
  this.emit('data', data);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
