# api documentation for  [n_ (v1.4.4)](https://github.com/borisdiakur/n_#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-n_.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-n_) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-n_.svg)](https://travis-ci.org/npmdoc/node-npmdoc-n_)
#### lodash REPL

[![NPM](https://nodei.co/npm/n_.png?downloads=true)](https://www.npmjs.com/package/n_)

[![apidoc](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-n__2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-n_/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Boris Diakur",
        "email": "contact@borisdiakur.com",
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
            "email": "contact@borisdiakur.com",
            "url": "https://github.com/borisdiakur"
        },
        {
            "name": "John-David Dalton",
            "email": "john.david.dalton@gmail.com",
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
            "name": "borisdiakur",
            "email": "contact@borisdiakur.com"
        },
        {
            "name": "jdalton",
            "email": "john.david.dalton@gmail.com"
        }
    ],
    "name": "n_",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module n_](#apidoc.module.n_)
1.  boolean <span class="apidocSignatureSpan">n_.</span>_inTemplateLiteral
1.  boolean <span class="apidocSignatureSpan">n_.</span>_sawKeyPress
1.  boolean <span class="apidocSignatureSpan">n_.</span>breakEvalOnSigint
1.  boolean <span class="apidocSignatureSpan">n_.</span>editorMode
1.  boolean <span class="apidocSignatureSpan">n_.</span>ignoreUndefined
1.  boolean <span class="apidocSignatureSpan">n_.</span>isCompletionEnabled
1.  boolean <span class="apidocSignatureSpan">n_.</span>terminal
1.  boolean <span class="apidocSignatureSpan">n_.</span>underscoreAssigned
1.  boolean <span class="apidocSignatureSpan">n_.</span>useColors
1.  boolean <span class="apidocSignatureSpan">n_.</span>useGlobal
1.  [function <span class="apidocSignatureSpan">n_.</span>_ttyWrite (d, key)](#apidoc.element.n_._ttyWrite)
1.  [function <span class="apidocSignatureSpan">n_.</span>completer (text, cb)](#apidoc.element.n_.completer)
1.  [function <span class="apidocSignatureSpan">n_.</span>context.Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer)
1.  [function <span class="apidocSignatureSpan">n_.</span>context.require (path)](#apidoc.element.n_.context.require)
1.  [function <span class="apidocSignatureSpan">n_.</span>eval ()](#apidoc.element.n_.eval)
1.  [function <span class="apidocSignatureSpan">n_.</span>writer (obj, showHidden, depth)](#apidoc.element.n_.writer)
1.  number <span class="apidocSignatureSpan">n_.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">n_.</span>_sawReturnAt
1.  number <span class="apidocSignatureSpan">n_.</span>crlfDelay
1.  number <span class="apidocSignatureSpan">n_.</span>cursor
1.  number <span class="apidocSignatureSpan">n_.</span>historyIndex
1.  number <span class="apidocSignatureSpan">n_.</span>historySize
1.  number <span class="apidocSignatureSpan">n_.</span>prevRows
1.  object <span class="apidocSignatureSpan">n_.</span>_domain
1.  object <span class="apidocSignatureSpan">n_.</span>_events
1.  object <span class="apidocSignatureSpan">n_.</span>_events.close
1.  object <span class="apidocSignatureSpan">n_.</span>commands
1.  object <span class="apidocSignatureSpan">n_.</span>context
1.  object <span class="apidocSignatureSpan">n_.</span>context.Buffer.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.console
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2.FormData.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2.HtmlReport.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2.Instrumenter.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2.TextReport.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2._DbTable.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2_moduleExports
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2_moduleExports.FormData.prototype
1.  object <span class="apidocSignatureSpan">n_.</span>context.utility2_serverRepl1
1.  object <span class="apidocSignatureSpan">n_.</span>domain
1.  object <span class="apidocSignatureSpan">n_.</span>history
1.  object <span class="apidocSignatureSpan">n_.</span>input
1.  object <span class="apidocSignatureSpan">n_.</span>inputStream
1.  object <span class="apidocSignatureSpan">n_.</span>inputStream._events
1.  object <span class="apidocSignatureSpan">n_.</span>inputStream._handle
1.  object <span class="apidocSignatureSpan">n_.</span>inputStream._writableState
1.  object <span class="apidocSignatureSpan">n_.</span>lineParser
1.  object <span class="apidocSignatureSpan">n_.</span>lines
1.  object <span class="apidocSignatureSpan">n_.</span>output
1.  object <span class="apidocSignatureSpan">n_.</span>outputStream
1.  object <span class="apidocSignatureSpan">n_.</span>outputStream._events
1.  object <span class="apidocSignatureSpan">n_.</span>outputStream._handle
1.  object <span class="apidocSignatureSpan">n_.</span>outputStream._writableState
1.  object <span class="apidocSignatureSpan">n_.</span>rli
1.  string <span class="apidocSignatureSpan">n_.</span>_initialPrompt
1.  string <span class="apidocSignatureSpan">n_.</span>_prompt
1.  string <span class="apidocSignatureSpan">n_.</span>bufferedCommand
1.  string <span class="apidocSignatureSpan">n_.</span>line
1.  symbol <span class="apidocSignatureSpan">n_.</span>replMode

#### [module n_._events](#apidoc.module.n_._events)
1.  [function <span class="apidocSignatureSpan">n_._events.</span>SIGCONT ()](#apidoc.element.n_._events.SIGCONT)
1.  [function <span class="apidocSignatureSpan">n_._events.</span>SIGINT ()](#apidoc.element.n_._events.SIGINT)
1.  [function <span class="apidocSignatureSpan">n_._events.</span>line (line, cmd)](#apidoc.element.n_._events.line)
1.  object <span class="apidocSignatureSpan">n_._events.</span>close

#### [module n_._events.close](#apidoc.module.n_._events.close)
1.  [function <span class="apidocSignatureSpan">n_._events.close.</span>0 ()](#apidoc.element.n_._events.close.0)
1.  [function <span class="apidocSignatureSpan">n_._events.close.</span>1 ()](#apidoc.element.n_._events.close.1)

#### [module n_.context](#apidoc.module.n_.context)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>clearImmediate (immediate)](#apidoc.element.n_.context.clearImmediate)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>clearInterval (timer)](#apidoc.element.n_.context.clearInterval)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>clearTimeout (timer)](#apidoc.element.n_.context.clearTimeout)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>debugInline (arg)](#apidoc.element.n_.context.debugInline)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>require (path)](#apidoc.element.n_.context.require)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>setImmediate (callback, arg1, arg2, arg3)](#apidoc.element.n_.context.setImmediate)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>setInterval (callback, repeat, arg1, arg2, arg3)](#apidoc.element.n_.context.setInterval)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>setTimeout (callback, after, arg1, arg2, arg3)](#apidoc.element.n_.context.setTimeout)
1.  object <span class="apidocSignatureSpan">n_.context.</span>__coverageCodeDict__
1.  object <span class="apidocSignatureSpan">n_.context.</span>console
1.  object <span class="apidocSignatureSpan">n_.context.</span>global
1.  object <span class="apidocSignatureSpan">n_.context.</span>local
1.  object <span class="apidocSignatureSpan">n_.context.</span>module
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_moduleExports
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_rollup
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_rollup_old
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_serverHttp1
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_serverRepl1
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2_serverReplTcp1

#### [module n_.context.Buffer](#apidoc.module.n_.context.Buffer)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer.Buffer)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>alloc (size, fill, encoding)](#apidoc.element.n_.context.Buffer.alloc)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>allocUnsafe (size)](#apidoc.element.n_.context.Buffer.allocUnsafe)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>allocUnsafeSlow (size)](#apidoc.element.n_.context.Buffer.allocUnsafeSlow)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>byteLength (string, encoding)](#apidoc.element.n_.context.Buffer.byteLength)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>compare (a, b)](#apidoc.element.n_.context.Buffer.compare)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>concat (list, length)](#apidoc.element.n_.context.Buffer.concat)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>from (value, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer.from)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>isBuffer (b)](#apidoc.element.n_.context.Buffer.isBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.</span>isEncoding (encoding)](#apidoc.element.n_.context.Buffer.isEncoding)
1.  number <span class="apidocSignatureSpan">n_.context.Buffer.</span>poolSize

#### [module n_.context.Buffer.prototype](#apidoc.module.n_.context.Buffer.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>asciiSlice ()](#apidoc.element.n_.context.Buffer.prototype.asciiSlice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>asciiWrite ()](#apidoc.element.n_.context.Buffer.prototype.asciiWrite)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>base64Slice ()](#apidoc.element.n_.context.Buffer.prototype.base64Slice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>base64Write ()](#apidoc.element.n_.context.Buffer.prototype.base64Write)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.n_.context.Buffer.prototype.compare)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>copy ()](#apidoc.element.n_.context.Buffer.prototype.copy)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>equals (b)](#apidoc.element.n_.context.Buffer.prototype.equals)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.n_.context.Buffer.prototype.fill)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>hexSlice ()](#apidoc.element.n_.context.Buffer.prototype.hexSlice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>hexWrite ()](#apidoc.element.n_.context.Buffer.prototype.hexWrite)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.includes)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>inspect ()](#apidoc.element.n_.context.Buffer.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>latin1Slice ()](#apidoc.element.n_.context.Buffer.prototype.latin1Slice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>latin1Write ()](#apidoc.element.n_.context.Buffer.prototype.latin1Write)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readDoubleBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readDoubleLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readFloatBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readFloatLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt16BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt16LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt32BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt32LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt8)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readIntBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readIntLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt16BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt16LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt32BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt32LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt8)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUIntBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUIntLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>slice (start, end)](#apidoc.element.n_.context.Buffer.prototype.slice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap16 ()](#apidoc.element.n_.context.Buffer.prototype.swap16)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap32 ()](#apidoc.element.n_.context.Buffer.prototype.swap32)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap64 ()](#apidoc.element.n_.context.Buffer.prototype.swap64)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>toJSON ()](#apidoc.element.n_.context.Buffer.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>toString ()](#apidoc.element.n_.context.Buffer.prototype.toString)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>ucs2Slice ()](#apidoc.element.n_.context.Buffer.prototype.ucs2Slice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>ucs2Write ()](#apidoc.element.n_.context.Buffer.prototype.ucs2Write)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>utf8Slice ()](#apidoc.element.n_.context.Buffer.prototype.utf8Slice)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>utf8Write ()](#apidoc.element.n_.context.Buffer.prototype.utf8Write)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.n_.context.Buffer.prototype.write)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeDoubleBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeDoubleLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeFloatBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeFloatLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt16BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt16LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt32BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt32LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt8)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeIntBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeIntLE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt16BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt16LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt32BE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt32LE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt8)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUIntBE)
1.  [function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUIntLE)

#### [module n_.context.console](#apidoc.module.n_.context.console)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>assert ()](#apidoc.element.n_.context.console.assert)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>dir ()](#apidoc.element.n_.context.console.dir)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>error ()](#apidoc.element.n_.context.console.error)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>info ()](#apidoc.element.n_.context.console.info)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>log ()](#apidoc.element.n_.context.console.log)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>time ()](#apidoc.element.n_.context.console.time)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>timeEnd ()](#apidoc.element.n_.context.console.timeEnd)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>trace ()](#apidoc.element.n_.context.console.trace)
1.  [function <span class="apidocSignatureSpan">n_.context.console.</span>warn ()](#apidoc.element.n_.context.console.warn)

#### [module n_.context.require](#apidoc.module.n_.context.require)
1.  [function <span class="apidocSignatureSpan">n_.context.</span>require (path)](#apidoc.element.n_.context.require.require)
1.  [function <span class="apidocSignatureSpan">n_.context.require.</span>resolve (request)](#apidoc.element.n_.context.require.resolve)
1.  object <span class="apidocSignatureSpan">n_.context.require.</span>cache
1.  object <span class="apidocSignatureSpan">n_.context.require.</span>extensions
1.  object <span class="apidocSignatureSpan">n_.context.require.</span>main

#### [module n_.context.utility2](#apidoc.module.n_.context.utility2)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>Blob (array, options)](#apidoc.element.n_.context.utility2.Blob)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>FormData ()](#apidoc.element.n_.context.utility2.FormData)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>HtmlReport (e)](#apidoc.element.n_.context.utility2.HtmlReport)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>Instrumenter (e)](#apidoc.element.n_.context.utility2.Instrumenter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>JSLINT (t, n)](#apidoc.element.n_.context.utility2.JSLINT)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>MAP (r, i, s)](#apidoc.element.n_.context.utility2.MAP)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>Module (id, parent)](#apidoc.element.n_.context.utility2.Module)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>TextReport (e)](#apidoc.element.n_.context.utility2.TextReport)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_DbTable (options)](#apidoc.element.n_.context.utility2._DbTable)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>__require (path)](#apidoc.element.n_.context.utility2.__require)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_middlewareError (error, request, response)](#apidoc.element.n_.context.utility2._middlewareError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_middlewareJsonpStateInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2._middlewareJsonpStateInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_serverLocalUrlTest ()](#apidoc.element.n_.context.utility2._serverLocalUrlTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_stateInit (options)](#apidoc.element.n_.context.utility2._stateInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>_testRunBefore ()](#apidoc.element.n_.context.utility2._testRunBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ajax (options, onError)](#apidoc.element.n_.context.utility2.ajax)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ajaxProgressUpdate ()](#apidoc.element.n_.context.utility2.ajaxProgressUpdate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>apiAjax (self, options, onError)](#apidoc.element.n_.context.utility2.apiAjax)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>apiDictUpdate (options)](#apidoc.element.n_.context.utility2.apiDictUpdate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>apidocCreate (options)](#apidoc.element.n_.context.utility2.apidocCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>apidocModuleDictAdd (options, moduleDict)](#apidoc.element.n_.context.utility2.apidocModuleDictAdd)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>array_to_hash (e)](#apidoc.element.n_.context.utility2.array_to_hash)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>assert (passed, message)](#apidoc.element.n_.context.utility2.assert)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>assertJsonEqual (aa, bb)](#apidoc.element.n_.context.utility2.assertJsonEqual)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>assertJsonNotEqual (aa, bb)](#apidoc.element.n_.context.utility2.assertJsonNotEqual)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_add_scope (e)](#apidoc.element.n_.context.utility2.ast_add_scope)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_lift_variables (e)](#apidoc.element.n_.context.utility2.ast_lift_variables)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_mangle (e, t)](#apidoc.element.n_.context.utility2.ast_mangle)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_squeeze (e, t)](#apidoc.element.n_.context.utility2.ast_squeeze)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_walker ()](#apidoc.element.n_.context.utility2.ast_walker)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromBuffer (bff)](#apidoc.element.n_.context.utility2.base64FromBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromHex (text)](#apidoc.element.n_.context.utility2.base64FromHex)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromString (text)](#apidoc.element.n_.context.utility2.base64FromString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToBuffer (text)](#apidoc.element.n_.context.utility2.base64ToBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToHex (text)](#apidoc.element.n_.context.utility2.base64ToHex)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToString (text)](#apidoc.element.n_.context.utility2.base64ToString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>blobRead (blob, encoding, onError)](#apidoc.element.n_.context.utility2.blobRead)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>browserTest (options, onError)](#apidoc.element.n_.context.utility2.browserTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferConcat (bufferList)](#apidoc.element.n_.context.utility2.bufferConcat)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferCreate (text)](#apidoc.element.n_.context.utility2.bufferCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferCreateIfNotBuffer (text)](#apidoc.element.n_.context.utility2.bufferCreateIfNotBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferIndexOfSubBuffer (bff, subBff, fromIndex)](#apidoc.element.n_.context.utility2.bufferIndexOfSubBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferRandomBytes (length)](#apidoc.element.n_.context.utility2.bufferRandomBytes)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferToNodeBuffer (bff)](#apidoc.element.n_.context.utility2.bufferToNodeBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferToString (bff)](#apidoc.element.n_.context.utility2.bufferToString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildApidoc (options, onError)](#apidoc.element.n_.context.utility2.buildApidoc)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildApp (options, onError)](#apidoc.element.n_.context.utility2.buildApp)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildLib (options, onError)](#apidoc.element.n_.context.utility2.buildLib)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildNpmdoc (options, onError)](#apidoc.element.n_.context.utility2.buildNpmdoc)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildReadme (options, onError)](#apidoc.element.n_.context.utility2.buildReadme)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildTest (options, onError)](#apidoc.element.n_.context.utility2.buildTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>cliRunIstanbul (options)](#apidoc.element.n_.context.utility2.cliRunIstanbul)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentDelete (options, onError)](#apidoc.element.n_.context.utility2.contentDelete)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentGet (options, onError)](#apidoc.element.n_.context.utility2.contentGet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentPut (options, onError)](#apidoc.element.n_.context.utility2.contentPut)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentPutFile (options, onError)](#apidoc.element.n_.context.utility2.contentPutFile)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentRequest (options, onError)](#apidoc.element.n_.context.utility2.contentRequest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentTouch (options, onError)](#apidoc.element.n_.context.utility2.contentTouch)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentTouchList (options, onError)](#apidoc.element.n_.context.utility2.contentTouchList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieDict ()](#apidoc.element.n_.context.utility2.cookieDict)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieRemove (name)](#apidoc.element.n_.context.utility2.cookieRemove)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieRemoveAll ()](#apidoc.element.n_.context.utility2.cookieRemoveAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieSet (name, value, expiresOffset)](#apidoc.element.n_.context.utility2.cookieSet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>coverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2.coverageMerge)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>coverageReportCreate ()](#apidoc.element.n_.context.utility2.coverageReportCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>curry (e)](#apidoc.element.n_.context.utility2.curry)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbCrudRemoveAll (onError)](#apidoc.element.n_.context.utility2.dbCrudRemoveAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbDrop (onError)](#apidoc.element.n_.context.utility2.dbDrop)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbExport (onError)](#apidoc.element.n_.context.utility2.dbExport)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbFieldRandomCreate (options)](#apidoc.element.n_.context.utility2.dbFieldRandomCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbImport (text, onError)](#apidoc.element.n_.context.utility2.dbImport)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbLoad (onError)](#apidoc.element.n_.context.utility2.dbLoad)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowGetItem (dbRow, key)](#apidoc.element.n_.context.utility2.dbRowGetItem)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListGetManyByOperator (dbRowList, fieldName, operator, bb)](#apidoc.element.n_.context.utility2.dbRowListGetManyByOperator)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListGetManyByQuery (dbRowList, query, fieldName)](#apidoc.element.n_.context.utility2.dbRowListGetManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListRandomCreate (options)](#apidoc.element.n_.context.utility2.dbRowListRandomCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowProject (dbRow, fieldList)](#apidoc.element.n_.context.utility2.dbRowProject)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowRandomCreate (options)](#apidoc.element.n_.context.utility2.dbRowRandomCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowSetId (dbRow, idIndex)](#apidoc.element.n_.context.utility2.dbRowSetId)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbSave (onError)](#apidoc.element.n_.context.utility2.dbSave)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableCreateMany (optionsList, onError)](#apidoc.element.n_.context.utility2.dbTableCreateMany)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableCreateOne (options, onError)](#apidoc.element.n_.context.utility2.dbTableCreateOne)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoCreate (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoCrudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoCrudGetManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoUpdate (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoUpdate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>domFragmentRender (template, dict)](#apidoc.element.n_.context.utility2.domFragmentRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>echo (arg)](#apidoc.element.n_.context.utility2.echo)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>envKeyIsSensitive (key)](#apidoc.element.n_.context.utility2.envKeyIsSensitive)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>envSanitize (env)](#apidoc.element.n_.context.utility2.envSanitize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>errorMessagePrepend (error, message)](#apidoc.element.n_.context.utility2.errorMessagePrepend)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>exit (exitCode)](#apidoc.element.n_.context.utility2.exit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsRmrSync (dir)](#apidoc.element.n_.context.utility2.fsRmrSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsWriteFileWithMkdirpSync (file, data)](#apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsWriteFileWithMkdirpSync2 (file, data)](#apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync2)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>gen_code (e, t)](#apidoc.element.n_.context.utility2.gen_code)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>httpRequest (options, onError)](#apidoc.element.n_.context.utility2.httpRequest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>idDomElementCreate (seed)](#apidoc.element.n_.context.utility2.idDomElementCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>idFieldInit (options)](#apidoc.element.n_.context.utility2.idFieldInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>instrumentInPackage (code, file)](#apidoc.element.n_.context.utility2.instrumentInPackage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>instrumentSync (code, file)](#apidoc.element.n_.context.utility2.instrumentSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>isNullOrUndefined (arg)](#apidoc.element.n_.context.utility2.isNullOrUndefined)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_alphanumeric_char (e)](#apidoc.element.n_.context.utility2.is_alphanumeric_char)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_identifier_char (e)](#apidoc.element.n_.context.utility2.is_identifier_char)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_identifier_start (e)](#apidoc.element.n_.context.utility2.is_identifier_start)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulCoverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2.istanbulCoverageMerge)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulCoverageReportCreate ()](#apidoc.element.n_.context.utility2.istanbulCoverageReportCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulInstrumentInPackage (code, file)](#apidoc.element.n_.context.utility2.istanbulInstrumentInPackage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulInstrumentSync (code, file)](#apidoc.element.n_.context.utility2.istanbulInstrumentSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintAndPrint (script, file)](#apidoc.element.n_.context.utility2.jslintAndPrint)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintAndPrintConditional (script, file, mode)](#apidoc.element.n_.context.utility2.jslintAndPrintConditional)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintEs6 (e, i, s)](#apidoc.element.n_.context.utility2.jslintEs6)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jsonCopy (arg)](#apidoc.element.n_.context.utility2.jsonCopy)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jsonStringifyOrdered (element, replacer, space)](#apidoc.element.n_.context.utility2.jsonStringifyOrdered)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtA256GcmDecrypt (token, key)](#apidoc.element.n_.context.utility2.jwtA256GcmDecrypt)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtA256GcmEncrypt (data, key)](#apidoc.element.n_.context.utility2.jwtA256GcmEncrypt)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtAes256KeyCreate ()](#apidoc.element.n_.context.utility2.jwtAes256KeyCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtAes256KeyInit (key)](#apidoc.element.n_.context.utility2.jwtAes256KeyInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtBase64UrlNormalize (text)](#apidoc.element.n_.context.utility2.jwtBase64UrlNormalize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtHs256Decode (token, key)](#apidoc.element.n_.context.utility2.jwtHs256Decode)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtHs256Encode (data, key)](#apidoc.element.n_.context.utility2.jwtHs256Encode)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtNormalize (data)](#apidoc.element.n_.context.utility2.jwtNormalize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>listGetElementRandom (list)](#apidoc.element.n_.context.utility2.listGetElementRandom)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>listShuffle (list)](#apidoc.element.n_.context.utility2.listShuffle)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>make_string (e, t)](#apidoc.element.n_.context.utility2.make_string)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>member (e, t)](#apidoc.element.n_.context.utility2.member)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareAssetsCached (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareAssetsCached)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareBodyParse (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareBodyParse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareBodyRead (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareBodyRead)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCacheControlLastModified ( request, response, nextMiddleware )](#apidoc.element.n_.context.utility2.middlewareCacheControlLastModified)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCrudBuiltin (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareCrudBuiltin)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCrudEnd (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareCrudEnd)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareFileServer (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareFileServer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareForwardProxy (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareForwardProxy)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareGroupCreate (middlewareList)](#apidoc.element.n_.context.utility2.middlewareGroupCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareRouter (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareRouter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareUserLogin (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareUserLogin)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareValidate (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareValidate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>moduleDirname (module, modulePathList)](#apidoc.element.n_.context.utility2.moduleDirname)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>nop ()](#apidoc.element.n_.context.utility2.nop)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeDict (dict)](#apidoc.element.n_.context.utility2.normalizeDict)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeList (list)](#apidoc.element.n_.context.utility2.normalizeList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeParamDictSwagger (data, pathObject)](#apidoc.element.n_.context.utility2.normalizeParamDictSwagger)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeText (text)](#apidoc.element.n_.context.utility2.normalizeText)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectGetElementFirst (arg)](#apidoc.element.n_.context.utility2.objectGetElementFirst)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectKeysTypeof (arg)](#apidoc.element.n_.context.utility2.objectKeysTypeof)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectLiteralize (arg)](#apidoc.element.n_.context.utility2.objectLiteralize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectSetDefault (arg, defaults, depth)](#apidoc.element.n_.context.utility2.objectSetDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectSetOverride (arg, overrides, depth, env)](#apidoc.element.n_.context.utility2.objectSetOverride)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectTraverse (arg, onSelf, circularList)](#apidoc.element.n_.context.utility2.objectTraverse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorDefault (error)](#apidoc.element.n_.context.utility2.onErrorDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorJsonapi (onError)](#apidoc.element.n_.context.utility2.onErrorJsonapi)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorThrow (error)](#apidoc.element.n_.context.utility2.onErrorThrow)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorWithStack (onError)](#apidoc.element.n_.context.utility2.onErrorWithStack)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onFileModifiedRestart (file)](#apidoc.element.n_.context.utility2.onFileModifiedRestart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onNext (options, onError)](#apidoc.element.n_.context.utility2.onNext)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onParallel (onError, onEach, onRetry)](#apidoc.element.n_.context.utility2.onParallel)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onParallelList (options, onEach, onError)](#apidoc.element.n_.context.utility2.onParallelList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onReadyAfter (onError)](#apidoc.element.n_.context.utility2.onReadyAfter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onReadyBefore (error, data)](#apidoc.element.n_.context.utility2.onReadyBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onResetAfter (onError)](#apidoc.element.n_.context.utility2.onResetAfter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onResetBefore (error, data)](#apidoc.element.n_.context.utility2.onResetBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>onTimeout (onError, timeout, message)](#apidoc.element.n_.context.utility2.onTimeout)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>parse (e, t, n)](#apidoc.element.n_.context.utility2.parse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>processSpawnWithTimeout ()](#apidoc.element.n_.context.utility2.processSpawnWithTimeout)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>profile (fnc, onError)](#apidoc.element.n_.context.utility2.profile)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>profileSync (fnc)](#apidoc.element.n_.context.utility2.profileSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>replStart ()](#apidoc.element.n_.context.utility2.replStart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>require (path)](#apidoc.element.n_.context.utility2.require)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>requireExampleJsFromReadme ()](#apidoc.element.n_.context.utility2.requireExampleJsFromReadme)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>schemaNormalizeAndCopy (schema)](#apidoc.element.n_.context.utility2.schemaNormalizeAndCopy)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondDefault (request, response, statusCode, error)](#apidoc.element.n_.context.utility2.serverRespondDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondEcho (request, response)](#apidoc.element.n_.context.utility2.serverRespondEcho)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondHeadSet (request, response, statusCode, headers)](#apidoc.element.n_.context.utility2.serverRespondHeadSet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondJsonapi (request, response, error, data, meta)](#apidoc.element.n_.context.utility2.serverRespondJsonapi)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondTimeoutDefault (request, response, timeout)](#apidoc.element.n_.context.utility2.serverRespondTimeoutDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>setTimeoutOnError (onError, error, data)](#apidoc.element.n_.context.utility2.setTimeoutOnError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>set_logger (e)](#apidoc.element.n_.context.utility2.set_logger)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashScryptCreate (password, options)](#apidoc.element.n_.context.utility2.sjclHashScryptCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashScryptValidate (password, hash)](#apidoc.element.n_.context.utility2.sjclHashScryptValidate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashSha256Create (data)](#apidoc.element.n_.context.utility2.sjclHashSha256Create)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHmacSha256Create (key, data)](#apidoc.element.n_.context.utility2.sjclHmacSha256Create)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>slice (e, t)](#apidoc.element.n_.context.utility2.slice)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>sortCompare (aa, bb)](#apidoc.element.n_.context.utility2.sortCompare)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>split_lines (e, t)](#apidoc.element.n_.context.utility2.split_lines)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageClear (onError)](#apidoc.element.n_.context.utility2.storageClear)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageDefer (options, onError)](#apidoc.element.n_.context.utility2.storageDefer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageGetItem (key, onError)](#apidoc.element.n_.context.utility2.storageGetItem)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageInit ()](#apidoc.element.n_.context.utility2.storageInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageKeys (onError)](#apidoc.element.n_.context.utility2.storageKeys)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageLength (onError)](#apidoc.element.n_.context.utility2.storageLength)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageRemoveItem (key, onError)](#apidoc.element.n_.context.utility2.storageRemoveItem)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageSetItem (key, value, onError)](#apidoc.element.n_.context.utility2.storageSetItem)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>streamListCleanup (streamList)](#apidoc.element.n_.context.utility2.streamListCleanup)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>streamReadAll (stream, onError)](#apidoc.element.n_.context.utility2.streamReadAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>stringHtmlSafe (text)](#apidoc.element.n_.context.utility2.stringHtmlSafe)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>taskCreate (options, onTask, onError)](#apidoc.element.n_.context.utility2.taskCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>taskCreateCached (options, onTask, onError)](#apidoc.element.n_.context.utility2.taskCreateCached)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>templateRender (template, dict)](#apidoc.element.n_.context.utility2.templateRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>templateRenderJslintLite (template, options)](#apidoc.element.n_.context.utility2.templateRenderJslintLite)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>testMock (mockList, onTestCase, onError)](#apidoc.element.n_.context.utility2.testMock)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>testReportCreate (testReport)](#apidoc.element.n_.context.utility2.testReportCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>testReportMerge (testReport1, testReport2)](#apidoc.element.n_.context.utility2.testReportMerge)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>testRunDefault (options)](#apidoc.element.n_.context.utility2.testRunDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>testRunServer (options)](#apidoc.element.n_.context.utility2.testRunServer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>timeElapsedPoll (options)](#apidoc.element.n_.context.utility2.timeElapsedPoll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>timeElapsedStart (options, timeStart)](#apidoc.element.n_.context.utility2.timeElapsedStart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>tokenizer (e)](#apidoc.element.n_.context.utility2.tokenizer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>tryCatchOnError (fnc, onError)](#apidoc.element.n_.context.utility2.tryCatchOnError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>tryCatchReadFile (file, options)](#apidoc.element.n_.context.utility2.tryCatchReadFile)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uglify (code, file)](#apidoc.element.n_.context.utility2.uglify)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateFadeIn (element)](#apidoc.element.n_.context.utility2.uiAnimateFadeIn)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateFadeOut (element)](#apidoc.element.n_.context.utility2.uiAnimateFadeOut)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateScrollTo (element)](#apidoc.element.n_.context.utility2.uiAnimateScrollTo)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateShake (element)](#apidoc.element.n_.context.utility2.uiAnimateShake)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideAccordian (element, elementList)](#apidoc.element.n_.context.utility2.uiAnimateSlideAccordian)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideDown (element)](#apidoc.element.n_.context.utility2.uiAnimateSlideDown)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideUp (element)](#apidoc.element.n_.context.utility2.uiAnimateSlideUp)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiDatatableRender (options)](#apidoc.element.n_.context.utility2.uiDatatableRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiEventDelegate (event)](#apidoc.element.n_.context.utility2.uiEventDelegate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiEventInit (element)](#apidoc.element.n_.context.utility2.uiEventInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiParamRender (paramDef)](#apidoc.element.n_.context.utility2.uiParamRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiRender ()](#apidoc.element.n_.context.utility2.uiRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiScrollTo (locationHash)](#apidoc.element.n_.context.utility2.uiScrollTo)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>urlBaseGet ()](#apidoc.element.n_.context.utility2.urlBaseGet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>urlParse (url)](#apidoc.element.n_.context.utility2.urlParse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>userLoginByPassword (options, onError)](#apidoc.element.n_.context.utility2.userLoginByPassword)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>userLogout (options, onError)](#apidoc.element.n_.context.utility2.userLogout)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>uuid4Create ()](#apidoc.element.n_.context.utility2.uuid4Create)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateByParamDefList (options)](#apidoc.element.n_.context.utility2.validateByParamDefList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateByPropDef (options)](#apidoc.element.n_.context.utility2.validateByPropDef)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateBySchema (options)](#apidoc.element.n_.context.utility2.validateBySchema)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateBySwagger (options)](#apidoc.element.n_.context.utility2.validateBySwagger)
1.  number <span class="apidocSignatureSpan">n_.context.utility2.</span>ajaxProgressCounter
1.  number <span class="apidocSignatureSpan">n_.context.utility2.</span>ajaxProgressState
1.  number <span class="apidocSignatureSpan">n_.context.utility2.</span>timeExit
1.  number <span class="apidocSignatureSpan">n_.context.utility2.</span>timeoutDefault
1.  object <span class="apidocSignatureSpan">n_.context.</span>utility2
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>ATOMIC_START_TOKEN
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>CSSLint
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>KEYWORDS
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>KEYWORDS_ATOM
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>OPERATORS
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>PRECEDENCE
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>RESERVED_WORDS
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>_debugTryCatchErrorCaught
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>_fs
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>_http
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>apiDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>apidoc
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>assetsDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>cacheDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>collector
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>contentTypeDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>coverageUtils
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>db
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>env
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>errorDefault
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>escodegen
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>esprima
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>estraverse
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>esutils
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>github_crud
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>handlebars
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbul
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>jslint
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>local
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>module
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>packageJsonNpmdocDefault
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>regexpEmailValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>regexpPhoneValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>regexpUriComponentCharset
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>regexpUuidValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>sjcl
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>storageDeferList
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>swaggerJson
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>swaggerSchemaJson
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>swgg
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>taskOnTaskDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>templateApiDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>testReport
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>uglifyjs
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>uiEventListenerDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>util
1.  object <span class="apidocSignatureSpan">n_.context.utility2.</span>writer
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>__dirname
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>foot.txt
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>head.txt
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>modeJs
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>serverLocalHost
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>storageDir
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>stringAsciiCharset
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>stringUriComponentCharset
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateApidocHtml
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateApidocMd
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateCoverageBadgeSvg
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateSwaggerUiLogoSmallBase64
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiDatatable
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiMain
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiOperation
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiParam
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiResource
1.  string <span class="apidocSignatureSpan">n_.context.utility2.</span>templateUiResponseAjax

#### [module n_.context.utility2.FormData.prototype](#apidoc.module.n_.context.utility2.FormData.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.FormData.prototype.</span>append (name, value, filename)](#apidoc.element.n_.context.utility2.FormData.prototype.append)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.FormData.prototype.</span>read (onError)](#apidoc.element.n_.context.utility2.FormData.prototype.read)

#### [module n_.context.utility2.HtmlReport.prototype](#apidoc.module.n_.context.utility2.HtmlReport.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>fillTemplate (e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.fillTemplate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>getPathHtml (e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.getPathHtml)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>standardLinkMapper ()](#apidoc.element.n_.context.utility2.HtmlReport.prototype.standardLinkMapper)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeDetailPage (e, t, n)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeDetailPage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeFiles ( e, t, n, r)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeFiles)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeIndexPage ( e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeIndexPage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeReport ( e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeReport)

#### [module n_.context.utility2.Instrumenter.prototype](#apidoc.module.n_.context.utility2.Instrumenter.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>arrowBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.arrowBlockConverter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchIncrementExprAst (e, t , n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchIncrementExprAst)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchLocationFor (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchLocationFor)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchName (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchName)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>conditionalBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.conditionalBranchInjector)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>convertToBlock (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.convertToBlock)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>coverFunction (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.coverFunction)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>coverStatement (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.coverStatement)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>endIgnore ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.endIgnore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>extractCurrentHint (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.extractCurrentHint)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>filterHints (e )](#apidoc.element.n_.context.utility2.Instrumenter.prototype.filterHints)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>findLeaves ( e, n, r, i)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.findLeaves)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>fixColumnPositions (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.fixColumnPositions)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>functionName (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.functionName)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>getPreamble (e, t )](#apidoc.element.n_.context.utility2.Instrumenter.prototype.getPreamble)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>ifBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBlockConverter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>ifBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBranchInjector)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrument (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrument)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrumentASTSync (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentASTSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrumentSync (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>isUseStrictExpression (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.isUseStrictExpression)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>lastFileCoverage ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.lastFileCoverage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>lastSourceMap ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.lastSourceMap)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>locationsForNodes (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.locationsForNodes)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>logicalExpressionBranchInjector (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.logicalExpressionBranchInjector)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>loopBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.loopBlockConverter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeAddSkip (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddSkip)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeAddType (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddType)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeSkipNode (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeSkipNode)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>paranoidHandlerCheck (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.paranoidHandlerCheck)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>skipInit (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.skipInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>skipLeft (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.skipLeft)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>splice (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.splice)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>startIgnore ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.startIgnore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>statementName (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.statementName)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>switchBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.switchBranchInjector)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>switchCaseInjector (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.switchCaseInjector)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>withBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.withBlockConverter)

#### [module n_.context.utility2.TextReport.prototype](#apidoc.module.n_.context.utility2.TextReport.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2.TextReport.prototype.</span>writeReport (e)](#apidoc.element.n_.context.utility2.TextReport.prototype.writeReport)

#### [module n_.context.utility2._DbTable.prototype](#apidoc.module.n_.context.utility2._DbTable.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_cleanup ()](#apidoc.element.n_.context.utility2._DbTable.prototype._cleanup)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudGetManyByQuery (query)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudGetManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudGetOneById (idDict)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudGetOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudRemoveOneById (idDict, circularList)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudRemoveOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudSetOneById (dbRow)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudSetOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudUpdateOneById (dbRow)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudUpdateOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudCountAll (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudCountAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudCountManyByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudCountManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetManyById (idDictList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneById (idDict, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneByRandom (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByRandom)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveAll (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveManyById (idDictList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveManyByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveOneById (idDict, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudSetManyById (dbRowList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudSetManyById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudSetOneById (dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudSetOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateManyById (dbRowList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateManyByQuery (query, dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateOneById (dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateOneById)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>drop (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.drop)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>export (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.export)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>idIndexCreate (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.idIndexCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>idIndexRemove (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.idIndexRemove)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>save (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.save)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>ttlSet (ttl, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.ttlSet)

#### [module n_.context.utility2_moduleExports](#apidoc.module.n_.context.utility2_moduleExports)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>Blob (array, options)](#apidoc.element.n_.context.utility2_moduleExports.Blob)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>FormData ()](#apidoc.element.n_.context.utility2_moduleExports.FormData)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>Module (id, parent)](#apidoc.element.n_.context.utility2_moduleExports.Module)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>__require (path)](#apidoc.element.n_.context.utility2_moduleExports.__require)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_middlewareError (error, request, response)](#apidoc.element.n_.context.utility2_moduleExports._middlewareError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_middlewareJsonpStateInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports._middlewareJsonpStateInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_serverLocalUrlTest ()](#apidoc.element.n_.context.utility2_moduleExports._serverLocalUrlTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_stateInit (options)](#apidoc.element.n_.context.utility2_moduleExports._stateInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_testRunBefore ()](#apidoc.element.n_.context.utility2_moduleExports._testRunBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajax (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.ajax)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajaxProgressUpdate ()](#apidoc.element.n_.context.utility2_moduleExports.ajaxProgressUpdate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>apidocCreate (options)](#apidoc.element.n_.context.utility2_moduleExports.apidocCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assert (passed, message)](#apidoc.element.n_.context.utility2_moduleExports.assert)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assertJsonEqual (aa, bb)](#apidoc.element.n_.context.utility2_moduleExports.assertJsonEqual)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assertJsonNotEqual (aa, bb)](#apidoc.element.n_.context.utility2_moduleExports.assertJsonNotEqual)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromBuffer (bff)](#apidoc.element.n_.context.utility2_moduleExports.base64FromBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromHex (text)](#apidoc.element.n_.context.utility2_moduleExports.base64FromHex)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromString (text)](#apidoc.element.n_.context.utility2_moduleExports.base64FromString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToBuffer (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToHex (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToHex)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToString (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>blobRead (blob, encoding, onError)](#apidoc.element.n_.context.utility2_moduleExports.blobRead)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>browserTest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.browserTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferConcat (bufferList)](#apidoc.element.n_.context.utility2_moduleExports.bufferConcat)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferCreate (text)](#apidoc.element.n_.context.utility2_moduleExports.bufferCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferCreateIfNotBuffer (text)](#apidoc.element.n_.context.utility2_moduleExports.bufferCreateIfNotBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferIndexOfSubBuffer (bff, subBff, fromIndex)](#apidoc.element.n_.context.utility2_moduleExports.bufferIndexOfSubBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferRandomBytes (length)](#apidoc.element.n_.context.utility2_moduleExports.bufferRandomBytes)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferToNodeBuffer (bff)](#apidoc.element.n_.context.utility2_moduleExports.bufferToNodeBuffer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferToString (bff)](#apidoc.element.n_.context.utility2_moduleExports.bufferToString)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildApidoc (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildApidoc)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildApp (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildApp)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildLib (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildLib)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildNpmdoc (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildNpmdoc)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildReadme (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildReadme)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildTest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildTest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieDict ()](#apidoc.element.n_.context.utility2_moduleExports.cookieDict)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieRemove (name)](#apidoc.element.n_.context.utility2_moduleExports.cookieRemove)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieRemoveAll ()](#apidoc.element.n_.context.utility2_moduleExports.cookieRemoveAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieSet (name, value, expiresOffset)](#apidoc.element.n_.context.utility2_moduleExports.cookieSet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoCreate (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoCrudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCrudGetManyByQuery)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoUpdate (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoUpdate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>domFragmentRender (template, dict)](#apidoc.element.n_.context.utility2_moduleExports.domFragmentRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>echo (arg)](#apidoc.element.n_.context.utility2_moduleExports.echo)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>envKeyIsSensitive (key)](#apidoc.element.n_.context.utility2_moduleExports.envKeyIsSensitive)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>envSanitize (env)](#apidoc.element.n_.context.utility2_moduleExports.envSanitize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>errorMessagePrepend (error, message)](#apidoc.element.n_.context.utility2_moduleExports.errorMessagePrepend)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>exit (exitCode)](#apidoc.element.n_.context.utility2_moduleExports.exit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>fsRmrSync (dir)](#apidoc.element.n_.context.utility2_moduleExports.fsRmrSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>fsWriteFileWithMkdirpSync (file, data)](#apidoc.element.n_.context.utility2_moduleExports.fsWriteFileWithMkdirpSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>httpRequest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.httpRequest)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>isNullOrUndefined (arg)](#apidoc.element.n_.context.utility2_moduleExports.isNullOrUndefined)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulCoverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageMerge)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulCoverageReportCreate ()](#apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageReportCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulInstrumentInPackage (code, file)](#apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentInPackage)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulInstrumentSync (code, file)](#apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jslintAndPrint (script, file)](#apidoc.element.n_.context.utility2_moduleExports.jslintAndPrint)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jslintAndPrintConditional (script, file, mode)](#apidoc.element.n_.context.utility2_moduleExports.jslintAndPrintConditional)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jsonCopy (arg)](#apidoc.element.n_.context.utility2_moduleExports.jsonCopy)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jsonStringifyOrdered (element, replacer, space)](#apidoc.element.n_.context.utility2_moduleExports.jsonStringifyOrdered)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtA256GcmDecrypt (token, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmDecrypt)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtA256GcmEncrypt (data, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmEncrypt)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtAes256KeyCreate ()](#apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtAes256KeyInit (key)](#apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtBase64UrlNormalize (text)](#apidoc.element.n_.context.utility2_moduleExports.jwtBase64UrlNormalize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtHs256Decode (token, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtHs256Decode)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtHs256Encode (data, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtHs256Encode)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtNormalize (data)](#apidoc.element.n_.context.utility2_moduleExports.jwtNormalize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>listGetElementRandom (list)](#apidoc.element.n_.context.utility2_moduleExports.listGetElementRandom)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>listShuffle (list)](#apidoc.element.n_.context.utility2_moduleExports.listShuffle)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareAssetsCached (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareAssetsCached)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareBodyRead (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareBodyRead)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareCacheControlLastModified ( request, response, nextMiddleware )](#apidoc.element.n_.context.utility2_moduleExports.middlewareCacheControlLastModified)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareFileServer (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareFileServer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareForwardProxy (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareForwardProxy)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareGroupCreate (middlewareList)](#apidoc.element.n_.context.utility2_moduleExports.middlewareGroupCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareInit)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>moduleDirname (module, modulePathList)](#apidoc.element.n_.context.utility2_moduleExports.moduleDirname)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>nop ()](#apidoc.element.n_.context.utility2_moduleExports.nop)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeDict (dict)](#apidoc.element.n_.context.utility2_moduleExports.normalizeDict)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeList (list)](#apidoc.element.n_.context.utility2_moduleExports.normalizeList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeText (text)](#apidoc.element.n_.context.utility2_moduleExports.normalizeText)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectGetElementFirst (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectGetElementFirst)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectKeysTypeof (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectKeysTypeof)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectLiteralize (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectLiteralize)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectSetDefault (arg, defaults, depth)](#apidoc.element.n_.context.utility2_moduleExports.objectSetDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectSetOverride (arg, overrides, depth, env)](#apidoc.element.n_.context.utility2_moduleExports.objectSetOverride)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectTraverse (arg, onSelf, circularList)](#apidoc.element.n_.context.utility2_moduleExports.objectTraverse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorDefault (error)](#apidoc.element.n_.context.utility2_moduleExports.onErrorDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorThrow (error)](#apidoc.element.n_.context.utility2_moduleExports.onErrorThrow)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorWithStack (onError)](#apidoc.element.n_.context.utility2_moduleExports.onErrorWithStack)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onFileModifiedRestart (file)](#apidoc.element.n_.context.utility2_moduleExports.onFileModifiedRestart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onNext (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.onNext)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onParallel (onError, onEach, onRetry)](#apidoc.element.n_.context.utility2_moduleExports.onParallel)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onParallelList (options, onEach, onError)](#apidoc.element.n_.context.utility2_moduleExports.onParallelList)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onReadyAfter (onError)](#apidoc.element.n_.context.utility2_moduleExports.onReadyAfter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onReadyBefore (error, data)](#apidoc.element.n_.context.utility2_moduleExports.onReadyBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onResetAfter (onError)](#apidoc.element.n_.context.utility2_moduleExports.onResetAfter)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onResetBefore (error, data)](#apidoc.element.n_.context.utility2_moduleExports.onResetBefore)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onTimeout (onError, timeout, message)](#apidoc.element.n_.context.utility2_moduleExports.onTimeout)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>processSpawnWithTimeout ()](#apidoc.element.n_.context.utility2_moduleExports.processSpawnWithTimeout)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>profile (fnc, onError)](#apidoc.element.n_.context.utility2_moduleExports.profile)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>profileSync (fnc)](#apidoc.element.n_.context.utility2_moduleExports.profileSync)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>replStart ()](#apidoc.element.n_.context.utility2_moduleExports.replStart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>requireExampleJsFromReadme ()](#apidoc.element.n_.context.utility2_moduleExports.requireExampleJsFromReadme)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondDefault (request, response, statusCode, error)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondEcho (request, response)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondEcho)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondHeadSet (request, response, statusCode, headers)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondHeadSet)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondTimeoutDefault (request, response, timeout)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondTimeoutDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>setTimeoutOnError (onError, error, data)](#apidoc.element.n_.context.utility2_moduleExports.setTimeoutOnError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashScryptCreate (password, options)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashScryptValidate (password, hash)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptValidate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashSha256Create (data)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashSha256Create)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHmacSha256Create (key, data)](#apidoc.element.n_.context.utility2_moduleExports.sjclHmacSha256Create)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>streamListCleanup (streamList)](#apidoc.element.n_.context.utility2_moduleExports.streamListCleanup)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>streamReadAll (stream, onError)](#apidoc.element.n_.context.utility2_moduleExports.streamReadAll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>stringHtmlSafe (text)](#apidoc.element.n_.context.utility2_moduleExports.stringHtmlSafe)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>taskCreate (options, onTask, onError)](#apidoc.element.n_.context.utility2_moduleExports.taskCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>taskCreateCached (options, onTask, onError)](#apidoc.element.n_.context.utility2_moduleExports.taskCreateCached)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>templateRender (template, dict)](#apidoc.element.n_.context.utility2_moduleExports.templateRender)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>templateRenderJslintLite (template, options)](#apidoc.element.n_.context.utility2_moduleExports.templateRenderJslintLite)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testMock (mockList, onTestCase, onError)](#apidoc.element.n_.context.utility2_moduleExports.testMock)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testReportCreate (testReport)](#apidoc.element.n_.context.utility2_moduleExports.testReportCreate)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testReportMerge (testReport1, testReport2)](#apidoc.element.n_.context.utility2_moduleExports.testReportMerge)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunDefault (options)](#apidoc.element.n_.context.utility2_moduleExports.testRunDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunServer (options)](#apidoc.element.n_.context.utility2_moduleExports.testRunServer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeElapsedPoll (options)](#apidoc.element.n_.context.utility2_moduleExports.timeElapsedPoll)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeElapsedStart (options, timeStart)](#apidoc.element.n_.context.utility2_moduleExports.timeElapsedStart)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>tryCatchOnError (fnc, onError)](#apidoc.element.n_.context.utility2_moduleExports.tryCatchOnError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>tryCatchReadFile (file, options)](#apidoc.element.n_.context.utility2_moduleExports.tryCatchReadFile)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>uglify (code, file)](#apidoc.element.n_.context.utility2_moduleExports.uglify)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>urlParse (url)](#apidoc.element.n_.context.utility2_moduleExports.urlParse)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>uuid4Create ()](#apidoc.element.n_.context.utility2_moduleExports.uuid4Create)
1.  number <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajaxProgressCounter
1.  number <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajaxProgressState
1.  number <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeExit
1.  number <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeoutDefault
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_debugTryCatchErrorCaught
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_http
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>apidoc
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assetsDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cacheDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>contentTypeDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>db
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>env
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>errorDefault
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>github_crud
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbul
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jslint
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>local
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>module
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>npmdoc_n_
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>packageJsonNpmdocDefault
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>regexpEmailValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>regexpPhoneValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>regexpUriComponentCharset
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>regexpUuidValidate
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjcl
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>taskOnTaskDict
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testReport
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunBeforeDone
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunBeforeTimer
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>uglifyjs
1.  object <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>utility2
1.  string <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>__dirname
1.  string <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>modeJs
1.  string <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverLocalHost
1.  string <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>stringAsciiCharset
1.  string <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>stringUriComponentCharset

#### [module n_.context.utility2_moduleExports.FormData.prototype](#apidoc.module.n_.context.utility2_moduleExports.FormData.prototype)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.FormData.prototype.</span>append (name, value, filename)](#apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.append)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.FormData.prototype.</span>read (onError)](#apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.read)

#### [module n_.context.utility2_serverRepl1](#apidoc.module.n_.context.utility2_serverRepl1)
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_inTemplateLiteral
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_sawKeyPress
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>breakEvalOnSigint
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>editorMode
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>ignoreUndefined
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>isCompletionEnabled
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>terminal
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>underscoreAssigned
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>useColors
1.  boolean <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>useGlobal
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_ttyWrite (d, key)](#apidoc.element.n_.context.utility2_serverRepl1._ttyWrite)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>completer (text, cb)](#apidoc.element.n_.context.utility2_serverRepl1.completer)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>eval (script, context, file, onError)](#apidoc.element.n_.context.utility2_serverRepl1.eval)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>evalDefault ()](#apidoc.element.n_.context.utility2_serverRepl1.evalDefault)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>nop ()](#apidoc.element.n_.context.utility2_serverRepl1.nop)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>onError (error)](#apidoc.element.n_.context.utility2_serverRepl1.onError)
1.  [function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>writer (obj, showHidden, depth)](#apidoc.element.n_.context.utility2_serverRepl1.writer)
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_sawReturnAt
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>crlfDelay
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>cursor
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>historyIndex
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>historySize
1.  number <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>prevRows
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_domain
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_events
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>commands
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>context
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>domain
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>history
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>input
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>inputStream
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>lineParser
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>lines
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>output
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>outputStream
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>rli
1.  object <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>socket
1.  string <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_initialPrompt
1.  string <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_prompt
1.  string <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>bufferedCommand
1.  string <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>line
1.  symbol <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>replMode

#### [module n_.inputStream](#apidoc.module.n_.inputStream)
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>_consuming
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>_hadError
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>allowHalfOpen
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>connecting
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>destroyed
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>isRaw
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>isTTY
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>readable
1.  boolean <span class="apidocSignatureSpan">n_.inputStream.</span>writable
1.  [function <span class="apidocSignatureSpan">n_.inputStream.</span>read (n)](#apidoc.element.n_.inputStream.read)
1.  number <span class="apidocSignatureSpan">n_.inputStream.</span>_bytesDispatched
1.  number <span class="apidocSignatureSpan">n_.inputStream.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">n_.inputStream.</span>fd
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_events
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_handle
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_host
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_parent
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_pendingData
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_readableState
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_server
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_sockname
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_writableState
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>_writev
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>domain
1.  object <span class="apidocSignatureSpan">n_.inputStream.</span>server
1.  string <span class="apidocSignatureSpan">n_.inputStream.</span>_pendingEncoding

#### [module n_.inputStream._events](#apidoc.module.n_.inputStream._events)
1.  [function <span class="apidocSignatureSpan">n_.inputStream._events.</span>_socketEnd ()](#apidoc.element.n_.inputStream._events._socketEnd)
1.  [function <span class="apidocSignatureSpan">n_.inputStream._events.</span>data (b)](#apidoc.element.n_.inputStream._events.data)
1.  [function <span class="apidocSignatureSpan">n_.inputStream._events.</span>finish ()](#apidoc.element.n_.inputStream._events.finish)
1.  [function <span class="apidocSignatureSpan">n_.inputStream._events.</span>pause ()](#apidoc.element.n_.inputStream._events.pause)
1.  object <span class="apidocSignatureSpan">n_.inputStream._events.</span>end
1.  object <span class="apidocSignatureSpan">n_.inputStream._events.</span>keypress

#### [module n_.inputStream._handle](#apidoc.module.n_.inputStream._handle)
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._handle.</span>reading
1.  [function <span class="apidocSignatureSpan">n_.inputStream._handle.</span>onread (nread, buffer)](#apidoc.element.n_.inputStream._handle.onread)
1.  number <span class="apidocSignatureSpan">n_.inputStream._handle.</span>bytesRead
1.  number <span class="apidocSignatureSpan">n_.inputStream._handle.</span>fd
1.  number <span class="apidocSignatureSpan">n_.inputStream._handle.</span>writeQueueSize
1.  object <span class="apidocSignatureSpan">n_.inputStream._handle.</span>_externalStream
1.  object <span class="apidocSignatureSpan">n_.inputStream._handle.</span>owner

#### [module n_.inputStream._writableState](#apidoc.module.n_.inputStream._writableState)
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>bufferProcessing
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>decodeStrings
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>ended
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>ending
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>errorEmitted
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>finished
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>needDrain
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>objectMode
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>prefinished
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>sync
1.  boolean <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>writing
1.  [function <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>onwrite (er)](#apidoc.element.n_.inputStream._writableState.onwrite)
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>bufferedRequestCount
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>corked
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>highWaterMark
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>length
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>pendingcb
1.  number <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>writelen
1.  object <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>bufferedRequest
1.  object <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>corkedRequestsFree
1.  object <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>lastBufferedRequest
1.  object <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>writecb
1.  string <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>defaultEncoding

#### [module n_.outputStream](#apidoc.module.n_.outputStream)
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>_hadError
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>_isStdio
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>allowHalfOpen
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>connecting
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>destroyed
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>readable
1.  boolean <span class="apidocSignatureSpan">n_.outputStream.</span>writable
1.  [function <span class="apidocSignatureSpan">n_.outputStream.</span>_write (chunk, encoding, callback)](#apidoc.element.n_.outputStream._write)
1.  [function <span class="apidocSignatureSpan">n_.outputStream.</span>_writeDefault (data, encoding, cb)](#apidoc.element.n_.outputStream._writeDefault)
1.  [function <span class="apidocSignatureSpan">n_.outputStream.</span>destroy (er)](#apidoc.element.n_.outputStream.destroy)
1.  [function <span class="apidocSignatureSpan">n_.outputStream.</span>destroySoon (er)](#apidoc.element.n_.outputStream.destroySoon)
1.  number <span class="apidocSignatureSpan">n_.outputStream.</span>_bytesDispatched
1.  number <span class="apidocSignatureSpan">n_.outputStream.</span>_eventsCount
1.  number <span class="apidocSignatureSpan">n_.outputStream.</span>columns
1.  number <span class="apidocSignatureSpan">n_.outputStream.</span>fd
1.  number <span class="apidocSignatureSpan">n_.outputStream.</span>rows
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_events
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_handle
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_host
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_parent
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_pendingData
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_readableState
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_server
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_sockname
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_writableState
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>_writev
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>domain
1.  object <span class="apidocSignatureSpan">n_.outputStream.</span>server
1.  string <span class="apidocSignatureSpan">n_.outputStream.</span>_pendingEncoding
1.  string <span class="apidocSignatureSpan">n_.outputStream.</span>_type

#### [module n_.outputStream._events](#apidoc.module.n_.outputStream._events)
1.  [function <span class="apidocSignatureSpan">n_.outputStream._events.</span>_socketEnd ()](#apidoc.element.n_.outputStream._events._socketEnd)
1.  [function <span class="apidocSignatureSpan">n_.outputStream._events.</span>end ()](#apidoc.element.n_.outputStream._events.end)
1.  [function <span class="apidocSignatureSpan">n_.outputStream._events.</span>finish ()](#apidoc.element.n_.outputStream._events.finish)
1.  object <span class="apidocSignatureSpan">n_.outputStream._events.</span>resize

#### [module n_.outputStream._handle](#apidoc.module.n_.outputStream._handle)
1.  [function <span class="apidocSignatureSpan">n_.outputStream._handle.</span>onread (nread, buffer)](#apidoc.element.n_.outputStream._handle.onread)
1.  number <span class="apidocSignatureSpan">n_.outputStream._handle.</span>bytesRead
1.  number <span class="apidocSignatureSpan">n_.outputStream._handle.</span>fd
1.  number <span class="apidocSignatureSpan">n_.outputStream._handle.</span>writeQueueSize
1.  object <span class="apidocSignatureSpan">n_.outputStream._handle.</span>_externalStream
1.  object <span class="apidocSignatureSpan">n_.outputStream._handle.</span>owner

#### [module n_.outputStream._writableState](#apidoc.module.n_.outputStream._writableState)
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>bufferProcessing
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>decodeStrings
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>ended
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>ending
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>errorEmitted
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>finished
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>needDrain
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>objectMode
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>prefinished
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>sync
1.  boolean <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>writing
1.  [function <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>onwrite (er)](#apidoc.element.n_.outputStream._writableState.onwrite)
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>bufferedRequestCount
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>corked
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>highWaterMark
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>length
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>pendingcb
1.  number <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>writelen
1.  object <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>bufferedRequest
1.  object <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>corkedRequestsFree
1.  object <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>lastBufferedRequest
1.  object <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>writecb
1.  string <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>defaultEncoding



# <a name="apidoc.module.n_"></a>[module n_](#apidoc.module.n_)

#### <a name="apidoc.element.n_._ttyWrite"></a>[function <span class="apidocSignatureSpan">n_.</span>_ttyWrite (d, key)](#apidoc.element.n_._ttyWrite)
- description and source-code
```javascript
(d, key) => {
  key = key || {};
  if (!self.editorMode || !self.terminal) {
    ttyWrite(d, key);
    return;
  }

  // editor mode
  if (key.ctrl && !key.shift) {
    switch (key.name) {
      case 'd': // End editor mode
        self.turnOffEditorMode();
        sawCtrlD = true;
        ttyWrite(d, { name: 'return' });
        break;
      case 'n': // Override next history item
      case 'p': // Override previous history item
        break;
      default:
        ttyWrite(d, key);
    }
  } else {
    switch (key.name) {
      case 'up':   // Override previous history item
      case 'down': // Override next history item
        break;
      case 'tab':
        // prevent double tab behavior
        self._previousKey = null;
        ttyWrite(d, key);
        break;
      default:
        ttyWrite(d, key);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.completer"></a>[function <span class="apidocSignatureSpan">n_.</span>completer (text, cb)](#apidoc.element.n_.completer)
- description and source-code
```javascript
function completer(text, cb) {
  complete.call(self, text, self.editorMode
    ? self.completeOnEditorMode(cb) : cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer"></a>[function <span class="apidocSignatureSpan">n_.</span>context.Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.require"></a>[function <span class="apidocSignatureSpan">n_.</span>context.require (path)](#apidoc.element.n_.context.require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.eval"></a>[function <span class="apidocSignatureSpan">n_.</span>eval ()](#apidoc.element.n_.eval)
- description and source-code
```javascript
function runBound() {
  return bound(this, self, cb, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.writer"></a>[function <span class="apidocSignatureSpan">n_.</span>writer (obj, showHidden, depth)](#apidoc.element.n_.writer)
- description and source-code
```javascript
writer = function (obj, showHidden, depth) {
  return util.inspect(obj, showHidden, depth, true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_._events"></a>[module n_._events](#apidoc.module.n_._events)

#### <a name="apidoc.element.n_._events.SIGCONT"></a>[function <span class="apidocSignatureSpan">n_._events.</span>SIGCONT ()](#apidoc.element.n_._events.SIGCONT)
- description and source-code
```javascript
SIGCONT = function () {
  if (self.editorMode) {
    self.outputStream.write('${self._initialPrompt}.editor\n');
    self.outputStream.write(
      '// Entering editor mode (^D to finish, ^C to cancel)\n');
    self.outputStream.write('${self.bufferedCommand}\n');
    self.prompt(true);
  } else {
    self.displayPrompt(true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_._events.SIGINT"></a>[function <span class="apidocSignatureSpan">n_._events.</span>SIGINT ()](#apidoc.element.n_._events.SIGINT)
- description and source-code
```javascript
SIGINT = function () {
  var empty = self.line.length === 0;
  self.clearLine();
  self.turnOffEditorMode();

  if (!(self.bufferedCommand && self.bufferedCommand.length > 0) && empty) {
    if (sawSIGINT) {
      self.close();
      sawSIGINT = false;
      return;
    }
    self.output.write('(To exit, press ^C again or type .exit)\n');
    sawSIGINT = true;
  } else {
    sawSIGINT = false;
  }

  self.lineParser.reset();
  self.bufferedCommand = '';
  self.lines.level = [];
  self.displayPrompt();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_._events.line"></a>[function <span class="apidocSignatureSpan">n_._events.</span>line (line, cmd)](#apidoc.element.n_._events.line)
- description and source-code
```javascript
line = function (line, cmd) {
<span class="apidocCodeCommentSpan">/* [wrapped with _.partial] */
</span>    var context = server.context;
    line[0](cmd); // actual command execution
    line[1](cmd); // history persistance
    redirect(context);
    currVal = prevVal;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_._events.close"></a>[module n_._events.close](#apidoc.module.n_._events.close)

#### <a name="apidoc.element.n_._events.close.0"></a>[function <span class="apidocSignatureSpan">n_._events.close.</span>0 ()](#apidoc.element.n_._events.close.0)
- description and source-code
```javascript
function g() {
  target.removeListener(type, g);
  if (!fired) {
    fired = true;
    listener.apply(target, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_._events.close.1"></a>[function <span class="apidocSignatureSpan">n_._events.close.</span>1 ()](#apidoc.element.n_._events.close.1)
- description and source-code
```javascript
1 = function () {
  self.emit('exit');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context"></a>[module n_.context](#apidoc.module.n_.context)

#### <a name="apidoc.element.n_.context.Buffer"></a>[function <span class="apidocSignatureSpan">n_.context.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.clearImmediate"></a>[function <span class="apidocSignatureSpan">n_.context.</span>clearImmediate (immediate)](#apidoc.element.n_.context.clearImmediate)
- description and source-code
```javascript
clearImmediate = function (immediate) {
  if (!immediate) return;

  immediate._onImmediate = null;

  immediateQueue.remove(immediate);

  if (!immediateQueue.head) {
    process._needImmediateCallback = false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.clearInterval"></a>[function <span class="apidocSignatureSpan">n_.context.</span>clearInterval (timer)](#apidoc.element.n_.context.clearInterval)
- description and source-code
```javascript
clearInterval = function (timer) {
  if (timer && timer._repeat) {
    timer._repeat = null;
    clearTimeout(timer);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.clearTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.</span>clearTimeout (timer)](#apidoc.element.n_.context.clearTimeout)
- description and source-code
```javascript
clearTimeout = function (timer) {
  if (timer && (timer[kOnTimeout] || timer._onTimeout)) {
    timer[kOnTimeout] = timer._onTimeout = null;
    if (timer instanceof Timeout) {
      timer.close(); // for after === 0
    } else {
      unenroll(timer);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.debugInline"></a>[function <span class="apidocSignatureSpan">n_.context.</span>debugInline (arg)](#apidoc.element.n_.context.debugInline)
- description and source-code
```javascript
debugInline = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will both print the arg to stderr and return it
 */
</span>    // debug arguments
    local['_debug_inlineArguments'.replace('_i', 'I')] = arguments;
    console.error('\n\n\ndebug_inline'.replace('_i', 'I'));
    console.error.apply(console, arguments);
    console.error();
    // return arg for inspection
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.require"></a>[function <span class="apidocSignatureSpan">n_.context.</span>require (path)](#apidoc.element.n_.context.require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.setImmediate"></a>[function <span class="apidocSignatureSpan">n_.context.</span>setImmediate (callback, arg1, arg2, arg3)](#apidoc.element.n_.context.setImmediate)
- description and source-code
```javascript
setImmediate = function (callback, arg1, arg2, arg3) {
  if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  var i, args;

  switch (arguments.length) {
    // fast cases
    case 1:
      break;
    case 2:
      args = [arg1];
      break;
    case 3:
      args = [arg1, arg2];
      break;
    default:
      args = [arg1, arg2, arg3];
      for (i = 4; i < arguments.length; i++)
        // extend array dynamically, makes .apply run much faster in v6.0.0
        args[i - 1] = arguments[i];
      break;
  }
  return createImmediate(args, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.setInterval"></a>[function <span class="apidocSignatureSpan">n_.context.</span>setInterval (callback, repeat, arg1, arg2, arg3)](#apidoc.element.n_.context.setInterval)
- description and source-code
```javascript
setInterval = function (callback, repeat, arg1, arg2, arg3) {
  if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  var len = arguments.length;
  var args;
  if (len === 3) {
    args = [arg1];
  } else if (len === 4) {
    args = [arg1, arg2];
  } else if (len > 4) {
    args = [arg1, arg2, arg3];
    for (var i = 5; i < len; i++)
      // extend array dynamically, makes .apply run much faster in v6.0.0
      args[i - 2] = arguments[i];
  }

  return createRepeatTimeout(callback, repeat, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.setTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.</span>setTimeout (callback, after, arg1, arg2, arg3)](#apidoc.element.n_.context.setTimeout)
- description and source-code
```javascript
setTimeout = function (callback, after, arg1, arg2, arg3) {
  if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  var len = arguments.length;
  var args;
  if (len === 3) {
    args = [arg1];
  } else if (len === 4) {
    args = [arg1, arg2];
  } else if (len > 4) {
    args = [arg1, arg2, arg3];
    for (var i = 5; i < len; i++)
      // extend array dynamically, makes .apply run much faster in v6.0.0
      args[i - 2] = arguments[i];
  }

  return createSingleTimeout(callback, after, args);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.Buffer"></a>[module n_.context.Buffer](#apidoc.module.n_.context.Buffer)

#### <a name="apidoc.element.n_.context.Buffer.Buffer"></a>[function <span class="apidocSignatureSpan">n_.context.</span>Buffer (arg, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer.Buffer)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.alloc"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>alloc (size, fill, encoding)](#apidoc.element.n_.context.Buffer.alloc)
- description and source-code
```javascript
alloc = function (size, fill, encoding) {
  assertSize(size);
  if (size > 0 && fill !== undefined) {
    // Since we are filling anyway, don't zero fill initially.
    // Only pay attention to encoding if it's a string. This
    // prevents accidentally sending in a number that would
    // be interpretted as a start offset.
    if (typeof encoding !== 'string')
      encoding = undefined;
    return createUnsafeBuffer(size).fill(fill, encoding);
  }
  return new FastBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.allocUnsafe"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>allocUnsafe (size)](#apidoc.element.n_.context.Buffer.allocUnsafe)
- description and source-code
```javascript
allocUnsafe = function (size) {
  assertSize(size);
  return allocate(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.allocUnsafeSlow"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>allocUnsafeSlow (size)](#apidoc.element.n_.context.Buffer.allocUnsafeSlow)
- description and source-code
```javascript
allocUnsafeSlow = function (size) {
  assertSize(size);
  return createUnsafeBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.byteLength"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>byteLength (string, encoding)](#apidoc.element.n_.context.Buffer.byteLength)
- description and source-code
```javascript
function byteLength(string, encoding) {
  if (typeof string !== 'string') {
    if (ArrayBuffer.isView(string) || isArrayBuffer(string) ||
        isSharedArrayBuffer(string)) {
      return string.byteLength;
    }

    string = '' + string;
  }

  var len = string.length;
  if (len === 0)
    return 0;

  // Use a for loop to avoid recursion
  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'ascii':
      case 'latin1':
      case 'binary':
        return len;

      case 'utf8':
      case 'utf-8':
      case undefined:
        return binding.byteLengthUtf8(string);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return len * 2;

      case 'hex':
        return len >>> 1;

      case 'base64':
        return base64ByteLength(string, len);

      default:
        // The C++ binding defaulted to UTF8, we should too.
        if (loweredCase)
          return binding.byteLengthUtf8(string);

        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.compare"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>compare (a, b)](#apidoc.element.n_.context.Buffer.compare)
- description and source-code
```javascript
function compare(a, b) {
  if (!(a instanceof Buffer) ||
      !(b instanceof Buffer)) {
    throw new TypeError('Arguments must be Buffers');
  }

  if (a === b) {
    return 0;
  }

  return binding.compare(a, b);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.concat"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>concat (list, length)](#apidoc.element.n_.context.Buffer.concat)
- description and source-code
```javascript
concat = function (list, length) {
  var i;
  if (!Array.isArray(list))
    throw new TypeError('"list" argument must be an Array of Buffers');

  if (list.length === 0)
    return new FastBuffer();

  if (length === undefined) {
    length = 0;
    for (i = 0; i < list.length; i++)
      length += list[i].length;
  } else {
    length = length >>> 0;
  }

  var buffer = Buffer.allocUnsafe(length);
  var pos = 0;
  for (i = 0; i < list.length; i++) {
    var buf = list[i];
    if (!Buffer.isBuffer(buf))
      throw new TypeError('"list" argument must be an Array of Buffers');
    buf.copy(buffer, pos);
    pos += buf.length;
  }

  // Note: 'length' is always equal to 'buffer.length' at this point
  if (pos < length) {
    // Zero-fill the remaining bytes if the specified 'length' was more than
    // the actual total length, i.e. if we have some remaining allocated bytes
    // there were not initialized.
    buffer.fill(0, pos, length);
  }

  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.from"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>from (value, encodingOrOffset, length)](#apidoc.element.n_.context.Buffer.from)
- description and source-code
```javascript
from = function (value, encodingOrOffset, length) {
  if (typeof value === 'number')
    throw new TypeError('"value" argument must not be a number');

  if (isArrayBuffer(value) || isSharedArrayBuffer(value))
    return fromArrayBuffer(value, encodingOrOffset, length);

  if (typeof value === 'string')
    return fromString(value, encodingOrOffset);

  return fromObject(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.isBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>isBuffer (b)](#apidoc.element.n_.context.Buffer.isBuffer)
- description and source-code
```javascript
function isBuffer(b) {
  return b instanceof Buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.isEncoding"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.</span>isEncoding (encoding)](#apidoc.element.n_.context.Buffer.isEncoding)
- description and source-code
```javascript
isEncoding = function (encoding) {
  return typeof encoding === 'string' &&
         typeof internalUtil.normalizeEncoding(encoding) === 'string';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.Buffer.prototype"></a>[module n_.context.Buffer.prototype](#apidoc.module.n_.context.Buffer.prototype)

#### <a name="apidoc.element.n_.context.Buffer.prototype.asciiSlice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>asciiSlice ()](#apidoc.element.n_.context.Buffer.prototype.asciiSlice)
- description and source-code
```javascript
function asciiSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.asciiWrite"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>asciiWrite ()](#apidoc.element.n_.context.Buffer.prototype.asciiWrite)
- description and source-code
```javascript
function asciiWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.base64Slice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>base64Slice ()](#apidoc.element.n_.context.Buffer.prototype.base64Slice)
- description and source-code
```javascript
function base64Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.base64Write"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>base64Write ()](#apidoc.element.n_.context.Buffer.prototype.base64Write)
- description and source-code
```javascript
function base64Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.compare"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.n_.context.Buffer.prototype.compare)
- description and source-code
```javascript
function compare(target, start, end, thisStart, thisEnd) {

  if (!(target instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');
  if (arguments.length === 1)
    return compare_(this, target);

  if (start === undefined)
    start = 0;
  else if (start < 0)
    throw new RangeError('out of range index');
  else
    start >>>= 0;

  if (end === undefined)
    end = target.length;
  else if (end > target.length)
    throw new RangeError('out of range index');
  else
    end >>>= 0;

  if (thisStart === undefined)
    thisStart = 0;
  else if (thisStart < 0)
    throw new RangeError('out of range index');
  else
    thisStart >>>= 0;

  if (thisEnd === undefined)
    thisEnd = this.length;
  else if (thisEnd > this.length)
    throw new RangeError('out of range index');
  else
    thisEnd >>>= 0;

  if (thisStart >= thisEnd)
    return (start >= end ? 0 : -1);
  else if (start >= end)
    return 1;

  return compareOffset(this, target, start, thisStart, end, thisEnd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.copy"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>copy ()](#apidoc.element.n_.context.Buffer.prototype.copy)
- description and source-code
```javascript
function copy() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.equals"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>equals (b)](#apidoc.element.n_.context.Buffer.prototype.equals)
- description and source-code
```javascript
function equals(b) {
  if (!(b instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');

  if (this === b)
    return true;

  return binding.compare(this, b) === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.fill"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.n_.context.Buffer.prototype.fill)
- description and source-code
```javascript
function fill(val, start, end, encoding) {
  // Handle string cases:
  if (typeof val === 'string') {
    if (typeof start === 'string') {
      encoding = start;
      start = 0;
      end = this.length;
    } else if (typeof end === 'string') {
      encoding = end;
      end = this.length;
    }

    if (encoding !== undefined && typeof encoding !== 'string') {
      throw new TypeError('encoding must be a string');
    }
    var normalizedEncoding = internalUtil.normalizeEncoding(encoding);
    if (normalizedEncoding === undefined) {
      throw new TypeError('Unknown encoding: ' + encoding);
    }

    if (val.length === 0) {
      // Previously, if val === '', the Buffer would not fill,
      // which is rather surprising.
      val = 0;
    } else if (val.length === 1) {
      var code = val.charCodeAt(0);
      if ((normalizedEncoding === 'utf8' && code < 128) ||
          normalizedEncoding === 'latin1') {
        // Fast path: If 'val' fits into a single byte, use that numeric value.
        val = code;
      }
    }
  } else if (typeof val === 'number') {
    val = val & 255;
  }

  // Invalid ranges are not set to a default, so can range check early.
  if (start < 0 || end > this.length)
    throw new RangeError('Out of range index');

  if (end <= start)
    return this;

  start = start >>> 0;
  end = end === undefined ? this.length : end >>> 0;

  binding.fill(this, val, start, end, encoding);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.hexSlice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>hexSlice ()](#apidoc.element.n_.context.Buffer.prototype.hexSlice)
- description and source-code
```javascript
function hexSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.hexWrite"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>hexWrite ()](#apidoc.element.n_.context.Buffer.prototype.hexWrite)
- description and source-code
```javascript
function hexWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.includes"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.includes)
- description and source-code
```javascript
function includes(val, byteOffset, encoding) {
  return this.indexOf(val, byteOffset, encoding) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.indexOf)
- description and source-code
```javascript
function indexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.inspect"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>inspect ()](#apidoc.element.n_.context.Buffer.prototype.inspect)
- description and source-code
```javascript
function inspect() {
  var str = '';
  var max = exports.INSPECT_MAX_BYTES;
  if (this.length > 0) {
    str = this.toString('hex', 0, max).match(/.{2}/g).join(' ');
    if (this.length > max)
      str += ' ... ';
  }
  return '<' + this.constructor.name + ' ' + str + '>';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.n_.context.Buffer.prototype.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.latin1Slice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>latin1Slice ()](#apidoc.element.n_.context.Buffer.prototype.latin1Slice)
- description and source-code
```javascript
function latin1Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.latin1Write"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>latin1Write ()](#apidoc.element.n_.context.Buffer.prototype.latin1Write)
- description and source-code
```javascript
function latin1Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readDoubleBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readDoubleBE)
- description and source-code
```javascript
function readDoubleBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readDoubleLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readDoubleLE)
- description and source-code
```javascript
function readDoubleLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readFloatBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readFloatBE)
- description and source-code
```javascript
function readFloatBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readFloatLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readFloatLE)
- description and source-code
```javascript
function readFloatLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readInt16BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt16BE)
- description and source-code
```javascript
readInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset + 1] | (this[offset] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readInt16LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt16LE)
- description and source-code
```javascript
readInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset] | (this[offset + 1] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readInt32BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt32BE)
- description and source-code
```javascript
readInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] << 24) |
      (this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      (this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readInt32LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt32LE)
- description and source-code
```javascript
readInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16) |
      (this[offset + 3] << 24);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readInt8"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readInt8)
- description and source-code
```javascript
readInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  var val = this[offset];
  return !(val & 0x80) ? val : (0xff - val + 1) * -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readIntBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readIntBE)
- description and source-code
```javascript
readIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var i = byteLength;
  var mul = 1;
  var val = this[offset + --i];
  while (i > 0 && (mul *= 0x100))
    val += this[offset + --i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readIntLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readIntLE)
- description and source-code
```javascript
readIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUInt16BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt16BE)
- description and source-code
```javascript
readUInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return (this[offset] << 8) | this[offset + 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUInt16LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt16LE)
- description and source-code
```javascript
readUInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return this[offset] | (this[offset + 1] << 8);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUInt32BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt32BE)
- description and source-code
```javascript
readUInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] * 0x1000000) +
      ((this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUInt32LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt32LE)
- description and source-code
```javascript
readUInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return ((this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16)) +
      (this[offset + 3] * 0x1000000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUInt8"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUInt8)
- description and source-code
```javascript
readUInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  return this[offset];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUIntBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUIntBE)
- description and source-code
```javascript
readUIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset + --byteLength];
  var mul = 1;
  while (byteLength > 0 && (mul *= 0x100))
    val += this[offset + --byteLength] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.readUIntLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.readUIntLE)
- description and source-code
```javascript
readUIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.slice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>slice (start, end)](#apidoc.element.n_.context.Buffer.prototype.slice)
- description and source-code
```javascript
function slice(start, end) {
  const srcLength = this.length;
  start = adjustOffset(start, srcLength);
  end = end !== undefined ? adjustOffset(end, srcLength) : srcLength;
  const newLength = end > start ? end - start : 0;
  return new FastBuffer(this.buffer, this.byteOffset + start, newLength);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.swap16"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap16 ()](#apidoc.element.n_.context.Buffer.prototype.swap16)
- description and source-code
```javascript
function swap16() {
  // For Buffer.length < 128, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 2 !== 0)
    throw new RangeError('Buffer size must be a multiple of 16-bits');
  if (len < 128) {
    for (var i = 0; i < len; i += 2)
      swap(this, i, i + 1);
    return this;
  }
  return swap16n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.swap32"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap32 ()](#apidoc.element.n_.context.Buffer.prototype.swap32)
- description and source-code
```javascript
function swap32() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 4 !== 0)
    throw new RangeError('Buffer size must be a multiple of 32-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 4) {
      swap(this, i, i + 3);
      swap(this, i + 1, i + 2);
    }
    return this;
  }
  return swap32n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.swap64"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>swap64 ()](#apidoc.element.n_.context.Buffer.prototype.swap64)
- description and source-code
```javascript
function swap64() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 8 !== 0)
    throw new RangeError('Buffer size must be a multiple of 64-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 8) {
      swap(this, i, i + 7);
      swap(this, i + 1, i + 6);
      swap(this, i + 2, i + 5);
      swap(this, i + 3, i + 4);
    }
    return this;
  }
  return swap64n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>toJSON ()](#apidoc.element.n_.context.Buffer.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  if (this.length) {
    const data = [];
    for (var i = 0; i < this.length; ++i)
      data[i] = this[i];
    return { type: 'Buffer', data };
  } else {
    return { type: 'Buffer', data: [] };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.toString"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>toString ()](#apidoc.element.n_.context.Buffer.prototype.toString)
- description and source-code
```javascript
toString = function () {
  let result;
  if (arguments.length === 0) {
    result = this.utf8Slice(0, this.length);
  } else {
    result = slowToString.apply(this, arguments);
  }
  if (result === undefined)
    throw new Error('"toString()" failed');
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.ucs2Slice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>ucs2Slice ()](#apidoc.element.n_.context.Buffer.prototype.ucs2Slice)
- description and source-code
```javascript
function ucs2Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.ucs2Write"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>ucs2Write ()](#apidoc.element.n_.context.Buffer.prototype.ucs2Write)
- description and source-code
```javascript
function ucs2Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.utf8Slice"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>utf8Slice ()](#apidoc.element.n_.context.Buffer.prototype.utf8Slice)
- description and source-code
```javascript
function utf8Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.utf8Write"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>utf8Write ()](#apidoc.element.n_.context.Buffer.prototype.utf8Write)
- description and source-code
```javascript
function utf8Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.write"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.n_.context.Buffer.prototype.write)
- description and source-code
```javascript
write = function (string, offset, length, encoding) {
  // Buffer#write(string);
  if (offset === undefined) {
    encoding = 'utf8';
    length = this.length;
    offset = 0;

  // Buffer#write(string, encoding)
  } else if (length === undefined && typeof offset === 'string') {
    encoding = offset;
    length = this.length;
    offset = 0;

  // Buffer#write(string, offset[, length][, encoding])
  } else if (isFinite(offset)) {
    offset = offset >>> 0;
    if (isFinite(length)) {
      length = length >>> 0;
      if (encoding === undefined)
        encoding = 'utf8';
    } else {
      encoding = length;
      length = undefined;
    }
  } else {
    // if someone is still calling the obsolete form of write(), tell them.
    // we don't want eg buf.write("foo", "utf8", 10) to silently turn into
    // buf.write("foo", "utf8"), so we can't ignore extra args
    throw new Error('Buffer.write(string, encoding, offset[, length]) ' +
                    'is no longer supported');
  }

  var remaining = this.length - offset;
  if (length === undefined || length > remaining)
    length = remaining;

  if (string.length > 0 && (length < 0 || offset < 0))
    throw new RangeError('Attempt to write outside buffer bounds');

  if (!encoding)
    encoding = 'utf8';

  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'hex':
        return this.hexWrite(string, offset, length);

      case 'utf8':
      case 'utf-8':
        return this.utf8Write(string, offset, length);

      case 'ascii':
        return this.asciiWrite(string, offset, length);

      case 'latin1':
      case 'binary':
        return this.latin1Write(string, offset, length);

      case 'base64':
        // Warning: maxLength not taken into account in base64Write
        return this.base64Write(string, offset, length);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return this.ucs2Write(string, offset, length);

      default:
        if (loweredCase)
          throw new TypeError('Unknown encoding: ' + encoding);
        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeDoubleBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeDoubleBE)
- description and source-code
```javascript
function writeDoubleBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleBE(this, val, offset);
  else
    binding.writeDoubleBE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeDoubleLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeDoubleLE)
- description and source-code
```javascript
function writeDoubleLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleLE(this, val, offset);
  else
    binding.writeDoubleLE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeFloatBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeFloatBE)
- description and source-code
```javascript
function writeFloatBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatBE(this, val, offset);
  else
    binding.writeFloatBE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeFloatLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeFloatLE)
- description and source-code
```javascript
function writeFloatLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatLE(this, val, offset);
  else
    binding.writeFloatLE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeInt16BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt16BE)
- description and source-code
```javascript
writeInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeInt16LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt16LE)
- description and source-code
```javascript
writeInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeInt32BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt32BE)
- description and source-code
```javascript
writeInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeInt32LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt32LE)
- description and source-code
```javascript
writeInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  this[offset + 2] = (value >>> 16);
  this[offset + 3] = (value >>> 24);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeInt8"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeInt8)
- description and source-code
```javascript
writeInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0x7f, -0x80);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeIntBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeIntBE)
- description and source-code
```javascript
writeIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = byteLength - 1;
  var mul = 1;
  var sub = 0;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i + 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeIntLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeIntLE)
- description and source-code
```javascript
writeIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = 0;
  var mul = 1;
  var sub = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i - 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUInt16BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt16BE)
- description and source-code
```javascript
writeUInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUInt16LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt16LE)
- description and source-code
```javascript
writeUInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUInt32BE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt32BE)
- description and source-code
```javascript
writeUInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUInt32LE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt32LE)
- description and source-code
```javascript
writeUInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset + 3] = (value >>> 24);
  this[offset + 2] = (value >>> 16);
  this[offset + 1] = (value >>> 8);
  this[offset] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUInt8"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUInt8)
- description and source-code
```javascript
writeUInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0xff, 0);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUIntBE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUIntBE)
- description and source-code
```javascript
writeUIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var i = byteLength - 1;
  var mul = 1;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.Buffer.prototype.writeUIntLE"></a>[function <span class="apidocSignatureSpan">n_.context.Buffer.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.n_.context.Buffer.prototype.writeUIntLE)
- description and source-code
```javascript
writeUIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var mul = 1;
  var i = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.console"></a>[module n_.context.console](#apidoc.module.n_.context.console)

#### <a name="apidoc.element.n_.context.console.assert"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>assert ()](#apidoc.element.n_.context.console.assert)
- description and source-code
```javascript
assert = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.dir"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>dir ()](#apidoc.element.n_.context.console.dir)
- description and source-code
```javascript
dir = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.error"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>error ()](#apidoc.element.n_.context.console.error)
- description and source-code
```javascript
error = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.info"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>info ()](#apidoc.element.n_.context.console.info)
- description and source-code
```javascript
info = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.log"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>log ()](#apidoc.element.n_.context.console.log)
- description and source-code
```javascript
log = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.time"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>time ()](#apidoc.element.n_.context.console.time)
- description and source-code
```javascript
time = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.timeEnd"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>timeEnd ()](#apidoc.element.n_.context.console.timeEnd)
- description and source-code
```javascript
timeEnd = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.trace"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>trace ()](#apidoc.element.n_.context.console.trace)
- description and source-code
```javascript
trace = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.console.warn"></a>[function <span class="apidocSignatureSpan">n_.context.console.</span>warn ()](#apidoc.element.n_.context.console.warn)
- description and source-code
```javascript
warn = function () { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.require"></a>[module n_.context.require](#apidoc.module.n_.context.require)

#### <a name="apidoc.element.n_.context.require.require"></a>[function <span class="apidocSignatureSpan">n_.context.</span>require (path)](#apidoc.element.n_.context.require.require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.require.resolve"></a>[function <span class="apidocSignatureSpan">n_.context.require.</span>resolve (request)](#apidoc.element.n_.context.require.resolve)
- description and source-code
```javascript
function resolve(request) {
  return Module._resolveFilename(request, self);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2"></a>[module n_.context.utility2](#apidoc.module.n_.context.utility2)

#### <a name="apidoc.element.n_.context.utility2.Blob"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>Blob (array, options)](#apidoc.element.n_.context.utility2.Blob)
- description and source-code
```javascript
Blob = function (array, options) {
<span class="apidocCodeCommentSpan">  /*
   * this function will create a node-compatible Blob instance
   */
</span>    this.bff = local.bufferConcat(array);
    this.type = options && options.type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.FormData"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>FormData ()](#apidoc.element.n_.context.utility2.FormData)
- description and source-code
```javascript
FormData = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a serverLocal-compatible FormData instance
 * https://xhr.spec.whatwg.org/#dom-formdata
 * The FormData(form) constructor must run these steps:
 * 1. Let fd be a new FormData object.
 * 2. If form is given, set fd's entries to the result
 *    of constructing the form data set for form. (not implemented)
 * 3. Return fd.
 */
</span>    this.entryList = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>HtmlReport (e)](#apidoc.element.n_.context.utility2.HtmlReport)
- description and source-code
```javascript
function HtmlReport(e){Report.call(this),this.opts=e||{},this.opts.dir=this.opts.dir||path.resolve(
process.cwd(),"html-report"),this.opts.sourceStore=this.opts.sourceStore||Store.
create("fslookup"),this.opts.linkMapper=this.opts.linkMapper||this.standardLinkMapper
(),this.opts.writer=this.opts.writer||null,this.opts.templateData={datetime:Date
()},this.opts.watermarks=this.opts.watermarks||defaults.watermarks()}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>Instrumenter (e)](#apidoc.element.n_.context.utility2.Instrumenter)
- description and source-code
```javascript
function g(e){this.opts=e||{debug:!1,walkDebug:!1,coverageVariable:"__coverage__"
,codeGenerationOptions:undefined,noAutoWrap:!1,noCompact:!1,embedSource:!1,preserveComments
:!1},this.walker=new v({ArrowFunctionExpression:[this.arrowBlockConverter],ExpressionStatement
:this.coverStatement,BreakStatement:this.coverStatement,ContinueStatement:this.coverStatement
,DebuggerStatement:this.coverStatement,ReturnStatement:this.coverStatement,ThrowStatement
:this.coverStatement,TryStatement:[this.paranoidHandlerCheck,this.coverStatement
],VariableDeclaration:this.coverStatement,IfStatement:[this.ifBlockConverter,this
.coverStatement,this.ifBranchInjector],ForStatement:[this.skipInit,this.loopBlockConverter
,this.coverStatement],ForInStatement:[this.skipLeft,this.loopBlockConverter,this
.coverStatement],ForOfStatement:[this.skipLeft,this.loopBlockConverter,this.coverStatement
],WhileStatement:[this.loopBlockConverter,this.coverStatement],DoWhileStatement:
[this.loopBlockConverter,this.coverStatement],SwitchStatement:[this.coverStatement
,this.switchBranchInjector],SwitchCase:[this.switchCaseInjector],WithStatement:[
this.withBlockConverter,this.coverStatement],FunctionDeclaration:[this.coverFunction
,this.coverStatement],FunctionExpression:this.coverFunction,LabeledStatement:this
.coverStatement,ConditionalExpression:this.conditionalBranchInjector,LogicalExpression
:this.logicalExpressionBranchInjector,ObjectExpression:this.maybeAddType},this.extractCurrentHint
,this,this.opts.walkDebug),this.opts.backdoor&&this.opts.backdoor.omitTrackerSuffix&&
(this.omitTrackerSuffix=!0)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.JSLINT"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>JSLINT (t, n)](#apidoc.element.n_.context.utility2.JSLINT)
- description and source-code
```javascript
JSLINT = function (t, n){var r,o,u;S.errors=[],S.tree="",S.properties="",i=P=X=O=Object
.create(W["(begin)"]),V=[],_=Object.create(null),st(U),H=Object.create(null);if(
n){M=Object.create(n),o=M.predef;if(o)if(Array.isArray(o))for(r=0;r<o.length;r+=1
)_[o[r]]=!0;else typeof o=="object"&&st(o)}else M=Object.create(null);M.indent=+
M.indent||4,M.maxerr=+M.maxerr||50,b=q=Object.create(null),y=m={scope:q,loopage:0
,level:0},g=[m],s=[],f=[],l=!1,w=!1,E=null,x=!1,C=[],L=!1,D=!0,z=!1,$=null,J=0,T
.init(t),ot();try{dt();if(O.id==="(number)")O.stop("unexpected_a");else switch(O
.id){case"{":case"[":l=!0,x=!0,ln();break;default:bt(1),O.id===";"&&!L&&(O.edge=!0
,dt(";")),u=tn(),i.first=u,S.tree=i,u.disrupt&&P.warn("weird_program")}E=null,dt
("(end)"),S.property=H}catch(a){a&&S.errors.push({reason:a.message,line:a.line||
O.line,character:a.character||O.from},null)}return S.errors.length===0}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.MAP"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>MAP (r, i, s)](#apidoc.element.n_.context.utility2.MAP)
- description and source-code
```javascript
MAP = function (r, i, s){function f(){var f=i.call(s,r[a],a);f instanceof t?(f=f.v,f instanceof n?u.
push.apply(u,f.v):u.push(f)):f!=e&&(f instanceof n?o.push.apply(o,f.v):o.push(f)
)}var o=[],u=[],a;if(r instanceof Array)for(a=0;a<r.length;++a)f();else for(a in
r)HOP(r,a)&&f();return u.concat(o)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Module"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>Module (id, parent)](#apidoc.element.n_.context.utility2.Module)
- description and source-code
```javascript
function Module(id, parent) {
  this.id = id;
  this.exports = {};
  this.parent = parent;
  if (parent && parent.children) {
    parent.children.push(this);
  }

  this.filename = null;
  this.loaded = false;
  this.children = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.TextReport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>TextReport (e)](#apidoc.element.n_.context.utility2.TextReport)
- description and source-code
```javascript
function TextReport(e){Report.call(this),e=e||{},this.dir=e.dir||process.cwd(),this
.file=e.file,this.summary=e.summary,this.maxCols=e.maxCols||0,this.watermarks=e.
watermarks||defaults.watermarks()}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_DbTable (options)](#apidoc.element.n_.context.utility2._DbTable)
- description and source-code
```javascript
_DbTable = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a dbTable
 */
</span>    options = local.normalizeDict(options);
    this.name = String(options.name);
    // register dbTable in dbTableDict
    local.dbTableDict[this.name] = this;
    this.dbRowList = [];
    this.isDirty = null;
    this.idIndexList = [{ name: '_id', dict: {} }];
    this.onSaveList = [];
    this.ttl = 0;
    this.ttlLast = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.__require"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>__require (path)](#apidoc.element.n_.context.utility2.__require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._middlewareError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_middlewareError (error, request, response)](#apidoc.element.n_.context.utility2._middlewareError)
- description and source-code
```javascript
_middlewareError = function (error, request, response) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * handle errors according to http://jsonapi.org/format/#errors
 */
</span>    if (!error) {
        error = new Error('404 Not Found');
        error.statusCode = 404;
    }
    local.serverRespondJsonapi(request, response, error);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._middlewareJsonpStateInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_middlewareJsonpStateInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2._middlewareJsonpStateInit)
- description and source-code
```javascript
_middlewareJsonpStateInit = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * serve the browser-state wrapped in the given jsonp-callback
 */
</span>    var state;
    if (request._stateInit || (request.urlParsed &&
            request.urlParsed.pathname === '/jsonp.utility2._stateInit')) {
        state = { utility2: { assetsDict: {
            '/assets.index.template.html':
                local.assetsDict['/assets.index.template.html']
        } } };
        local.objectSetDefault(state, { utility2: { env: {
            NODE_ENV: local.env.NODE_ENV,
            npm_config_mode_backend: local.env.npm_config_mode_backend,
            npm_package_description: local.env.npm_package_description,
            npm_package_homepage: local.env.npm_package_homepage,
            npm_package_name: local.env.npm_package_name,
            npm_package_nameAlias: local.env.npm_package_nameAlias,
            npm_package_version: local.env.npm_package_version
        } } }, 3);
        if (request._stateInit) {
            return state;
        }
        response.end(
            request.urlParsed.query.callback + '(' + JSON.stringify(state) + ');'
        );
        return;
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._serverLocalUrlTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_serverLocalUrlTest ()](#apidoc.element.n_.context.utility2._serverLocalUrlTest)
- description and source-code
```javascript
_serverLocalUrlTest = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._stateInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_stateInit (options)](#apidoc.element.n_.context.utility2._stateInit)
- description and source-code
```javascript
_stateInit = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will init the state-options
 */
</span>    local.objectSetOverride(local, options, 10);
    // init api
    local.apiDictUpdate(local.swaggerJson);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._testRunBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>_testRunBefore ()](#apidoc.element.n_.context.utility2._testRunBefore)
- description and source-code
```javascript
_testRunBefore = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ajax"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ajax (options, onError)](#apidoc.element.n_.context.utility2.ajax)
- description and source-code
```javascript
ajax = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will send an ajax-request with error-handling and timeout
 */
</span>    var timerTimeout, tmp, xhr;
    onError = local.onErrorWithStack(onError);
    // init modeServerLocal
    if (!local.env.npm_config_mode_backend && local._serverLocalUrlTest(options.url)) {
        xhr = new local._http.XMLHttpRequest();
    }
    // init xhr
    xhr = xhr || (local.modeJs === 'browser'
        ? new local.global.XMLHttpRequest()
        : new local._http.XMLHttpRequest());
    // debug xhr
    local._debugXhr = xhr;
    // init options
    local.objectSetOverride(xhr, options);
    // init headers
    xhr.headers = {};
    Object.keys(options.headers || {}).forEach(function (key) {
        xhr.headers[key.toLowerCase()] = options.headers[key];
    });
    // init method
    xhr.method = xhr.method || 'GET';
    // init timeout
    xhr.timeout = xhr.timeout || local.timeoutDefault;
    // init timerTimeout
    timerTimeout = local.onTimeout(function (error) {
        xhr.error = xhr.error || error;
        xhr.abort();
        // cleanup requestStream and responseStream
        local.streamListCleanup([xhr.requestStream, xhr.responseStream]);
    }, xhr.timeout, 'ajax ' + xhr.method + ' ' + xhr.url);
    // init event handling
    xhr.onEvent = function (event) {
        // init statusCode
        xhr.statusCode = xhr.status;
        switch (event.type) {
        case 'abort':
        case 'error':
        case 'load':
            // do not run more than once
            if (xhr.done) {
                return;
            }
            xhr.done = true;
            // cleanup timerTimeout
            clearTimeout(timerTimeout);
            // cleanup requestStream and responseStream
            setTimeout(function () {
                local.streamListCleanup([xhr.requestStream, xhr.responseStream]);
            });
            // decrement ajaxProgressCounter
            local.ajaxProgressCounter -= 1;
            // handle abort or error event
            if (!xhr.error &&
                    (event.type === 'abort' ||
                    event.type === 'error' ||
                    xhr.statusCode >= 400)) {
                xhr.error = new Error(event.type);
            }
            // handle completed xhr request
            if (xhr.readyState === 4) {
                // debug xhr
                if (xhr.modeDebug) {
                    console.error(new Date().toISOString(
                    ) + ' ajax-response ' + JSON.stringify({
                        statusCode: xhr.statusCode,
                        method: xhr.method,
                        url: xhr.url,
                        responseText: local.tryCatchOnError(function () {
                            return xhr.responseText.slice(0, 256);
                        }, local.nop)
                    }));
                }
                // handle string data
                if (xhr.error) {
                    // debug statusCode
                    xhr.error.statusCode = xhr.statusCode;
                    // debug statusCode / method / url
                    tmp = local.modeJs + ' - ' + xhr.statusCode + ' ' + xhr.method +
                        ' ' + xhr.url + '\n';
                    // try to debug responseText
                    local.tryCatchOnError(function () {
                        tmp += '    ' + JSON.stringify(xhr.responseText.slice(0, 256) +
                            '...') + '\n';
                    }, local.nop);
                    local.errorMessagePrepend(xhr.error, tmp);
                }
            }
            onError(xhr.error, xhr);
            break;
        }
        local.ajaxProgressUpdate();
    };
    // increment ajaxProgressCounter
    local.ajaxProgressCounter += 1;
    xhr.addEventListener('abort', xhr.onEvent);
    xhr.addEventListener('error', xhr.onEvent);
    xhr.addEventListener('load', xhr.onEvent);
    xhr.addEventListener('loadstart', local.ajaxProgressUpdate);
    xhr.addEventListener('progress', local.ajaxProgressUpdate);
    xhr.upload.addEventListener('progress', local.a ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ajaxProgressUpdate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ajaxProgressUpdate ()](#apidoc.element.n_.context.utility2.ajaxProgressUpdate)
- description and source-code
```javascript
ajaxProgressUpdate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will update ajaxProgress
 */
</span>    var ajaxProgressDiv1;
    ajaxProgressDiv1 = local.modeJs === 'browser' &&
        document.querySelector('#ajaxProgressDiv1');
    if (!ajaxProgressDiv1) {
        return;
    }
    // init ajaxProgressDiv1StyleBackground
    local.ajaxProgressDiv1StyleBackground = local.ajaxProgressDiv1StyleBackground ||
        ajaxProgressDiv1.style.background;
    // show ajaxProgress
    if (ajaxProgressDiv1.style.background === 'transparent') {
        ajaxProgressDiv1.style.background = local.ajaxProgressDiv1StyleBackground;
    }
    // cleanup timerTimeout
    clearTimeout(local.timerTimeoutAjaxProgressHide);
    // increment ajaxProgress
    if (local.ajaxProgressCounter > 0) {
        // this algorithm will indefinitely increment the ajaxProgressBar
        // with successively smaller increments without ever reaching 100%
        local.ajaxProgressState += 1;
        ajaxProgressDiv1.style.width =
            100 - 75 * Math.exp(-0.125 * local.ajaxProgressState) + '%';
        return;
    }
    // finish ajaxProgress
    ajaxProgressDiv1.style.width = '100%';
    // hide ajaxProgress
    local.timerTimeoutAjaxProgressHide = setTimeout(function () {
        ajaxProgressDiv1.style.background = 'transparent';
        // reset ajaxProgress
        setTimeout(function () {
            local.ajaxProgressCounter = 0;
            local.ajaxProgressState = 0;
            ajaxProgressDiv1.style.width = '25%';
        }, 500);
    }, 1500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.apiAjax"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>apiAjax (self, options, onError)](#apidoc.element.n_.context.utility2.apiAjax)
- description and source-code
```javascript
apiAjax = function (self, options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will send a swagger-api ajax-request with the pathObject self
 */
</span>    var isMultipartFormData, tmp;
    isMultipartFormData = (self.consumes && self.consumes[0]) === 'multipart/form-data';
    local.objectSetDefault(options, { data: '', paramDict: {}, url: '' });
    // try to validate paramDict
    local.tryCatchOnError(function () {
        local.validateByParamDefList({
            // normalize paramDict
            data: local.normalizeParamDictSwagger(
                local.jsonCopy(options.paramDict),
                self
            ),
            dataReadonlyRemove: options.paramDict,
            key: self.operationId,
            paramDefList: self.parameters
        });
    }, function (error) {
        options.errorValidate = error;
        onError(error);
    });
    if (options.errorValidate) {
        return;
    }
    // init options-defaults
    local.objectSetDefault(options, {
        inForm: isMultipartFormData
            ? new local.FormData()
            : '',
        inHeader: {},
        inPath: self._path,
        inQuery: '',
        headers: {},
        method: self._method,
        responseType: self.produces &&
                self.produces[0].indexOf('application/octet-stream') === 0
            ? 'arraybuffer'
            : ''
    });
    // init paramDict
    self.parameters.forEach(function (paramDef) {
        tmp = options.paramDict[paramDef.name];
        if (tmp === undefined) {
            return;
        }
        // serialize array
        if (paramDef.type === 'array' && paramDef.in !== 'body') {
            if (typeof tmp !== 'string') {
                switch (paramDef.collectionFormat) {
                case 'json':
                    tmp = JSON.stringify(tmp);
                    break;
                case 'multi':
                    tmp.forEach(function (value) {
                        options[paramDef.in === 'formData'
                            ? 'inForm'
                            : 'inQuery'] += '&' +
                            encodeURIComponent(paramDef.name) + '=' +
                            encodeURIComponent(paramDef.items.type === 'string'
                                ? value
                                : JSON.stringify(value));
                    });
                    return;
                case 'pipes':
                    tmp = tmp.join('|');
                    break;
                case 'ssv':
                    tmp = tmp.join(' ');
                    break;
                case 'tsv':
                    tmp = tmp.join('\t');
                    break;
                // default to csv
                default:
                    tmp = tmp.join(',');
                }
            }
        } else if (!(paramDef.type === 'string' || tmp instanceof local.Blob)) {
            tmp = JSON.stringify(tmp);
        }
        switch (paramDef.in) {
        case 'body':
            options.inBody = tmp;
            break;
        case 'formData':
            if (isMultipartFormData) {
                options.inForm.append(paramDef.name, tmp, tmp && tmp.name);
                break;
            }
            options.inForm += '&' + encodeURIComponent(paramDef.name) + '=' +
                encodeURIComponent(tmp);
            break;
        case 'header':
            options.inHeader[encodeURIComponent(paramDef.name.toLowerCase())] = tmp;
            break;
        case 'query':
            options.inQuery += '&' + encodeURIComponent(paramDef.name) + '=' +
                encodeURIComponent(tmp);
            break;
        case 'path':
            options.inPath = options.inPath
                .replace('{' + paramDef.name + '}', encodeURIComponent(tmp));
            break;
        }
    });
    // init data
    options.data = options.inBody || (isMultipartFormData
        ? options.inForm
        : options.inForm.slice(1));
    // init headers
    local.objectSetOverride(options.headers, options.inHeader);
    // init headers - Content-Type
    if (options.inForm) {
        options.headers['Co ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.apiDictUpdate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>apiDictUpdate (options)](#apidoc.element.n_.context.utility2.apiDictUpdate)
- description and source-code
```javascript
apiDictUpdate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will update the swagger-api dict of api-calls
 */
</span>    var tmp;
    options = options || {};
    // init apiDict
    local.apiDict = local.apiDict || {};
    // init swaggerJson
    local.swaggerJson = local.swaggerJson || {
        "basePath": "/api/v0",
        "definitions": {
            "BuiltinFile": {
                "properties": {
                    "_id": {
                        "readOnly": true,
                        "type": "string"
                    },
                    "_timeCreated": {
                        "format": "date-time",
                        "readOnly": true,
                        "type": "string"
                    },
                    "_timeUpdated": {
                        "format": "date-time",
                        "readOnly": true,
                        "type": "string"
                    },
                    "fileBlob": {
                        "format": "byte",
                        "type": "string"
                    },
                    "fileContentType": {
                        "type": "string"
                    },
                    "fileDescription": {
                        "type": "string"
                    },
                    "fileFilename": {
                        "type": "string"
                    },
                    "fileInputName": {
                        "type": "string"
                    },
                    "fileSize": {
                        "minimum": 0,
                        "type": "integer"
                    },
                    "fileUrl": {
                        "type": "string"
                    },
                    "id": {
                        "type": "string"
                    }
                }
            },
            "BuiltinJsonapiResponse": {
                "properties": {
                    "data": {
                        "items": {
                            "type": "object"
                        },
                        "type": "array"
                    },
                    "errors": {
                        "items": {
                            "type": "object"
                        },
                        "type": "array"
                    },
                    "meta": {
                        "type": "object"
                    }
                }
            },
            "BuiltinUser": {
                "properties": {
                    "_id": {
                        "readOnly": true,
                        "type": "string"
                    },
                    "_timeCreated": {
                        "format": "date-time",
                        "readOnly": true,
                        "type": "string"
                    },
                    "_timeUpdated": {
                        "format": "date-time",
                        "readOnly": true,
                        "type": "string"
                    },
                    "id": {
                        "type": "string"
                    },
                    "jwtEncrypted": {
                        "type": "string"
                    },
                    "password": {
                        "format": "password",
                        "type": "string"
                    },
                    "username": {
                        "type": "string"
                    }
                }
            }
        },
        "info": {
            "description": "demo of swagger-ui server",
            "title": "swgg api",
            "version": "0"
        },
        "paths": {},
        "securityDefinitions": {},
        "swagger": "2.0",
        "tags": []
    };
    // save tags
    tmp = {};
    [local.swaggerJson.tags, options.tags || []].forEach(function (tagList) {
        tagList.forEach(function (tag) {
            local.objectSetOverride(tmp, local.objectLiteralize({
                '$[]': [tag.name, tag]
            }));
        }, 2);
    });
    tmp = Object.keys(tmp).sort().map(function (key) {
        return tmp[key]; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.apidocCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>apidocCreate (options)](#apidoc.element.n_.context.utility2.apidocCreate)
- description and source-code
```javascript
apidocCreate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create the apidoc from options.dir
 */
</span>    var elementCreate, module, moduleMain, readExample, tmp, trimLeft;
    elementCreate = function (module, prefix, key) {
    /*
     * this function will create the apidoc-element in the given module
     */
        var element;
        element = {};
        element.moduleName = prefix.split('.');
        // handle case where module is a function
        if (element.moduleName.slice(-1)[0] === key) {
            element.moduleName.pop();
        }
        element.moduleName = element.moduleName.join('.');
        element.id = encodeURIComponent('apidoc.element.' + prefix + '.' + key);
        element.typeof = typeof module[key];
        element.name = (element.typeof + ' <span class="apidocSignatureSpan">' +
            element.moduleName + '.</span>' + key)
            // handle case where module is a function
            .replace('>.<', '><');
        if (element.typeof !== 'function') {
            return element;
        }
        // init source
        element.source = 'n/a';
        // bug-workaround - catch and ignore error
        // "Function.prototype.toString is not generic"
        try {
            element.source = trimLeft(module[key].toString());
        } catch (ignore) {
        }
        if (element.source.length > 4096) {
            element.source = element.source.slice(0, 4096).trimRight() + ' ...';
        }
        element.source = (options.template === local.templateApidocHtml
            ? local.stringHtmlSafe(element.source)
            : element.source)
            .replace((/\([\S\s]*?\)/), function (match0) {
                // init signature
                element.signature = match0
                    .replace((/ *?\/\*[\S\s]*?\*\/ */g), '')
                    .replace((/,/g), ', ')
                    .replace((/\s+/g), ' ');
                return element.signature;
            })
            .replace(
                (/( *?\/\*[\S\s]*?\*\/\n)/),
                '<span class="apidocCodeCommentSpan">$1</span>'
            )
            .replace((/^function \(/), key + ' = function (');
        // init example
        options.exampleList.some(function (example) {
            example.replace(
                new RegExp('((?:\n.*?){8}\\.)(' + key + ')(\\((?:.*?\n){8})'),
                function (match0, match1, match2, match3) {
                    element.example = '...' + trimLeft(
                        options.template === local.templateApidocHtml
                            ?  local.stringHtmlSafe(match1) +
                                '<span class="apidocCodeKeywordSpan">' +
                                local.stringHtmlSafe(match2) +
                                '</span>' +
                                local.stringHtmlSafe(match3)
                            : match0
                    ).trimRight() + '\n...';
                }
            );
            return element.example;
        });
        element.example = element.example || 'n/a';
        return element;
    };
    readExample = function (file) {
    /*
     * this function will read the example from the given file
     */
        try {
            return ('\n\n\n\n\n\n\n\n' +
                local.fs.readFileSync(local.path.resolve(options.dir, file), 'utf8') +
                '\n\n\n\n\n\n\n\n').replace((/\r\n*/g), '\n');
        } catch (errorCaught) {
            return '';
        }
    };
    trimLeft = function (text) {
    /*
     * this function will normalize the whitespace around the text
     */
        var whitespace;
        whitespace = '';
        text.trim().replace((/^ */gm), function (match0) {
            if (!whitespace || match0.length < whitespace.length) {
                whitespace = match0;
            }
        });
        text = text.replace(new RegExp('^' + whitespace, 'gm'), '');
        // enforce 128 character column limit
        text = text.replace((/^.{128}[^\\\n]+/gm), function (match0) {
            return match0.replace((/(.{128}(?:\b|\w+))/g), '$1\n').trimRight();
        });
        r ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.apidocModuleDictAdd"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>apidocModuleDictAdd (options, moduleDict)](#apidoc.element.n_.context.utility2.apidocModuleDictAdd)
- description and source-code
```javascript
apidocModuleDictAdd = function (options, moduleDict) {
<span class="apidocCodeCommentSpan">/*
 * this function will add the modules in moduleDict to options.moduleDict
 */
</span>    var isModule, tmp;
    ['child', 'prototype', 'grandchild', 'prototype'].forEach(function (element) {
        Object.keys(moduleDict).sort().forEach(function (prefix) {
            if (!(/^\w[\w\-.]*?$/).test(prefix)) {
                return;
            }
            Object.keys(moduleDict[prefix]).forEach(function (key) {
                if (!(/^\w[\w\-.]*?$/).test(key)) {
                    return;
                }
                // bug-workaround - buggy electron accessors
                try {
                    tmp = element === 'prototype'
                        ? {
                            module: moduleDict[prefix][key].prototype,
                            name: prefix + '.' + key + '.prototype'
                        }
                        : {
                            module: moduleDict[prefix][key],
                            name: prefix + '.' + key
                        };
                    if (!tmp.module ||
                            !(typeof tmp.module === 'function' ||
                            typeof tmp.module === 'object') ||
                            options.moduleDict[tmp.name] ||
                            options.circularList.indexOf(tmp.module) >= 0) {
                        return;
                    }
                    isModule = [
                        tmp.module,
                        tmp.module.prototype
                    ].some(function (dict) {
                        return Object.keys(dict || {}).some(function (key) {
                            try {
                                return typeof dict[key] === 'function';
                            } catch (ignore) {
                            }
                        });
                    });
                    if (!isModule) {
                        return;
                    }
                    options.circularList.push(tmp.module);
                    options.moduleDict[tmp.name] = tmp.module;
                } catch (ignore) {
                }
            });
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.array_to_hash"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>array_to_hash (e)](#apidoc.element.n_.context.utility2.array_to_hash)
- description and source-code
```javascript
function array_to_hash(e){var t={};for(var n=0
;n<e.length;++n)t[e[n]]=!0;return t}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.assert"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>assert (passed, message)](#apidoc.element.n_.context.utility2.assert)
- description and source-code
```javascript
assert = function (passed, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will throw the error message if passed is falsey
 */
</span>    var error;
    if (passed) {
        return;
    }
    error = message && message.message
        // if message is an error-object, then leave it as is
        ? message
        : new Error(typeof message === 'string'
            // if message is a string, then leave it as is
            ? message
            // else JSON.stringify message
            : JSON.stringify(message));
    throw error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.assertJsonEqual"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>assertJsonEqual (aa, bb)](#apidoc.element.n_.context.utility2.assertJsonEqual)
- description and source-code
```javascript
assertJsonEqual = function (aa, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert
 * utility2.jsonStringifyOrdered(aa) === JSON.stringify(bb)
 */
</span>    aa = local.jsonStringifyOrdered(aa);
    bb = JSON.stringify(bb);
    local.assert(aa === bb, [aa, bb]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.assertJsonNotEqual"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>assertJsonNotEqual (aa, bb)](#apidoc.element.n_.context.utility2.assertJsonNotEqual)
- description and source-code
```javascript
assertJsonNotEqual = function (aa, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert
 * utility2.jsonStringifyOrdered(aa) !== JSON.stringify(bb)
 */
</span>    aa = local.jsonStringifyOrdered(aa);
    bb = JSON.stringify(bb);
    local.assert(aa !== bb, [aa, bb]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ast_add_scope"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_add_scope (e)](#apidoc.element.n_.context.utility2.ast_add_scope)
- description and source-code
```javascript
function ast_add_scope(e){function s(e){t=new Scope(t),t.labels=new Scope;var n=
t.body=e();return n.scope=t,t=t.parent,n}function o(e,n){return t.define(e,n)}function u
(e){t.refs[e]=!0}function a(e,t,n){var i=this[0]=="defun";return[this[0],i?o(e,"defun"
):e,t,s(function(){return i||o(e,"lambda"),MAP(t,function(e){o(e,"arg")}),MAP(n,
r)})]}function f(e){return function(t){MAP(t,function(t){o(t[0],e),t[1]&&u(t[0])
})}}function l(e){e&&(t.labels.refs[e]=!0)}var t=null,n=ast_walker(),r=n.walk,i=
[];return s(function(){function c(e,t){for(t=e.children.length;--t>=0;)c(e.children
[t]);for(t in e.refs)if(HOP(e.refs,t))for(var n=e.has(t),r=e;r;r=r.parent){r.refs
[t]=n;if(r===n)break}}var s=n.with_walkers({"function":a,defun:a,label:function(
e,n){t.labels.define(e)},"break":l,"continue":l,"with":function(e,n){for(var r=t
;r;r=r.parent)r.uses_with=!0},"var":f("var"),"const":f("const"),"try":function(e
,t,n){if(t!=null)return[this[0],MAP(e,r),[o(t[0],"catch"),MAP(t[1],r)],n!=null?MAP
(n,r):null]},name:function(e){e=="eval"&&i.push(t),u(e)}},function(){return r(e)
});return MAP(i,function(e){if(!e.has("eval"))while(e)e.uses_eval=!0,e=e.parent}
),c(t),s})}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ast_lift_variables"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_lift_variables (e)](#apidoc.element.n_.context.utility2.ast_lift_variables)
- description and source-code
```javascript
function ast_lift_variables(e){function i(e,t){var i=r;r=t,e=MAP(e,n);var s=
{},o=MAP(t.names,function(e,n){return e!="var"?MAP.skip:t.references(n)?(s[n]=!0
,[n]):MAP.skip});return o.length>0&&(for_side_effects(["block",e],function(e,t,n
,r){if(e[0]=="assign"&&e[1]===!0&&e[2][0]=="name"&&HOP(s,e[2][1])){for(var i=o.length
;--i>=0;)if(o[i][0]==e[2][1]){o[i][1]&&n(),o[i][1]=e[3],o.push(o.splice(i,1)[0])
;break}var u=t.parent();if(u[0]=="seq"){var a=u[2];a.unshift(0,u.length),u.splice
.apply(u,a)}else u[0]=="stat"?u.splice(0,u.length,"block"):n();r()}n()}),e.unshift
(["var",o])),r=i,e}function s(e){var n=null;for(var r=e.length;--r>=0;){var i=e[
r];if(!i[1])continue;i=["assign",!0,["name",i[0]],i[1]],n==null?n=i:n=["seq",i,n
]}return n==null&&t.parent()[0]!="for"?t.parent()[0]=="for-in"?["name",e[0][0]]:
MAP.skip:["stat",n]}function o(e){return[this[0],i(e,this.scope)]}var t=ast_walker
(),n=t.walk,r;return t.with_walkers({"function":function(e,t,n){for(var r=t.length
;--r>=0&&!n.scope.references(t[r]);)t.pop();return n.scope.references(e)||(e=null
),[this[0],e,t,i(n,n.scope)]},defun:function(e,t,n){if(!r.references(e))return MAP
.skip;for(var s=t.length;--s>=0&&!n.scope.references(t[s]);)t.pop();return[this[0
],e,t,i(n,n.scope)]},"var":s,toplevel:o},function(){return n(ast_add_scope(e))})
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ast_mangle"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_mangle (e, t)](#apidoc.element.n_.context.utility2.ast_mangle)
- description and source-code
```javascript
function ast_mangle(e, t){function s(e,n){return t.mangle?!t.toplevel&&!
i.parent?e:t.except&&member(e,t.except)?e:t.no_functions&&HOP(i.names,e)&&(i.names
[e]=="defun"||i.names[e]=="lambda")?e:i.get_mangled(e,n):e}function o(e){if(t.defines
)return!i.has(e)&&HOP(t.defines,e)?t.defines[e]:null}function u(e,n,o){if(!t.no_functions&&
t.mangle){var u=this[0]=="defun",f;e&&(u?e=s(e):o.scope.references(e)?(f={},!i.uses_eval&&!
i.uses_with?e=f[e]=i.next_mangled():f[e]=e):e=null)}return o=a(o.scope,function(
){return n=MAP(n,function(e){return s(e)}),MAP(o,r)},f),[this[0],e,n,o]}function a
(e,t,n){var r=i;i=e;if(n)for(var o in n)HOP(n,o)&&e.set_mangle(o,n[o]);for(var o in
e.names)HOP(e.names,o)&&s(o,!0);var u=t();return u.scope=e,i=r,u}function f(e){return[
this[0],MAP(e,function(e){return[s(e[0]),r(e[1])]})]}function l(e){if(e)return[this
[0],i.labels.get_mangled(e)]}var n=ast_walker(),r=n.walk,i;return t=defaults(t,{
mangle:!0,toplevel:!1,defines:null,except:null,no_functions:!1}),n.with_walkers(
{"function":u,defun:function(){var e=u.apply(this,arguments);switch(n.parent()[0
]){case"toplevel":case"function":case"defun":return MAP.at_top(e)}return e},label
:function(e,t){return i.labels.refs[e]?[this[0],i.labels.get_mangled(e,!0),r(t)]
:r(t)},"break":l,"continue":l,"var":f,"const":f,name:function(e){return o(e)||[this
[0],s(e)]},"try":function(e,t,n){return[this[0],MAP(e,r),t!=null?[s(t[0]),MAP(t[1
],r)]:null,n!=null?MAP(n,r):null]},toplevel:function(e){var t=this;return a(t.scope
,function(){return[t[0],MAP(e,r)]})},directive:function(){return MAP.at_top(this
)}},function(){return r(ast_add_scope(e))})}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ast_squeeze"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_squeeze (e, t)](#apidoc.element.n_.context.utility2.ast_squeeze)
- description and source-code
```javascript
function ast_squeeze(e, t){return e=squeeze_1(e,t),e=squeeze_2(e,t),e}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.ast_walker"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>ast_walker ()](#apidoc.element.n_.context.utility2.ast_walker)
- description and source-code
```javascript
function ast_walker(){function e(e){return[this[0],MAP(e,function(e){var t=[e[0]
];return e.length>1&&(t[1]=s(e[1])),t})]}function t(e){var t=[this[0]];return e!=
null&&t.push(MAP(e,s)),t}function s(e){if(e==null)return null;try{i.push(e);var t=
e[0],s=r[t];if(s){var o=s.apply(e,e.slice(1));if(o!=null)return o}return s=n[t],
s.apply(e,e.slice(1))}finally{i.pop()}}function o(e){if(e==null)return null;try{
return i.push(e),n[e[0]].apply(e,e.slice(1))}finally{i.pop()}}function u(e,t){var n=
{},i;for(i in e)HOP(e,i)&&(n[i]=r[i],r[i]=e[i]);var s=t();for(i in n)HOP(n,i)&&(
n[i]?r[i]=n[i]:delete r[i]);return s}var n={string:function(e){return[this[0],e]
},num:function(e){return[this[0],e]},name:function(e){return[this[0],e]},toplevel
:function(e){return[this[0],MAP(e,s)]},block:t,splice:t,"var":e,"const":e,"try":
function(e,t,n){return[this[0],MAP(e,s),t!=null?[t[0],MAP(t[1],s)]:null,n!=null?
MAP(n,s):null]},"throw":function(e){return[this[0],s(e)]},"new":function(e,t){return[
this[0],s(e),MAP(t,s)]},"switch":function(e,t){return[this[0],s(e),MAP(t,function(
e){return[e[0]?s(e[0]):null,MAP(e[1],s)]})]},"break":function(e){return[this[0],
e]},"continue":function(e){return[this[0],e]},conditional:function(e,t,n){return[
this[0],s(e),s(t),s(n)]},assign:function(e,t,n){return[this[0],e,s(t),s(n)]},dot
:function(e){return[this[0],s(e)].concat(slice(arguments,1))},call:function(e,t)
{return[this[0],s(e),MAP(t,s)]},"function":function(e,t,n){return[this[0],e,t.slice
(),MAP(n,s)]},"debugger":function(){return[this[0]]},defun:function(e,t,n){return[
this[0],e,t.slice(),MAP(n,s)]},"if":function(e,t,n){return[this[0],s(e),s(t),s(n
)]},"for":function(e,t,n,r){return[this[0],s(e),s(t),s(n),s(r)]},"for-in":function(
e,t,n,r){return[this[0],s(e),s(t),s(n),s(r)]},"while":function(e,t){return[this[0
],s(e),s(t)]},"do":function(e,t){return[this[0],s(e),s(t)]},"return":function(e)
{return[this[0],s(e)]},binary:function(e,t,n){return[this[0],e,s(t),s(n)]},"unary-prefix"
:function(e,t){return[this[0],e,s(t)]},"unary-postfix":function(e,t){return[this
[0],e,s(t)]},sub:function(e,t){return[this[0],s(e),s(t)]},object:function(e){return[
this[0],MAP(e,function(e){return e.length==2?[e[0],s(e[1])]:[e[0],s(e[1]),e[2]]}
)]},regexp:function(e,t){return[this[0],e,t]},array:function(e){return[this[0],MAP
(e,s)]},stat:function(e){return[this[0],s(e)]},seq:function(){return[this[0]].concat
(MAP(slice(arguments),s))},label:function(e,t){return[this[0],e,s(t)]},"with":function(
e,t){return[this[0],s(e),s(t)]},atom:function(e){return[this[0],e]},directive:function(
e){return[this[0],e]}},r={},i=[];return{walk:s,dive:o,with_walkers:u,parent:function(
){return i[i.length-2]},stack:function(){return i}}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64FromBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromBuffer (bff)](#apidoc.element.n_.context.utility2.base64FromBuffer)
- description and source-code
```javascript
base64FromBuffer = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * https://developer.mozilla.org/en-US/Add-ons/Code_snippets/StringView#The_code
 * this function will convert the Uint8Array-bff to base64-encoded-text
 */
</span>    var ii, mod3, text, uint24, uint6ToB64;
    text = '';
    uint24 = 0;
    uint6ToB64 = function (uint6) {
        return uint6 < 26
            ? uint6 + 65
            : uint6 < 52
            ? uint6 + 71
            : uint6 < 62
            ? uint6 - 4
            : uint6 === 62
            ? 43
            : 47;
    };
    for (ii = 0; ii < bff.length; ii += 1) {
        mod3 = ii % 3;
        uint24 |= bff[ii] << (16 >>> mod3 & 24);
        if (mod3 === 2 || bff.length - ii === 1) {
            text += String.fromCharCode(
                uint6ToB64(uint24 >>> 18 & 63),
                uint6ToB64(uint24 >>> 12 & 63),
                uint6ToB64(uint24 >>> 6 & 63),
                uint6ToB64(uint24 & 63)
            );
            uint24 = 0;
        }
    }
    return text.replace(/A(?=A$|$)/g, '=');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64FromHex"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromHex (text)](#apidoc.element.n_.context.utility2.base64FromHex)
- description and source-code
```javascript
base64FromHex = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the hex-text to base64-encoded-text
 */
</span>    var bff, ii;
    bff = [];
    for (ii = 0; ii < text.length; ii += 2) {
        bff.push(parseInt(text[ii] + text[ii + 1], 16));
    }
    return local.base64FromBuffer(bff);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64FromString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64FromString (text)](#apidoc.element.n_.context.utility2.base64FromString)
- description and source-code
```javascript
base64FromString = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the utf8-text to base64-encoded-text
 */
</span>    return local.base64FromBuffer(local.bufferCreate(text));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64ToBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToBuffer (text)](#apidoc.element.n_.context.utility2.base64ToBuffer)
- description and source-code
```javascript
base64ToBuffer = function (text) {
<span class="apidocCodeCommentSpan">/*
 * https://gist.github.com/wang-bin/7332335
 * this function will convert the base64-encoded text to Uint8Array
 */
</span>    var de = new Uint8Array(text.length); //3/4
    var u = 0, q = '', x = '', c;
    var map64 = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/";
    for (var r=0; c=text[x++]; ~c&&(u=q%4?u*64+c:c,q++%4)?de[r++]=(255&u>>(-2*q&6)):0)
        c = map64.indexOf(c);
    return de.subarray(0, r);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64ToHex"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToHex (text)](#apidoc.element.n_.context.utility2.base64ToHex)
- description and source-code
```javascript
base64ToHex = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the base64-encoded-text to hex-text
 */
</span>    var bff, ii;
    bff = local.base64ToBuffer(text);
    text = '';
    for (ii = 0; ii < bff.length; ii += 1) {
        text += (0x100 + bff[ii]).toString(16).slice(-2);
    }
    return text;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.base64ToString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>base64ToString (text)](#apidoc.element.n_.context.utility2.base64ToString)
- description and source-code
```javascript
base64ToString = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the base64-encoded text to utf8-text
 */
</span>    return local.bufferToString(local.base64ToBuffer(text));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.blobRead"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>blobRead (blob, encoding, onError)](#apidoc.element.n_.context.utility2.blobRead)
- description and source-code
```javascript
blobRead = function (blob, encoding, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will read from the blob with the given encoding
 * possible encodings are:
 * - Uint8Array (default)
 * - dataURL
 * - text
 */
</span>    var data, done, reader;
    if (local.modeJs === 'node') {
        switch (encoding) {
        // readAsDataURL
        case 'dataURL':
            data = 'data:' + (blob.type || '') + ';base64,' +
                local.base64FromBuffer(blob.bff);
            break;
        // readAsText
        case 'text':
            data = local.bufferToString(blob.bff);
            break;
        // readAsArrayBuffer
        default:
            data = local.bufferCreate(blob.bff);
        }
        onError(null, data);
        return;
    }
    reader = new local.global.FileReader();
    reader.onabort = reader.onerror = reader.onload = function (event) {
        if (done) {
            return;
        }
        done = true;
        switch (event.type) {
        case 'abort':
        case 'error':
            onError(new Error('blobRead - ' + event.type));
            break;
        case 'load':
            onError(null, reader.result instanceof local.global.ArrayBuffer
                // convert ArrayBuffer to Uint8Array
                ? local.bufferCreate(reader.result)
                : reader.result);
            break;
        }
    };
    switch (encoding) {
    // readAsDataURL
    case 'dataURL':
        reader.readAsDataURL(blob);
        break;
    // readAsText
    case 'text':
        reader.readAsText(blob);
        break;
    // readAsArrayBuffer
    default:
        reader.readAsArrayBuffer(blob);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.browserTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>browserTest (options, onError)](#apidoc.element.n_.context.utility2.browserTest)
- description and source-code
```javascript
browserTest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will spawn an electron process to test options.url
 */
</span>    var done, modeNext, onNext, onParallel, timerTimeout;
    if (typeof local === 'object' && local && local.modeJs === 'node') {
        local.objectSetDefault(options, local.envSanitize(local.env));
        options.timeoutDefault = options.timeoutDefault || local.timeoutDefault;
    }
    modeNext = Number(options.modeNext || 0);
    onNext = function (error, data) {
        modeNext = error instanceof Error
            ? Infinity
            : modeNext + 1;
        switch (modeNext) {
        // run node code
        case 1:
            // init options
            if (!(/^\w+:\/\//).test(options.url)) {
                options.url = local.path.resolve(process.cwd(), options.url);
            }
            options.testName = local.env.MODE_BUILD + '.browser.' +
                encodeURIComponent(local.urlParse(options.url).pathname
                    .replace(
                        '/build..' + local.env.CI_BRANCH + '..' + local.env.CI_HOST,
                        '/build'
                    ));
            local.objectSetDefault(options, {
                fileCoverage: local.env.npm_config_dir_tmp +
                    '/coverage.' + options.testName + '.json',
                fileScreenCapture: (local.env.npm_config_dir_build +
                    '/screenCapture.' + options.testName + '.png')
                    .replace((/%/g), '_')
                    .replace((/_2F\.png$/), '.png'),
                fileTestReport: local.env.npm_config_dir_tmp +
                    '/test-report.' + options.testName + '.json',
                modeBrowserTest: 'test',
                timeExit: Date.now() + options.timeoutDefault,
                timeoutScreenCapture: Number(options.timeoutScreenCapture || 10000)
            }, 1);
            // init timerTimeout
            timerTimeout = local.onTimeout(
                onNext,
                options.timeoutDefault,
                options.testName
            );
            // init file fileElectronHtml
            options.browserTestScript = local.browserTest
                .toString()
                .replace((/<\//g), '<\\/')
                // coverage-hack - un-instrument
                .replace((/\b__cov_.*?\+\+/g), '0');
            options.modeNext = 20;
            options.fileElectronHtml = local.env.npm_config_dir_tmp + '/electron.' +
                Date.now().toString(16) + Math.random().toString(16) + '.html';
            local.fsWriteFileWithMkdirpSync(options.fileElectronHtml, '<style>body {' +
                    'border: 1px solid black;' +
                    'margin: 0;' +
                    'padding: 0;' +
                '}</style>' +
                '<webview id=webview1 preload="' + options.fileElectronHtml +
                '.preload.js" src="' +
                options.url.replace('{{timeExit}}', options.timeExit) +
                '" style="' +
                    'border: none;' +
                    'height: 100%;' +
                    'margin: 0;' +
                    'padding: 0;' +
                    'width: 100%;' +
                '"></webview>' +
                '<script>window.local = {}; (' + options.browserTestScript +
                '(' + JSON.stringify(options) + '))</script>');
            console.error('\nbrowserTest - created electron entry-page ' +
                options.fileElectronHtml + '\n');
            // init file fileElectronHtml.preload.js
            options.modeNext = 30;
            local.fsWriteFileWithMkdirpSync(
                options.fileElectronHtml + '.preload.js',
                '(' + options.browserTestScript + '(' + JSON.stringify(options) +
                    '))'
            );
            // spawn an electron process to test a url
            options.modeNext = 10;
            local.processSpawnWithTimeout('electron', [
                __filename,
                'browserTest',
                '--disable-overlay-scrollbar',
                '--enable-logging'
            ], { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferConcat"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferConcat (bufferList)](#apidoc.element.n_.context.utility2.bufferConcat)
- description and source-code
```javascript
bufferConcat = function (bufferList) {
<span class="apidocCodeCommentSpan">/*
 * this function will emulate node's Buffer.concat for Uint8Array in the browser
 */
</span>    var ii, jj, length, result;
    length = 0;
    bufferList = bufferList
        .filter(function (element) {
            return element || element === 0;
        })
        .map(function (element) {
            // convert number to string
            if (typeof element === 'number') {
                element = String(element);
            }
            // convert non-Uint8Array to Uint8Array
            element = local.bufferCreateIfNotBuffer(element);
            length += element.length;
            return element;
        });
    result = local.bufferCreate(length);
    ii = 0;
    bufferList.forEach(function (element) {
        for (jj = 0; jj < element.length; ii += 1, jj += 1) {
            result[ii] = element[jj];
        }
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferCreate (text)](#apidoc.element.n_.context.utility2.bufferCreate)
- description and source-code
```javascript
bufferCreate = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a Uint8Array from the text,
 * with either 'utf8' (default) or 'base64' encoding
 */
</span>    if (typeof text === 'string') {
        if (local.modeJs === 'node') {
            return new Buffer(text);
        }
        if (local.global.TextEncoder) {
            return new local.global.TextEncoder('utf-8').encode(text);
        }
// bug-workaround - TextEncoder.encode polyfill
/* jslint-ignore-begin */
// utility2-uglifyjs https://github.com/feross/buffer/blob/v4.9.1/index.js#L1670
/* istanbul ignore next */
function utf8ToBytes(e,t){t=t||Infinity;var n,r=e.length,i=null,s=[];for(var o=0
;o<r;++o){n=e.charCodeAt(o);if(n>55295&&n<57344){if(!i){if(n>56319){(t-=3)>-1&&s
.push(239,191,189);continue}if(o+1===r){(t-=3)>-1&&s.push(239,191,189);continue}
i=n;continue}if(n<56320){(t-=3)>-1&&s.push(239,191,189),i=n;continue}n=(i-55296<<10|
n-56320)+65536}else i&&(t-=3)>-1&&s.push(239,191,189);i=null;if(n<128){if((t-=1)<0
)break;s.push(n)}else if(n<2048){if((t-=2)<0)break;s.push(n>>6|192,n&63|128)}else if(
n<65536){if((t-=3)<0)break;s.push(n>>12|224,n>>6&63|128,n&63|128)}else{if(!(n<1114112
))throw new Error("Invalid code point");if((t-=4)<0)break;s.push(n>>18|240,n>>12&63|128
,n>>6&63|128,n&63|128)}}return s}
return new local.global.Uint8Array(utf8ToBytes(text));
/* jslint-ignore-end */
    }
    return new local.global.Uint8Array(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferCreateIfNotBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferCreateIfNotBuffer (text)](#apidoc.element.n_.context.utility2.bufferCreateIfNotBuffer)
- description and source-code
```javascript
bufferCreateIfNotBuffer = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a Uint8Array from the text with the given encoding,
 * if it is not already a Uint8Array
 */
</span>    return text instanceof local.global.Uint8Array
        ? text
        : local.bufferCreate(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferIndexOfSubBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferIndexOfSubBuffer (bff, subBff, fromIndex)](#apidoc.element.n_.context.utility2.bufferIndexOfSubBuffer)
- description and source-code
```javascript
bufferIndexOfSubBuffer = function (bff, subBff, fromIndex) {
<span class="apidocCodeCommentSpan">/*
 * this function will search bff for the indexOf-like position of the subBff
 */
</span>    var ii, jj, kk;
    for (ii = fromIndex || 0; ii < bff.length; ii += 1) {
        for (jj = 0, kk = ii; jj < subBff.length; jj += 1, kk += 1) {
            if (subBff[jj] !== bff[kk]) {
                break;
            }
        }
        if (jj === subBff.length) {
            return kk - jj;
        }
    }
    return subBff.length && -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferRandomBytes"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferRandomBytes (length)](#apidoc.element.n_.context.utility2.bufferRandomBytes)
- description and source-code
```javascript
bufferRandomBytes = function (length) {
<span class="apidocCodeCommentSpan">/*
 * this function will create create a Uint8Array with the given length,
 * filled with random bytes
 */
</span>    var bff, ii;
    bff = new local.global.Uint8Array(length);
    for (ii = 0; ii < bff.length; ii += 1) {
        bff[ii] = Math.random() * 0x100;
    }
    return bff;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferToNodeBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferToNodeBuffer (bff)](#apidoc.element.n_.context.utility2.bufferToNodeBuffer)
- description and source-code
```javascript
bufferToNodeBuffer = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the Uint8Array instance to a node Buffer instance
 */
</span>    if (local.modeJs === 'node' &&
            bff instanceof local.global.Uint8Array && (!Buffer.isBuffer(bff))) {
        Object.setPrototypeOf(bff, Buffer.prototype);
    }
    return bff;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.bufferToString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>bufferToString (bff)](#apidoc.element.n_.context.utility2.bufferToString)
- description and source-code
```javascript
bufferToString = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the Uint8Array bff to a utf8 string
 */
</span>    bff = bff || '';
    if (typeof bff === 'string') {
        return bff;
    }
    bff = local.bufferCreateIfNotBuffer(bff);
    if (local.modeJs === 'node') {
        return new Buffer(bff).toString();
    }
    if (local.global.TextDecoder) {
        return new local.global.TextDecoder('utf-8').decode(bff);
    }
// bug-workaround - TextDecoder.decode polyfill
/* jslint-ignore-begin */
// http://stackoverflow.com/questions/17191945/conversion-between-utf-8-arraybuffer-and-string
function Utf8ArrayToStr(e){var t,n,r,i,s,o;t="",r=e.length,n=0;while(n<r){i=e[n++
];switch(i>>4){case 0:case 1:case 2:case 3:case 4:case 5:case 6:case 7:t+=String
.fromCharCode(i);break;case 12:case 13:s=e[n++],t+=String.fromCharCode((i&31)<<6|
s&63);break;case 14:s=e[n++],o=e[n++],t+=String.fromCharCode((i&15)<<12|(s&63)<<6|
(o&63)<<0)}}return t}
return Utf8ArrayToStr(bff);
/* jslint-ignore-end */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildApidoc"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildApidoc (options, onError)](#apidoc.element.n_.context.utility2.buildApidoc)
- description and source-code
```javascript
buildApidoc = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the apidoc
 */
</span>    // optimization - do not run if $npm_config_mode_coverage = all
    if (local.env.npm_config_mode_coverage === 'all') {
        onError();
        return;
    }
    local.objectSetDefault(options, { blacklistDict: local });
    // create apidoc.html
    local.fsWriteFileWithMkdirpSync(
        local.env.npm_config_dir_build + '/apidoc.html',
        local.apidocCreate(options)
    );
    console.error('created apidoc file://' + local.env.npm_config_dir_build +
        '/apidoc.html\n');
    local.browserTest({
        modeBrowserTest: 'screenCapture',
        url: local.env.npm_config_dir_build + '/apidoc.html'
    }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildApp"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildApp (options, onError)](#apidoc.element.n_.context.utility2.buildApp)
- description and source-code
```javascript
buildApp = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the app
 */
</span>    var writeFileSync;
    local.fsRmrSync(local.env.npm_config_dir_build + '/app');
    local.onParallelList({ list: options.concat([{
        file: '/assets.' + local.env.npm_package_nameAlias + '.js',
        url: '/assets.' + local.env.npm_package_nameAlias + '.js'
    }, {
        file: '/assets.' + local.env.npm_package_nameAlias + '.rollup.js',
        url: '/assets.' + local.env.npm_package_nameAlias + '.rollup.js'
    }, {
        file: '/assets.app.js',
        url: '/assets.app.js'
    }, {
        file: '/assets.example.js',
        url: '/assets.example.js'
    }, {
        file: '/assets.test.js',
        url: '/assets.test.js'
    }, {
        file: '/assets.utility2.rollup.js',
        url: '/assets.utility2.rollup.js'
    }, {
        file: '/index.html',
        url: '/index.html'
    }, {
        file: '/jsonp.utility2._stateInit',
        url: '/jsonp.utility2._stateInit?callback=window.utility2._stateInit'
    }]) }, function (options, onParallel) {
        options = options.element;
        onParallel.counter += 1;
        local.ajax(options, function (error, xhr) {
            // validate no error occurred
            local.assert(!error, error);
            // jslint file
            local.jslintAndPrintConditional(xhr.responseText, options.file);
            // validate no error occurred
            local.assert(!local.jslint.errorText, local.jslint.errorText);
            local.fsWriteFileWithMkdirpSync(
                local.env.npm_config_dir_build + '/app' + options.file,
                new Buffer(xhr.response)
            );
            onParallel();
        });
    }, function (error) {
        // validate no error occurred
        local.assert(!error, error);
        // coverage-hack
        writeFileSync = local.fs.writeFileSync;
        local.nop(local.global.__coverage__ && (function () {
            writeFileSync = local.nop;
        }()));
        writeFileSync(
            'assets.' + local.env.npm_package_nameAlias + '.rollup.js',
            local.assetsDict['/assets.' + local.env.npm_package_nameAlias +
                '.rollup.js']
        );
        // test standalone assets.app.js
        local.fs.writeFileSync('tmp/assets.app.js', local.assetsDict['/assets.app.js']);
        local.processSpawnWithTimeout(process.argv[0], ['assets.app.js'], {
            cwd: 'tmp',
            env: {
                PORT: (Math.random() * 0x10000) | 0x8000,
                npm_config_timeout_exit: 5000
            },
            stdio: ['ignore', 1, 2]
        })
            .once('error', onError)
            .once('exit', function (exitCode) {
                // validate exitCode
                local.assert(!exitCode, exitCode);
                onError();
            });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildLib"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildLib (options, onError)](#apidoc.element.n_.context.utility2.buildLib)
- description and source-code
```javascript
buildLib = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the lib
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile(
            'lib.' + local.env.npm_package_nameAlias + '.js',
            'utf8'
        ),
        dataTo: local.templateRenderJslintLite(
            local.assetsDict['/assets.lib.template.js'],
            {}
        )
    });
    // search-and-replace - customize dataTo
    [
        // customize body before istanbul
        (/[\S\s]*?^\/\* istanbul instrument in package /m),
        // customize body after init exports
        (/\n {12}module.exports.module = module;\n[\S\s]*?$/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    options.customize();
    // save lib.xxx.js
    local.fs.writeFileSync(
        'lib.' + local.env.npm_package_nameAlias + '.js',
        options.dataTo
    );
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildNpmdoc"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildNpmdoc (options, onError)](#apidoc.element.n_.context.utility2.buildNpmdoc)
- description and source-code
```javascript
buildNpmdoc = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the npmdoc
 */
</span>    var done, onError2, onParallel, packageJson;
    // ensure exit after 5 minutes
    setTimeout(process.exit, 5 * 60 * 1000);
    onError2 = function (error) {
        local.onErrorDefault(error);
        if (done) {
            return;
        }
        done = true;
        // try to recover from error
        setTimeout(onError, error && local.timeoutDefault);
    };
    // try to salvage uncaughtException
    process.on('uncaughtException', onError2);
    onParallel = local.utility2.onParallel(onError2);
    onParallel.counter += 1;
    // build package.json
    packageJson = JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    local.objectSetDefault(packageJson, local.objectLiteralize({
        devDependencies: {
            '$[]': [local.env.npm_package_buildNpmdoc, '*']
        },
        repository: {
            type: 'git',
            url: 'https://github.com/npmdoc/node-npmdoc-' +
                local.env.npm_package_buildNpmdoc + '.git'
        }
    }), 2);
    local.objectSetOverride(packageJson, local.objectLiteralize({
        keywords: ['documentation', local.env.npm_package_buildNpmdoc]
    }), 2);
    onParallel.counter += 1;
    local.buildReadme({
        dataFrom: '\n# package.json\n'''json\n' +
            JSON.stringify(packageJson) + '\n'''\n'
    }, onParallel);
    packageJson = JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    // build apidoc.html
    onParallel.counter += 1;
    local.buildApidoc({
        dir: local.env.npm_package_buildNpmdoc,
        modulePathList: options.modulePathList
    }, onParallel);
    // build README.md
    options = { modulePathList: options.modulePathList };
    options.readme = local.apidocCreate({
        dir: local.env.npm_package_buildNpmdoc,
/* jslint-ignore-begin */
header: '\
# api documentation for \
 \
n_ (v1.4.4) \
 \
[![npm package](https://img.shields.io/npm/v/npmdoc-n_.svg?style=flat-square)](https://www.npmjs.org/package
/npmdoc-n_)\
[![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-n_.svg)](https://travis-ci.org
/npmdoc/node-npmdoc-n_)\
\n\
#### lodash REPL \
\n\
\n\
[![NPM](https://nodei.co/npm/n_.png?downloads=true)](https://www.npmjs.com/package/n_)\
\n\
\n\
[![apidoc](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode
-npmdoc-n__2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-n_/
build/apidoc.html)\
\n\
\n\
![npmPackageListing](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageListing.svg) \
\n\
\n\
![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageDependencyTree
.svg)\
\n\
\n\
\n\
\n\
# package.json \
\n\
\n\
'''json \
\n\
\n\
{
    "author": {
        "name": "Boris Diakur",
        "email": "contact@borisdiakur.com",
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
            "email": "contact@borisdiakur.com",
            "url": "https://github.com/borisdiakur"
        },
        {
            "name": "John-David Dalton",
            "email": "john.david.dalton@gmail.com",
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
            "name": "borisdiakur",
            "email": "contact@borisdiakur.com"
        },
        {
            "name": "jdalton",
            "email": "john.david.dalton@gmail.com"
        }
    ],
    "name": "n_",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
} \
\n\
''' \
\n\
',
/* jslint-ignore-end */
        modulePathList: options.modulePathList,
        template: local.apidoc.templateApidocMd
    });
    local.fs.writeFileSync('README.md', options.readme);
    // re-build package.json
    packageJson.description = (/\w.*/).exec(options.readme)[0]
        .replace((/ {2,}/g), ' ')
        .trim();
    local.fs.writeFileSync(
        'package.json',
        local.jsonStringifyOrdered(packageJson, null, 4) + '\n'
    );
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildReadme"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildReadme (options, onError)](#apidoc.element.n_.context.utility2.buildReadme)
- description and source-code
```javascript
buildReadme = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the readme in jslint-lite style
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile('README.md', 'utf8')
    });
    // init package.json
    options.rgx = (/\n# package.json\n'''json\n([\S\s]*?)\n'''\n/);
    options.dataFrom.replace(options.rgx, function (match0, match1) {
        options.packageJson = JSON.parse(match1);
        options.packageJson.description = options.dataFrom.split('\n')[1];
        local.objectSetDefault(options.packageJson, {
            nameAlias: options.packageJson.name.replace((/\W/g), '_'),
            nameOriginal: options.packageJson.name
        });
        local.objectSetDefault(
            options.packageJson,
            JSON.parse(local.templateRenderJslintLite(
                options.rgx.exec(local.assetsDict['/assets.readme.template.md'])[1],
                options
            )),
            2
        );
        // avoid npm-installing self
        delete options.packageJson.devDependencies[options.packageJson.name];
        // save package.json
        local.fs.writeFileSync(
            'package.json',
            local.jsonStringifyOrdered(options.packageJson, null, 4) + '\n'
        );
        // update dataTo
        options.dataTo = local.templateRenderJslintLite(
            local.assetsDict['/assets.readme.template.md'],
            options
        );
        options.dataTo = options.dataTo.replace(
            options.rgx,
            match0.replace(
                match1,
                local.jsonStringifyOrdered(options.packageJson, null, 4)
            )
        );
    });
    // search-and-replace - customize dataTo
    [
        // customize header
        (/.*?\n.*?\n/),
        // customize todo
        (/\n#### todo\n[\S\s]*?\n\n\n\n/),
        // customize quickstart-header
        (/\n'''javascript\n\/\*\nexample\.js\n\n[^']*?\n/),
        (/\n {8}\$ npm install [^']*? &&/),
        (/\n {12}: global;\n[^']*?\n {8}local\.global\.local = local;\n/),
        (/\n {8}local\.global\.local = local;\n[^']*?\n {4}\/\/ post-init\n/),
        new RegExp('\\n {8}local\\.testRunBrowser = function \\(event\\) \\{\\n' +
            '[^']*?^ {12}if \\(!event \\|\\| \\(event &&\\n', 'm'),
        (/\n {12}\/\/ custom-case\n[^']*?\n {12}\}\n/),
        // customize quickstart-html-style
        (/\n<\/style>\\n\\\n<style>\\n\\\n[^']*?\\n\\\n<\/style>\\n\\\n/),
        // customize quickstart-html-body
        (/\nutility2-comment -->(?:\\n\\\n){4}[^']*?^<!-- utility2-comment\\n\\\n/m),
        // customize build-script
        (/\n# internal build-script\n[\S\s]*?^- build_ci\.sh\n/m),
        (/\nshBuildCiPost\(\) \{\(set -e\n[^']*?\n\)\}\n/),
        (/\nshBuildCiPre\(\) \{\(set -e\n[^']*?\n\)\}\n/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    // customize comment
    options.dataFrom.replace(
        (/^( *?)(?:#!! |#\/\/ |\/\/!!)(.*?)$/gm),
        function (match0, match1, match2) {
            options.dataTo = options.dataTo.replace(match1 + match2, match0);
        }
    );
    options.customize();
    // save README.md
    local.fs.writeFileSync('README.md', options.dataTo);
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.buildTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>buildTest (options, onError)](#apidoc.element.n_.context.utility2.buildTest)
- description and source-code
```javascript
buildTest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the test
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile('test.js', 'utf8'),
        dataTo: local.templateRenderJslintLite(
            local.assetsDict['/assets.test.template.js'],
            {}
        )
    });
    // search-and-replace - customize dataTo
    [
        // customize js\-env code
        new RegExp('\\n {4}\\/\\/ run shared js\\-env code - pre-init\\n[\\S\\s]*?' +
            '^ {4}\\(function \\(\\) \\{\\n', 'm'),
        (/\n {8}local.global.local = local;\n[\S\s]*?^ {4}\}\(\)\);\n/m),
        (/\n {4}\/\/ run shared js\-env code - function\n[\S\s]*?\n {4}\}\(\)\);\n/),
        (/\n {4}\/\/ run browser js\-env code - function\n[\S\s]*?\n {8}break;\n/),
        (/\n {4}\/\/ run node js\-env code - function\n[\S\s]*?\n {8}break;\n/),
        new RegExp('\\n {4}\\/\\/ run browser js\\-env code - post-init\\n[\\S\\s]*?' +
            '^ {4}case \'browser\':\n', 'm'),
        (/\n {4}\/\/ run shared js\-env code - post-init\n[\S\s]*?\n {4}\}\(\)\);\n/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    options.customize();
    // save test.js
    local.fs.writeFileSync('test.js', options.dataTo);
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.cliRunIstanbul"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>cliRunIstanbul (options)](#apidoc.element.n_.context.utility2.cliRunIstanbul)
- description and source-code
```javascript
cliRunIstanbul = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the cli
 */
</span>    var tmp;
    if ((module !== local.require.main || local.global.utility2_rollup) &&
            !(options && options.runMain)) {
        return;
    }
    switch (process.argv[2]) {
    // transparently adds coverage information to a node command
    case 'cover':
        try {
            tmp = JSON.parse(local._fs.readFileSync('package.json', 'utf8'));
            process.env.npm_package_nameAlias = process.env.npm_package_nameAlias ||
                tmp.nameAlias ||
                tmp.name.replace((/-/g), '_');
        } catch (ignore) {
        }
        process.env.npm_config_mode_coverage = process.env.npm_config_mode_coverage ||
            process.env.npm_package_nameAlias ||
            'all';
        // add coverage hook to require
        local._moduleExtensionsJs = local.module._extensions['.js'];
        local.module._extensions['.js'] = function (module, file) {
            if (typeof file === 'string' &&
                    file.indexOf(process.cwd()) === 0 &&
                    file.indexOf(process.cwd() + '/node_modules/') !== 0) {
                module._compile(local.instrumentInPackage(
                    local._fs.readFileSync(file, 'utf8'),
                    file
                ), file);
                return;
            }
            local._moduleExtensionsJs(module, file);
        };
        // init process.argv
        process.argv.splice(1, 2);
        process.argv[1] = local.path.resolve(process.cwd(), process.argv[1]);
        console.log('\ncovering $ ' + process.argv.join(' '));
        // create coverage on exit
        process.on('exit', function () {
            local.coverageReportCreate({ coverage: local.global.__coverage__ });
        });
        // re-run cli
        local.module.runMain();
        break;
    // instrument a file and print result to stdout
    case 'instrument':
        process.argv[3] = local.path.resolve(process.cwd(), process.argv[3]);
        process.stdout.write(local.instrumentSync(
            local._fs.readFileSync(process.argv[3], 'utf8'),
            process.argv[3]
        ));
        break;
    // cover a node command only when npm_config_mode_coverage is set
    case 'test':
        if (process.env.npm_config_mode_coverage) {
            process.argv[2] = 'cover';
            // re-run cli
            local.cliRunIstanbul(options);
            return;
        }
        // init process.argv
        process.argv.splice(1, 2);
        process.argv[1] = local.path.resolve(process.cwd(), process.argv[1]);
        // re-run cli
        local.module.runMain();
        break;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentDelete"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentDelete (options, onError)](#apidoc.element.n_.context.utility2.contentDelete)
- description and source-code
```javascript
contentDelete = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will delete the github file
 * https://developer.github.com/v3/repos/contents/#delete-a-file
 */
</span>    options = { message: options.message, url: options.url };
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            // get sha
            local.contentRequest({ method: 'GET', url: options.url }, options.onNext);
            break;
        case 2:
            // delete file with sha
            if (!error && data.sha) {
                local.contentRequest({
                    message: options.message,
                    method: 'DELETE',
                    sha: data.sha,
                    url: options.url
                }, options.onNext);
                return;
            }
            // delete tree
            local.onParallelList({ list: data }, function (data, onParallel) {
                onParallel.counter += 1;
                // recurse
                local.contentDelete({
                    message: options.message,
                    url: data.element.url
                }, onParallel);
            }, options.onNext);
            break;
        default:
            onError();
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentGet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentGet (options, onError)](#apidoc.element.n_.context.utility2.contentGet)
- description and source-code
```javascript
contentGet = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the github file
 * https://developer.github.com/v3/repos/contents/#get-contents
 */
</span>    options = { url: options.url };
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            local.contentRequest({ method: 'GET', url: options.url }, options.onNext);
            break;
        case 2:
            options.onNext(null, new Buffer(data.content, 'base64'));
            break;
        default:
            onError(error, !error && data);
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentPut"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentPut (options, onError)](#apidoc.element.n_.context.utility2.contentPut)
- description and source-code
```javascript
contentPut = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will put options.content into the github file
 * https://developer.github.com/v3/repos/contents/#update-a-file
 */
</span>    options = {
        content: options.content,
        message: options.message,
        modeErrorIgnore: true,
        url: options.url
    };
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            // get sha
            local.contentRequest({ method: 'GET', url: options.url }, options.onNext);
            break;
        case 2:
            // put file with sha
            local.contentRequest({
                content: options.content,
                message: options.message,
                method: 'PUT',
                sha: data.sha,
                url: options.url
            }, options.onNext);
            break;
        default:
            onError(error);
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentPutFile"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentPutFile (options, onError)](#apidoc.element.n_.context.utility2.contentPutFile)
- description and source-code
```javascript
contentPutFile = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will put options.file into the github file
 * https://developer.github.com/v3/repos/contents/#update-a-file
 */
</span>    options = { file: options.file, message: options.message, url: options.url };
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            // get file from url
            if ((/^(?:http|https):\/\//).test(options.file)) {
                local.httpRequest({
                    method: 'GET',
                    url: options.file
                }, function (error, response) {
                    options.onNext(error, response && response.data);
                });
                return;
            }
            // get file
            local.fs.readFile(
                local.path.resolve(process.cwd(), options.file),
                options.onNext
            );
            break;
        case 2:
            local.contentPut({
                content: data,
                message: options.message,
                // resolve file in url
                url: (/\/$/).test(options.url)
                    ? options.url + local.path.basename(options.file)
                    : options.url
            }, options.onNext);
            break;
        default:
            onError(error);
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentRequest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentRequest (options, onError)](#apidoc.element.n_.context.utility2.contentRequest)
- description and source-code
```javascript
contentRequest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will request the content from github
 */
</span>    // init options
    options = {
        chunkList: [],
        content: options.content,
        headers: {
            // github oauth authentication
            Authorization: 'token ' + process.env.GITHUB_TOKEN,
            // bug-workaround - github api requires user-agent header
            'User-Agent': 'undefined'
        },
        message: options.message,
        method: options.method,
        responseJson: {},
        sha: options.sha,
        url: options.url
    };
    options.url = options.url
/* jslint-ignore-begin */
// parse https://github.com/:owner/:repo/blob/:branch/:path
.replace(
    (/^https:\/\/github.com\/([^\/]+?\/[^\/]+?)\/blob\/([^\/]+?)\/(.+)/),
    'https://api.github.com/repos/$1/contents/$3?branch=$2'
)
// parse https://github.com/:owner/:repo/tree/:branch/:path
.replace(
    (/^https:\/\/github.com\/([^\/]+?\/[^\/]+?)\/tree\/([^\/]+?)\/(.+)/),
    'https://api.github.com/repos/$1/contents/$3?branch=$2'
)
// parse https://raw.githubusercontent.com/:owner/:repo/:branch/:path
.replace(
(/^https:\/\/raw.githubusercontent.com\/([^\/]+?\/[^\/]+?)\/([^\/]+?)\/(.+)/),
    'https://api.github.com/repos/$1/contents/$3?branch=$2'
)
// parse https://:owner.github.io/:repo/:path
.replace(
    (/^https:\/\/([^\.]+?)\.github\.io\/([^\/]+?)\/(.+)/),
    'https://api.github.com/repos/$1/$2/contents/$3?branch=gh-pages'
)
/* jslint-ignore-end */
        .replace((/\?branch=(.*)/), function (match0, match1) {
            options.branch = match1;
            if (options.method === 'GET') {
                match0 = match0.replace('branch', 'ref');
            }
            return match0;
        });
    if (options.url.indexOf('https://api.github.com/repos/') !== 0) {
        options.onError2(new Error('invalid url ' + options.url));
        return;
    }
    if (options.method !== 'GET') {
        options.message = options.message ||
            '[ci skip] ' + options.method + ' file ' + options.url
            .replace((/\?.*/), '');
        options.url += '&message=' + encodeURIComponent(options.message);
        if (options.sha) {
            options.url += '&sha=' + options.sha;
        }
        options.data = JSON.stringify({
            branch: options.branch,
            content: new Buffer(options.content || '').toString('base64'),
            message: options.message,
            sha: options.sha
        });
    }
    local.httpRequest(options, function (error, response) {
        try {
            options.responseJson = JSON.parse(response.data.toString());
        } catch (ignore) {
        }
        onError(error, options.responseJson);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentTouch"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentTouch (options, onError)](#apidoc.element.n_.context.utility2.contentTouch)
- description and source-code
```javascript
contentTouch = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will touch options.url
 * https://developer.github.com/v3/repos/contents/#update-a-file
 */
</span>    options = {
        message: options.message,
        modeErrorIgnore: true,
        url: options.url
    };
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            // get sha
            local.contentRequest({ method: 'GET', url: options.url }, options.onNext);
            break;
        case 2:
            // put file with sha
            local.contentRequest({
                content: new Buffer(data.content || '', 'base64'),
                message: options.message,
                method: 'PUT',
                sha: data.sha,
                url: options.url
            }, options.onNext);
            break;
        default:
            onError(error);
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.contentTouchList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>contentTouchList (options, onError)](#apidoc.element.n_.context.utility2.contentTouchList)
- description and source-code
```javascript
contentTouchList = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will touch options.urlList in parallel
 * https://developer.github.com/v3/repos/contents/#update-a-file
 */
</span>    local.onParallelList({ list: options.urlList }, function (data, onParallel) {
        onParallel.counter += 1;
        local.contentTouch({
            message: options.message,
            modeErrorIgnore: true,
            url: data.element
        }, onParallel);
    }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.cookieDict"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieDict ()](#apidoc.element.n_.context.utility2.cookieDict)
- description and source-code
```javascript
cookieDict = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will return a dict of all cookies
 */
</span>    var result;
    result = {};
    document.cookie.replace((/(\w+)=([^;]*)/g), function (match0, match1, match2) {
        // jslint-hack
        local.nop(match0);
        result[match1] = match2;
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.cookieRemove"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieRemove (name)](#apidoc.element.n_.context.utility2.cookieRemove)
- description and source-code
```javascript
cookieRemove = function (name) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the cookie with the given name
 */
</span>    document.cookie = name + '=; expires=Thu, 01 Jan 1970 00:00:00 GMT';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.cookieRemoveAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieRemoveAll ()](#apidoc.element.n_.context.utility2.cookieRemoveAll)
- description and source-code
```javascript
cookieRemoveAll = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will remove all cookies
 */
</span>    document.cookie.replace((/(\w+)=/g), function (match0, match1) {
        // jslint-hack
        local.nop(match0);
        document.cookie = match1 + '=; expires=Thu, 01 Jan 1970 00:00:00 GMT';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.cookieSet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>cookieSet (name, value, expiresOffset)](#apidoc.element.n_.context.utility2.cookieSet)
- description and source-code
```javascript
cookieSet = function (name, value, expiresOffset) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the cookie with the given name, value,
 * and expiresOffset (in ms)
 */
</span>    var tmp;
    tmp = name + '=' + value + '; expires=' +
        new Date(Date.now() + expiresOffset).toUTCString();
    document.cookie = tmp;
    return tmp;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.coverageMerge"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>coverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2.coverageMerge)
- description and source-code
```javascript
coverageMerge = function (coverage1, coverage2) {
<span class="apidocCodeCommentSpan">/*
 * this function will merge coverage2 into coverage1
 */
</span>    var dict1, dict2;
    coverage1 = coverage1 || {};
    coverage2 = coverage2 || {};
    Object.keys(coverage2).forEach(function (file) {
        if (!coverage2[file]) {
            return;
        }
        // if file is undefined in coverage1, then add it
        if (!coverage1[file]) {
            coverage1[file] = coverage2[file];
            return;
        }
        // merge file from coverage2 into coverage1
        ['b', 'f', 's'].forEach(function (key) {
            dict1 = coverage1[file][key];
            dict2 = coverage2[file][key];
            switch (key) {
            // increment coverage for branch lines
            case 'b':
                Object.keys(dict2).forEach(function (key) {
                    dict2[key].forEach(function (count, ii) {
                        dict1[key][ii] += count;
                    });
                });
                break;
            // increment coverage for function and statement lines
            case 'f':
            case 's':
                Object.keys(dict2).forEach(function (key) {
                    dict1[key] += dict2[key];
                });
                break;
            }
        });
    });
    return coverage1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.coverageReportCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>coverageReportCreate ()](#apidoc.element.n_.context.utility2.coverageReportCreate)
- description and source-code
```javascript
coverageReportCreate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. print coverage in text-format to stdout
 * 2. write coverage in html-format to filesystem
 * 3. return coverage in html-format as single document
 */
</span>    var options;
    /* istanbul ignore next */
    if (!local.global.__coverage__) {
        return '';
    }
    options = {};
    options.dir = process.cwd() + '/tmp/build/coverage.html';
    // merge previous coverage
    if (local.modeJs === 'node' && process.env.npm_config_mode_coverage_merge) {
        console.log('merging file://' + options.dir + '/coverage.json to coverage');
        try {
            local.coverageMerge(
                local.global.__coverage__,
                JSON.parse(
                    local._fs.readFileSync(options.dir + '/coverage.json', 'utf8')
                )
            );
        } catch (ignore) {
        }
        try {
            options.coverageCodeDict = JSON.parse(local._fs.readFileSync(
                options.dir + '/coverage.code-dict.json',
                'utf8'
            ));
            Object.keys(options.coverageCodeDict).forEach(function (key) {
                local.global.__coverageCodeDict__[key] =
                    local.global.__coverageCodeDict__[key] ||
                    options.coverageCodeDict[key];
            });
        } catch (ignore) {
        }
    }
    // init writer
    local.coverageReportHtml = '';
    local.coverageReportHtml += '<div class="coverageReportDiv">\n' +
        '<h1>coverage-report</h1>\n' +
        '<div ' +
        'style="background: #fff; border: 1px solid #000; margin 0; padding: 0;">\n';
    local.writerData = '';
    options.sourceStore = {};
    options.writer = local.writer;
    // 1. print coverage in text-format to stdout
    new local.TextReport(options).writeReport(local.collector);
    // 2. write coverage in html-format to filesystem
    new local.HtmlReport(options).writeReport(local.collector);
    local.writer.writeFile('', local.nop);
    // write coverage.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.json',
        JSON.stringify(local.global.__coverage__)
    );
    // write coverage.code-dict.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.code-dict.json',
        JSON.stringify(local.global.__coverageCodeDict__)
    );
    // write coverage.badge.svg
    options.pct = local.coverageReportSummary.root.metrics.lines.pct;
    local.fsWriteFileWithMkdirpSync2(
        local.path.dirname(options.dir) + '/coverage.badge.svg',
        local.templateCoverageBadgeSvg
            // edit coverage badge percent
            .replace((/100.0/g), options.pct)
            // edit coverage badge color
            .replace(
                (/0d0/g),
                ('0' + Math.round((100 - options.pct) * 2.21).toString(16)).slice(-2) +
                    ('0' + Math.round(options.pct * 2.21).toString(16)).slice(-2) + '00'
            )
    );
    console.log('created coverage file://' + options.dir + '/index.html');
    // 3. return coverage in html-format as a single document
    local.coverageReportHtml += '</div>\n</div>\n';
    // write coverage.rollup.html
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.rollup.html',
        local.coverageReportHtml
    );
    return local.coverageReportHtml;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.curry"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>curry (e)](#apidoc.element.n_.context.utility2.curry)
- description and source-code
```javascript
function curry(e){var t=
slice(arguments,1);return function(){return e.apply(this,t.concat(slice(arguments
)))}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbCrudRemoveAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbCrudRemoveAll (onError)](#apidoc.element.n_.context.utility2.dbCrudRemoveAll)
- description and source-code
```javascript
dbCrudRemoveAll = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove all dbRow's from the db
 */
</span>    var onParallel;
    onParallel = local.onParallel(function (error) {
        local.setTimeoutOnError(onError, error);
    });
    onParallel.counter += 1;
    Object.keys(local.dbTableDict).forEach(function (key) {
        onParallel.counter += 1;
        local.dbTableDict[key].crudRemoveAll(onParallel);
    });
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbDrop"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbDrop (onError)](#apidoc.element.n_.context.utility2.dbDrop)
- description and source-code
```javascript
dbDrop = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will drop the db
 */
</span>    var onParallel;
    onParallel = local.onParallel(function (error) {
        local.setTimeoutOnError(onError, error);
    });
    onParallel.counter += 1;
    onParallel.counter += 1;
    local.storageClear(onParallel);
    Object.keys(local.dbTableDict).forEach(function (key) {
        onParallel.counter += 1;
        local.dbTableDict[key].drop(onParallel);
    });
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbExport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbExport (onError)](#apidoc.element.n_.context.utility2.dbExport)
- description and source-code
```javascript
dbExport = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will export the db as serialized text
 */
</span>    var result;
    result = '';
    Object.keys(local.dbTableDict).forEach(function (key) {
        result += local.dbTableDict[key].export();
        result += '\n\n';
    });
    return local.setTimeoutOnError(onError, null, result.trim());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbFieldRandomCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbFieldRandomCreate (options)](#apidoc.element.n_.context.utility2.dbFieldRandomCreate)
- description and source-code
```javascript
dbFieldRandomCreate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random dbField from options.propDef
 */
</span>    var ii, max, min, propDef, tmp;
    propDef = options.propDef;
    if (propDef.readOnly) {
        return;
    }
    if (propDef.enum) {
        tmp = options.modeNotRandom
            ? propDef.enum[0]
            : local.listGetElementRandom(propDef.enum);
        return propDef.type === 'array'
            ? [tmp]
            : tmp;
    }
    // http://json-schema.org/latest/json-schema-validation.html#anchor13
    // 5.1.  Validation keywords for numeric instances (number and integer)
    max = isFinite(propDef.maximum)
        ? propDef.maximum
        : 999;
    min = isFinite(propDef.maximum)
        ? propDef.minimum
        : 0;
    switch (propDef.type) {
    case 'array':
        tmp = [];
        // http://json-schema.org/latest/json-schema-validation.html#anchor36
        // 5.3.  Validation keywords for arrays
        for (ii = 0; ii < (propDef.minItems || 0); ii += 1) {
            tmp.push(null);
        }
        break;
    case 'boolean':
        tmp = options.modeNotRandom
            ? false
            : Math.random() <= 0.5
            ? false
            : true;
        break;
    case 'integer':
        if (propDef.exclusiveMaximum) {
            max -= 1;
        }
        if (propDef.exclusiveMinimum) {
            min += 1;
        }
        min = Math.min(min, max);
        tmp = options.modeNotRandom
            ? 0
            : Math.random();
        tmp = Math.floor(min + tmp * (max - min));
        break;
    case 'object':
        tmp = {};
        // http://json-schema.org/latest/json-schema-validation.html#anchor53
        // 5.4.  Validation keywords for objects
        for (ii = 0; ii < (propDef.minProperties || 0); ii += 1) {
            tmp['property' + ii] = null;
        }
        break;
    case 'number':
        if (propDef.exclusiveMinimum) {
            min = min < 0
                ? min * 0.99999
                : min * 1.00001 + 0.00001;
        }
        if (propDef.exclusiveMaximum) {
            max = max > 0
                ? max * 0.99999
                : max * 1.00001 - 0.00001;
        }
        min = Math.min(min, max);
        tmp = options.modeNotRandom
            ? 0
            : Math.random();
        tmp = min + tmp * (max - min);
        break;
    case 'string':
        tmp = options.modeNotRandom
            ? 'abcd1234'
            : ((1 + Math.random()) * 0x10000000000000).toString(36).slice(1);
        switch (propDef.format) {
        case 'byte':
            tmp = local.base64FromString(tmp);
            break;
        case 'date':
        case 'date-time':
            tmp = new Date().toISOString();
            break;
        case 'email':
            tmp = tmp + '@random.com';
            break;
        case 'json':
            tmp = JSON.stringify({ random: tmp });
            break;
        case 'phone':
            tmp = options.modeNotRandom
                ? '+123 (1234) 1234-1234'
                : '+' + Math.random().toString().slice(-3) +
                    ' (' + Math.random().toString().slice(-4) + ') ' +
                    Math.random().toString().slice(-4) + '-' +
                    Math.random().toString().slice(-4);
            break;
        }
        // http://json-schema.org/latest/json-schema-validation.html#anchor25
        // 5.2.  Validation keywords for strings
        while (tmp.length < (propDef.minLength || 0)) {
            tmp += tmp;
        }
        tmp = tmp.slice(0, propDef.maxLength || Infinity);
        break;
    }
    // http://json-schema.org/latest/json-schema-validation.html#anchor13
    // 5.1.  Validation keywords for numeric instances (number and integer)
    if (propDef.multipleOf) {
        tmp = propDef.multipleOf * Math.floor(tmp / propDef.multipleOf);
        if (tmp < min) {
            tmp += propDef.multipleOf;
        }
    }
    return tmp;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbImport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbImport (text, onError)](#apidoc.element.n_.context.utility2.dbImport)
- description and source-code
```javascript
dbImport = function (text, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will import the serialized text into the db
 */
</span>    var dbTable;
    local.modeImport = true;
    setTimeout(function () {
        local.modeImport = null;
    });
    text.replace((/^(\w\S*?) (\S+?) (\S.+?)$/gm), function (
        match0,
        match1,
        match2,
        match3
    ) {
        // jslint-hack
        local.nop(match0);
        switch (match2) {
        case 'dbRowSet':
            dbTable = local.dbTableCreateOne({ isLoaded: true, name: match1 });
            dbTable.crudSetOneById(JSON.parse(match3));
            break;
        case 'idIndexCreate':
            dbTable = local.dbTableCreateOne({ isLoaded: true, name: match1 });
            dbTable.idIndexCreate(JSON.parse(match3));
            break;
        case 'sortDefault':
            dbTable = local.dbTableCreateOne({ isLoaded: true, name: match1 });
            break;
        case 'ttlSet':
            dbTable = local.dbTableCreateOne({ isLoaded: true, name: match1 });
            dbTable.ttlSet(JSON.parse(match3));
            break;
        default:
            local.onErrorDefault(new Error('dbImport - invalid operation - ' + match0));
        }
    });
    local.modeImport = null;
    return local.setTimeoutOnError(onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbLoad"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbLoad (onError)](#apidoc.element.n_.context.utility2.dbLoad)
- description and source-code
```javascript
dbLoad = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will load the db from storage
 */
</span>    var onParallel;
    onParallel = local.onParallel(function (error) {
        local.setTimeoutOnError(onError, error);
    });
    local.storageKeys(function (error, data) {
        onParallel.counter += 1;
        onParallel.counter += 1;
        onParallel(error);
        local.normalizeList(data)
            .filter(function (key) {
                return key.indexOf('dbTable.') === 0;
            })
            .forEach(function (key) {
                onParallel.counter += 1;
                local.storageGetItem(key, function (error, data) {
                    onParallel.counter += 1;
                    onParallel(error);
                    local.dbImport(data, onParallel);
                });
            });
        onParallel();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowGetItem"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowGetItem (dbRow, key)](#apidoc.element.n_.context.utility2.dbRowGetItem)
- description and source-code
```javascript
dbRowGetItem = function (dbRow, key) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the item with the given key from dbRow
 */
</span>    var ii, value;
    value = dbRow;
    key = String(key).split('.');
    // optimization - for-loop
    for (ii = 0; ii < key.length && value && typeof value === 'object'; ii += 1) {
        value = value[key[ii]];
    }
    return value === undefined
        ? null
        : value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowListGetManyByOperator"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListGetManyByOperator (dbRowList, fieldName, operator, bb)](#apidoc.element.n_.context.utility2.dbRowListGetManyByOperator)
- description and source-code
```javascript
dbRowListGetManyByOperator = function (dbRowList, fieldName, operator, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow's in dbRowList with the given operator
 */
</span>    var ii, jj, result, fieldValue, test, typeof2;
    result = [];
    typeof2 = typeof bb;
    if (bb && typeof2 === 'object') {
        switch (operator) {
        case '$in':
        case '$nin':
        case '$regex':
            break;
        default:
            return result;
        }
    }
    switch (operator) {
    case '$eq':
        test = function (aa, bb) {
            return aa === bb;
        };
        break;
    case '$exists':
        bb = !bb;
        test = function (aa, bb) {
            return !((aa === null) ^ bb);
        };
        break;
    case '$gt':
        test = function (aa, bb, typeof1, typeof2) {
            return typeof1 === typeof2 && aa > bb;
        };
        break;
    case '$gte':
        test = function (aa, bb, typeof1, typeof2) {
            return typeof1 === typeof2 && aa >= bb;
        };
        break;
    case '$in':
        if (bb && typeof bb.indexOf === 'function') {
            if (typeof2 === 'string') {
                test = function (aa, bb, typeof1, typeof2) {
                    return typeof1 === typeof2 && bb.indexOf(aa) >= 0;
                };
            } else {
                test = function (aa, bb) {
                    return bb.indexOf(aa) >= 0;
                };
            }
        }
        break;
    case '$lt':
        test = function (aa, bb, typeof1, typeof2) {
            return typeof1 === typeof2 && aa < bb;
        };
        break;
    case '$lte':
        test = function (aa, bb, typeof1, typeof2) {
            return typeof1 === typeof2 && aa <= bb;
        };
        break;
    case '$ne':
        test = function (aa, bb) {
            return aa !== bb;
        };
        break;
    case '$nin':
        if (bb && typeof bb.indexOf === 'function') {
            if (typeof2 === 'string') {
                test = function (aa, bb, typeof1, typeof2) {
                    return typeof1 === typeof2 && bb.indexOf(aa) < 0;
                };
            } else {
                test = function (aa, bb) {
                    return bb.indexOf(aa) < 0;
                };
            }
        }
        break;
    case '$regex':
        if (bb && typeof bb.test === 'function') {
            test = function (aa, bb) {
                return bb.test(aa);
            };
        }
        break;
    case '$typeof':
        test = function (aa, bb, typeof1) {
            // jslint-hack
            local.nop(aa);
            return typeof1 === bb;
        };
        break;
    }
    if (!test) {
        return result;
    }
    // optimization - for-loop
    for (ii = dbRowList.length - 1; ii >= 0; ii -= 1) {
        fieldValue = local.dbRowGetItem(dbRowList[ii], fieldName);
        // normalize to list
        if (!Array.isArray(fieldValue)) {
            fieldValue = [fieldValue];
        }
        // optimization - for-loop
        for (jj = fieldValue.length - 1; jj >= 0; jj -= 1) {
            if (test(fieldValue[jj], bb, typeof fieldValue[jj], typeof2)) {
                result.push(dbRowList[ii]);
                break;
            }
        }
    }
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowListGetManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListGetManyByQuery (dbRowList, query, fieldName)](#apidoc.element.n_.context.utility2.dbRowListGetManyByQuery)
- description and source-code
```javascript
dbRowListGetManyByQuery = function (dbRowList, query, fieldName) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow's in dbRowList with the given query
 */
</span>    var bb, dbRowDict, result;
    result = dbRowList;
    if (!result.length) {
        return result;
    }
    if (!(query && typeof query === 'object')) {
        result = local.dbRowListGetManyByOperator(result, fieldName, '$eq', query);
        return result;
    }
    Object.keys(query).some(function (key) {
        bb = query[key];
        if (key === '$or' && Array.isArray(bb)) {
            dbRowDict = {};
            bb.forEach(function (query) {
                // recurse
                local.dbRowListGetManyByQuery(result, query).forEach(function (dbRow) {
                    dbRowDict[dbRow._id] = dbRow;
                });
            });
            result = Object.keys(dbRowDict).map(function (id) {
                return dbRowDict[id];
            });
            return !result.length;
        }
        if (key[0] === '$') {
            result = local.dbRowListGetManyByOperator(result, fieldName, key, bb);
            return !result.length;
        }
        // recurse
        result = local.dbRowListGetManyByQuery(result, bb, key);
        return !result.length;
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowListRandomCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowListRandomCreate (options)](#apidoc.element.n_.context.utility2.dbRowListRandomCreate)
- description and source-code
```javascript
dbRowListRandomCreate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a dbRowList of options.length random dbRow's
 */
</span>    local.objectSetDefault(options, { dbRowList: [] });
    for (options.ii = 0; options.ii < options.length; options.ii += 1) {
        options.dbRowList.push(local.dbRowRandomCreate(options));
    }
    return options.dbRowList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowProject"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowProject (dbRow, fieldList)](#apidoc.element.n_.context.utility2.dbRowProject)
- description and source-code
```javascript
dbRowProject = function (dbRow, fieldList) {
<span class="apidocCodeCommentSpan">/*
 * this function will deepcopy and project the dbRow with the given fieldList
 */
</span>    var result;
    if (!dbRow) {
        return null;
    }
    // handle list-case
    if (Array.isArray(dbRow)) {
        return dbRow.map(function (dbRow) {
            // recurse
            return local.dbRowProject(dbRow, fieldList);
        });
    }
    // normalize to list
    if (!(Array.isArray(fieldList) && fieldList.length)) {
        fieldList = Object.keys(dbRow);
    }
    result = {};
    fieldList.forEach(function (key) {
        if (key[0] !== '$') {
            result[key] = dbRow[key];
        }
    });
    return JSON.parse(local.jsonStringifyOrdered(result));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowRandomCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowRandomCreate (options)](#apidoc.element.n_.context.utility2.dbRowRandomCreate)
- description and source-code
```javascript
dbRowRandomCreate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random dbRow from options.properties
 */
</span>    var dbRow, tmp;
    dbRow = {};
    Object.keys(options.properties).forEach(function (key) {
        // try to validate data
        local.tryCatchOnError(function () {
            tmp = local.dbFieldRandomCreate({
                modeNotRandom: options.modeNotRandom,
                propDef: options.properties[key]
            });
            local.validateByPropDef({
                data: tmp,
                key: options.properties[key].name,
                schema: options.properties[key]
            });
            dbRow[key] = tmp;
        }, local.nop);
    });
    return local.jsonCopy(local.objectSetOverride(dbRow, options.override(options)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbRowSetId"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbRowSetId (dbRow, idIndex)](#apidoc.element.n_.context.utility2.dbRowSetId)
- description and source-code
```javascript
dbRowSetId = function (dbRow, idIndex) {
<span class="apidocCodeCommentSpan">/*
 * this function will set a random and unique id into dbRow for the given idIndex,
 * if it does not exist
 */
</span>    var id;
    id = dbRow[idIndex.name];
    if (typeof id !== 'number' && typeof id !== 'string') {
        do {
            id = idIndex.isInteger
                ? (1 + Math.random()) * 0x10000000000000
                : 'a' + ((1 + Math.random()) * 0x10000000000000).toString(36).slice(1);
        // optimization - hasOwnProperty
        } while (idIndex.dict.hasOwnProperty(id));
        dbRow[idIndex.name] = id;
    }
    return id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbSave"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbSave (onError)](#apidoc.element.n_.context.utility2.dbSave)
- description and source-code
```javascript
dbSave = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will save the db to storage
 */
</span>    var onParallel;
    onParallel = local.onParallel(function (error) {
        local.setTimeoutOnError(onError, error);
    });
    onParallel.counter += 1;
    Object.keys(local.dbTableDict).forEach(function (key) {
        onParallel.counter += 1;
        local.dbTableDict[key].save(onParallel);
    });
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbTableCreateMany"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableCreateMany (optionsList, onError)](#apidoc.element.n_.context.utility2.dbTableCreateMany)
- description and source-code
```javascript
dbTableCreateMany = function (optionsList, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the optionsList into the db
 */
</span>    var onParallel, result;
    onParallel = local.onParallel(function (error) {
        local.setTimeoutOnError(onError, error, result);
    });
    onParallel.counter += 1;
    result = local.normalizeList(optionsList).map(function (options) {
        onParallel.counter += 1;
        return local.dbTableCreateOne(options, onParallel);
    });
    return local.setTimeoutOnError(onParallel, null, result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbTableCreateOne"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableCreateOne (options, onError)](#apidoc.element.n_.context.utility2.dbTableCreateOne)
- description and source-code
```javascript
dbTableCreateOne = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a dbTable with the given options
 */
</span>    var self;
    options = local.normalizeDict(options);
    // register dbTable
    self = local.dbTableDict[options.name] =
        local.dbTableDict[options.name] || new local._DbTable(options);
    self.sortDefault = options.sortDefault ||
        self.sortDefault ||
        [{ fieldName: '_timeUpdated', isDescending: true }];
    // remove idIndex
    local.normalizeList(options.idIndexRemoveList).forEach(function (index) {
        self.idIndexRemove(index);
    });
    // create idIndex
    local.normalizeList(options.idIndexCreateList).forEach(function (index) {
        self.idIndexCreate(index);
    });
    // upsert dbRow
    self.crudSetManyById(options.dbRowList);
    self.isLoaded = self.isLoaded || options.isLoaded;
    if (!self.isLoaded) {
        local.storageGetItem('dbTable.' + self.name + '.json', function (error, data) {
            // validate no error occurred
            console.assert(!error, error);
            if (!self.isLoaded) {
                local.dbImport(data);
            }
            self.isLoaded = true;
            local.setTimeoutOnError(onError, null, self);
        });
        return self;
    }
    return local.setTimeoutOnError(onError, null, self);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbTableTravisRepoCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoCreate (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoCreate)
- description and source-code
```javascript
dbTableTravisRepoCreate = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a persistent dbTableTravisRepo
 */
</span>    options = local.objectSetDefault(options, {
        idIndexCreateList: [{ name: 'githubRepo' }],
        sortDefault: [{
            fieldName: 'githubRepo'
        }, {
            fieldName: 'last_build_started_at'
        }],
        name: 'TravisRepo'
    });
    local.dbTableTravisRepo = local.db.dbTableCreateOne(options, onError);
    return local.dbTableTravisRepo;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbTableTravisRepoCrudGetManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoCrudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoCrudGetManyByQuery)
- description and source-code
```javascript
dbTableTravisRepoCrudGetManyByQuery = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will query dbTableTravisRepo
 */
</span>    options = local.objectSetDefault(options, {
        fieldList: ['githubRepo', 'last_build_started_at', 'last_build_status'],
        sort: [{ fieldName: 'last_build_started_at' }]
    });
    return local.dbTableTravisRepoCreate().crudGetManyByQuery(options, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.dbTableTravisRepoUpdate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>dbTableTravisRepoUpdate (options, onError)](#apidoc.element.n_.context.utility2.dbTableTravisRepoUpdate)
- description and source-code
```javascript
dbTableTravisRepoUpdate = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will update dbTableTravisRepo with active, public repos
 */
</span>    var dbRowList, self;
    options = local.objectSetDefault(options, { queryLimit: 500, rateLimit: 10 });
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            local.timeElapsedStart(options);
            self = local.dbTableTravisRepo =
                local.dbTableTravisRepoCreate(options, options.onNext);
            break;
        case 2:
            self = local.dbTableTravisRepo = data;
            console.error('dbTableTravisRepoUpdate - updating ' +
                Math.min(options.queryLimit, self.crudCountAll()) +
                ' of ' + self.crudCountAll() + ' dbRows ...');
            local.ajax({
                headers: { Authorization: 'token ' + local.env.TRAVIS_ACCESS_TOKEN },
                url: 'https://api.travis-ci.org/hooks'
            }, options.onNext);
            break;
        case 3:
            // validate no error occurred
            local.assert(!error, error);
            data = JSON.parse(data.responseText)
                .filter(function (dbRow) {
                    return dbRow.active === true && dbRow.private === false;
                })
                .map(function (dbRow) {
                    dbRow.githubRepo = dbRow.uid.replace(':', '/');
                    dbRow.uid = null;
                    dbRow.url = null;
                    return dbRow;
                });
            self.crudUpdateManyById(data);
            dbRowList = local.dbTableTravisRepoCrudGetManyByQuery({
                limit: options.queryLimit
            });
            local.onParallelList({
                list: dbRowList,
                rateLimit: options.rateLimit
            }, function (dbRow, onParallel) {
                dbRow = dbRow.element;
                onParallel.counter += 1;
                local.ajax({
                    headers: {
                        Authorization: 'token ' + local.env.TRAVIS_ACCESS_TOKEN
                    },
                    url: 'https://api.travis-ci.org/repos/' + dbRow.githubRepo
                }, function (error, data) {
                    // validate no error occurred
                    local.assert(!error, error);
                    data = JSON.parse(data.responseText);
                    Object.keys(data).forEach(function (key) {
                        if (data[key] !== null) {
                            dbRow[key] = data[key];
                        }
                    });
                    // ignore extraneous data to save space
                    dbRow.description = null;
                    dbRow.last_build_duration = null;
                    dbRow.last_build_finished_at = null;
                    dbRow.last_build_id = null;
                    dbRow.last_build_number = null;
                    dbRow.last_build_result = null;
                    dbRow.public_key = null;
                    dbRow.slug = null;
                    dbRow.uid = null;
                    dbRow.url = null;
                    if (onParallel.counter === 1 || ((onParallel.ii + 1) % 10 === 0 &&
                            local.timeElapsedPoll(options).timeElapsed >= 5000)) {
                        local.timeElapsedStart(options, Date.now());
                        console.error('dbTableTravisRepoUpdate - updated ' +
                            (onParallel.ii + 1) + ' dbRows');
                    }
                    onParallel();
                });
            }, options.onNext);
            break;
        case 4:
            self.crudSetManyById(dbRowList);
            self.save(options.onNext);
            break;
        default:
            local.setTimeoutOnError(onError, error, self);
        }
    });
    options.modeNext = 0;
    options.onNext();
    return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.domFragmentRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>domFragmentRender (template, dict)](#apidoc.element.n_.context.utility2.domFragmentRender)
- description and source-code
```javascript
domFragmentRender = function (template, dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a dom-fragment rendered from the givent template and dict
 */
</span>    var tmp;
    tmp = document.createElement('template');
    tmp.innerHTML = local.templateRender(template, dict);
    return tmp.content;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.echo"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>echo (arg)](#apidoc.element.n_.context.utility2.echo)
- description and source-code
```javascript
echo = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return the arg
 */
</span>    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.envKeyIsSensitive"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>envKeyIsSensitive (key)](#apidoc.element.n_.context.utility2.envKeyIsSensitive)
- description and source-code
```javascript
envKeyIsSensitive = function (key) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to determine if the env-key is sensitive
 */
</span>    return (/(?:\b|_)(?:decrypt|key|pass|private|secret|token)/)
        .test(key.toLowerCase()) ||
        (/Decrypt|Key|Pass|Private|Secret|Token/).test(key);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.envSanitize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>envSanitize (env)](#apidoc.element.n_.context.utility2.envSanitize)
- description and source-code
```javascript
envSanitize = function (env) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a sanitized copy of the env object,
 * with sensitive env-vars removed
 */
</span>    var result;
    result = {};
    Object.keys(env).forEach(function (key) {
        if (!local.envKeyIsSensitive(key) &&
                typeof env[key] === 'string' &&
                env[key].length <= 4096) {
            result[key] = env[key];
        }
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.errorMessagePrepend"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>errorMessagePrepend (error, message)](#apidoc.element.n_.context.utility2.errorMessagePrepend)
- description and source-code
```javascript
errorMessagePrepend = function (error, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will prepend the message to error.message and error.stack
 */
</span>    error.message = message + error.message;
    error.stack = message + error.stack;
    return error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.exit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>exit (exitCode)](#apidoc.element.n_.context.utility2.exit)
- description and source-code
```javascript
exit = function (exitCode) {
<span class="apidocCodeCommentSpan">/*
 * this function will exit the current process with the given exitCode
 */
</span>    exitCode = !exitCode || Number(exitCode) === 0
        ? 0
        : Number(exitCode) || 1;
    switch (local.modeJs) {
    case 'browser':
        console.error(local.global.fileElectronHtml + ' global_test_results ' +
            JSON.stringify({ global_test_results: local.global.global_test_results }));
        break;
    case 'node':
        process.exit(exitCode);
        break;
    }
    // reset modeTest
    local.modeTest = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.fsRmrSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsRmrSync (dir)](#apidoc.element.n_.context.utility2.fsRmrSync)
- description and source-code
```javascript
fsRmrSync = function (dir) {
<span class="apidocCodeCommentSpan">/*
 * this function will synchronously 'rm -fr' the dir
 */
</span>    local.child_process.spawnSync(
        'rm',
        ['-fr', local.path.resolve(process.cwd(), dir)],
        { stdio: ['ignore', 1, 2] }
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsWriteFileWithMkdirpSync (file, data)](#apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync)
- description and source-code
```javascript
fsWriteFileWithMkdirpSync = function (file, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will synchronously 'mkdir -p' and write the data to file
 */
</span>    // try to write to file
    try {
        require('fs').writeFileSync(file, data);
    } catch (errorCaught) {
        // mkdir -p
        require('child_process').spawnSync(
            'mkdir',
            ['-p', require('path').dirname(file)],
            { stdio: ['ignore', 1, 2] }
        );
        // re-write to file
        require('fs').writeFileSync(file, data);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync2"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>fsWriteFileWithMkdirpSync2 (file, data)](#apidoc.element.n_.context.utility2.fsWriteFileWithMkdirpSync2)
- description and source-code
```javascript
fsWriteFileWithMkdirpSync2 = function (file, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will synchronously 'mkdir -p' and write the data to file
 */
</span>    // try to write to file
    try {
        require('fs').writeFileSync(file, data);
    } catch (errorCaught) {
        // mkdir -p
        require('child_process').spawnSync(
            'mkdir',
            ['-p', require('path').dirname(file)],
            { stdio: ['ignore', 1, 2] }
        );
        // re-write to file
        require('fs').writeFileSync(file, data);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.gen_code"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>gen_code (e, t)](#apidoc.element.n_.context.utility2.gen_code)
- description and source-code
```javascript
function gen_code(e, t){function o(
e){var n=make_string(e,t.ascii_only);return t.inline_script&&(n=n.replace(/<\x2fscript([>\/\t\n\f\r ])/gi
,"<\\/script$1")),n}function u(e){return e=e.toString(),t.ascii_only&&(e=to_ascii
(e)),e}function a(e){return e==null&&(e=""),n&&(e=repeat_string(" ",t.indent_start+
r*t.indent_level)+e),e}function f(e,t){t==null&&(t=1),r+=t;try{return e.apply(null
,slice(arguments,1))}finally{r-=t}}function l(e){return e=e.toString(),e.charAt(
e.length-1)}function c(e){return e.toString().charAt(0)}function h(e){if(n)return e
.join(" ");var t=[];for(var r=0;r<e.length;++r){var i=e[r+1];t.push(e[r]),i&&(is_identifier_char
(l(e[r]))&&(is_identifier_char(c(i))||c(i)=="\\")||/[\+\-]$/.test(e[r].toString(
))&&/^[\+\-]/.test(i.toString())||l(e[r])=="/"&&c(i)=="/")&&t.push(" ")}return t
.join("")}function p(e){return e.join(","+s)}function d(e){var t=b(e);for(var n=1
;n<arguments.length;++n){var r=arguments[n];if(r instanceof Function&&r(e)||e[0]==
r)return"("+t+")"}return t}function v(e){if(e.length==1)return e[0];if(e.length==2
){var t=e[1];return e=e[0],e.length<=t.length?e:t}return v([e[0],v(e.slice(1))])
}function m(e){if(e[0]=="function"||e[0]=="object"){var t=slice(y.stack()),n=t.pop
(),r=t.pop();while(r){if(r[0]=="stat")return!0;if((r[0]!="seq"&&r[0]!="call"&&r[0
]!="dot"&&r[0]!="sub"&&r[0]!="conditional"||r[1]!==n)&&(r[0]!="binary"&&r[0]!="assign"&&
r[0]!="unary-postfix"||r[2]!==n))return!1;n=r,r=t.pop()}}return!HOP(DOT_CALL_NO_PARENS
,e[0])}function g(e){var t=e.toString(10),n=[t.replace(/^0\./,".").replace("e+","e"
)],r;return Math.floor(e)===e?(e>=0?n.push("0x"+e.toString(16).toLowerCase(),"0"+
e.toString(8)):n.push("-0x"+(-e).toString(16).toLowerCase(),"-0"+(-e).toString(8
)),(r=/^(.*?)(0+)$/.exec(e))&&n.push(r[1]+"e"+r[2].length)):(r=/^0?\.(0+)(.*)$/.
exec(e))&&n.push(r[2]+"e-"+(r[1].length+r[2].length),t.substr(t.indexOf("."))),v
(n)}function w(e){if(e==null)return";";if(e[0]=="do")return N([e]);var t=e;for(;
;){var n=t[0];if(n=="if"){if(!t[3])return b(["block",[e]]);t=t[3]}else if(n=="while"||
n=="do")t=t[2];else{if(n!="for"&&n!="for-in")break;t=t[4]}}return b(e)}function E
(e,t,n,r,i){var s=r||"function";return e&&(s+=" "+u(e)),s+="("+p(MAP(t,u))+")",s=
h([s,N(n)]),!i&&m(this)?"("+s+")":s}function S(e){switch(e[0]){case"with":case"while"
:return empty(e[2])||S(e[2]);case"for":case"for-in":return empty(e[4])||S(e[4]);
case"if":if(empty(e[2])&&!e[3])return!0;if(e[3])return empty(e[3])?!0:S(e[3]);return S
(e[2]);case"directive":return!0}}function x(e,t){for(var r=[],i=e.length-1,s=0;s<=
i;++s){var o=e[s],u=b(o);u!=";"&&(!n&&s==i&&!S(o)&&(u=u.replace(/;+\s*$/,"")),r.
push(u))}return t?r:MAP(r,a)}function T(e){var t=e.length;return t==0?"{}":"{"+i+
MAP(e,function(e,r){var s=e[1].length>0,o=f(function(){return a(e[0]?h(["case",b
(e[0])+":"]):"default:")},.5)+(s?i+f(function(){return x(e[1]).join(i)}):"");return!
n&&s&&r<t-1&&(o+=";"),o}).join(i)+i+a("}")}function N(e){return e?e.length==0?"{}"
:"{"+i+f(function(){return x(e).join(i)})+i+a("}"):";"}function C(e){var t=e[0],
n=e[1];return n!=null&&(t=h([u(t),"=",d(n,"seq")])),t}t=defaults(t,{indent_start
:0,indent_level:4,quote_keys:!1,space_colon:!1,beautify:!1,ascii_only:!1,inline_script
:!1});var n=!!t.beautify,r=0,i=n?"\n":"",s=n?" ":"",y=ast_walker(),b=y.walk;return y
.with_walkers({string:o,num:g,name:u,"debugger":function(){return"debugger;"},toplevel
:function(e){return x(e).join(i+i)},splice:function(e){var t=y.parent();return HOP
(SPLICE_NEEDS_BRACKETS,t)?N.apply(this,arguments):MAP(x(e,!0),function(e,t){return t>0?
a(e):e}).join(i)},block:N,"var":function(e){return"var "+p(MAP(e,C))+";"},"const"
:function(e){return"const "+p(MAP(e,C))+";"},"try":function(e,t,n){var r=["try",
N(e)];return t&&r.push("catch","("+t[0]+")",N(t[1])),n&&r.push("finally",N(n)),h
(r)},"throw":function(e){return h(["throw",b(e)])+";"},"new":function(e,t){return t=
t.length>0?"("+p(MAP(t,function(e){return d(e,"seq")}))+")":"",h(["new",d(e,"seq"
,"binary","conditional","assign",function(e){var t=ast_walker(),n={};try{t.with_walkers
({call:function(){throw n},"fun ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.httpRequest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>httpRequest (options, onError)](#apidoc.element.n_.context.utility2.httpRequest)
- description and source-code
```javascript
httpRequest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will request the data from options.url
 */
</span>    var chunkList, onError2, timerTimeout, done, request, response, urlParsed;
    // init onError2
    onError2 = function (error) {
        if (done) {
            return;
        }
        done = true;
        // cleanup timerTimeout
        clearTimeout(timerTimeout);
        // cleanup request and response
        [request, response].forEach(function (stream) {
            // try to end the stream
            try {
                stream.end();
            // else try to destroy the stream
            } catch (errorCaught) {
                try {
                    stream.destroy();
                } catch (ignore) {
                }
            }
        });
        // debug response
        console.error(new Date().toISOString() + ' http-response ' + JSON.stringify({
            method: options.method,
            url: options.url,
            statusCode: (response && response.statusCode) || 0
        }));
        onError(error, response);
    };
    // init timerTimeout
    timerTimeout = setTimeout(function () {
        onError2(new Error('http-request timeout'));
    }, options.timeout || 30000);
    urlParsed = require('url').parse(options.url);
    urlParsed.headers = options.headers;
    urlParsed.method = options.method;
    // debug request
    console.error();
    console.error(new Date().toISOString() + ' http-request ' + JSON.stringify({
        method: options.method,
        url: options.url
    }));
    request = require(
        urlParsed.protocol.slice(0, -1)
    ).request(urlParsed, function (_response) {
        response = _response;
        if (response.statusCode < 200 || response.statusCode > 299) {
            onError2(new Error(response.statusCode));
            return;
        }
        chunkList = [];
        response
            .on('data', function (chunk) {
                chunkList.push(chunk);
            })
            .on('end', function () {
                response.data = Buffer.concat(chunkList);
                onError2();
            })
            .on('error', onError2);
    }).on('error', onError2);
    request.end(options.data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.idDomElementCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>idDomElementCreate (seed)](#apidoc.element.n_.context.utility2.idDomElementCreate)
- description and source-code
```javascript
idDomElementCreate = function (seed) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a unique dom-element id from the seed,
 * that is both dom-selector and url friendly
 */
</span>    var id, ii;
    id = encodeURIComponent(seed).replace((/\W/g), '_');
    for (ii = 2; local.idDomElementDict[id]; ii += 1) {
        id = encodeURIComponent(seed + '_' + ii).replace((/\W/g), '_');
    }
    local.idDomElementDict[id] = true;
    return id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.idFieldInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>idFieldInit (options)](#apidoc.element.n_.context.utility2.idFieldInit)
- description and source-code
```javascript
idFieldInit = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will init options.idAlias, options.idField, and options.queryById
 */
</span>    var idAlias, idField;
    // init idField
    options.idAlias = options.operationId.split('.');
    idField = options.idField = options.idAlias[1] || 'id';
    // init idAlias
    idAlias = options.idAlias = options.idAlias[2] || options.idField;
    // invert queryById
    if (options.modeQueryByIdInvert) {
        idAlias = options.idField;
        idField = options.idAlias;
    }
    // init queryById
    options.idValue = (options.data && options.data[idAlias]) || options.idValue;
    options.queryById = {};
    options.queryById[idField] = options.idValue;
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.instrumentInPackage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>instrumentInPackage (code, file)](#apidoc.element.n_.context.utility2.instrumentInPackage)
- description and source-code
```javascript
instrumentInPackage = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will instrument the code
 * only if the macro /\* istanbul instrument in package $npm_package_nameAlias *\/
 * exists in the code
 */
</span>    return process.env.npm_config_mode_coverage &&
        code.indexOf('/* istanbul ignore all */\n') < 0 && (
            process.env.npm_config_mode_coverage === 'all' ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_package_nameAlias + ' */\n') >= 0 ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_config_mode_coverage + ' */\n') >= 0
        )
        ? local.instrumentSync(code, file)
        : code;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.instrumentSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>instrumentSync (code, file)](#apidoc.element.n_.context.utility2.instrumentSync)
- description and source-code
```javascript
instrumentSync = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. normalize the file
 * 2. save code to __coverageCodeDict__[file] for future html-report
 * 3. return instrumented code
 */
</span>    // 1. normalize the file
    file = local.path.resolve('/', file);
    // 2. save code to __coverageCodeDict__[file] for future html-report
    local.global.__coverageCodeDict__[file] = code;
    // 3. return instrumented code
    return new local.Instrumenter({
        embedSource: true,
        noAutoWrap: true
    }).instrumentSync(code, file).trimLeft();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.isNullOrUndefined"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>isNullOrUndefined (arg)](#apidoc.element.n_.context.utility2.isNullOrUndefined)
- description and source-code
```javascript
isNullOrUndefined = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will test if the arg is null or undefined
 */
</span>    return arg === null || arg === undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.is_alphanumeric_char"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_alphanumeric_char (e)](#apidoc.element.n_.context.utility2.is_alphanumeric_char)
- description and source-code
```javascript
function is_alphanumeric_char(e){return is_digit(e)||is_letter(e)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.is_identifier_char"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_identifier_char (e)](#apidoc.element.n_.context.utility2.is_identifier_char)
- description and source-code
```javascript
function is_identifier_char(e){return is_identifier_start
(e)||is_unicode_combining_mark(e)||is_unicode_digit(e)||is_unicode_connector_punctuation
(e)||e=="\u200c"||e=="\u200d"}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.is_identifier_start"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>is_identifier_start (e)](#apidoc.element.n_.context.utility2.is_identifier_start)
- description and source-code
```javascript
function is_identifier_start(e)
{return e=="$"||e=="_"||is_letter(e)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.istanbulCoverageMerge"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulCoverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2.istanbulCoverageMerge)
- description and source-code
```javascript
istanbulCoverageMerge = function (coverage1, coverage2) {
<span class="apidocCodeCommentSpan">/*
 * this function will merge coverage2 into coverage1
 */
</span>    var dict1, dict2;
    coverage1 = coverage1 || {};
    coverage2 = coverage2 || {};
    Object.keys(coverage2).forEach(function (file) {
        if (!coverage2[file]) {
            return;
        }
        // if file is undefined in coverage1, then add it
        if (!coverage1[file]) {
            coverage1[file] = coverage2[file];
            return;
        }
        // merge file from coverage2 into coverage1
        ['b', 'f', 's'].forEach(function (key) {
            dict1 = coverage1[file][key];
            dict2 = coverage2[file][key];
            switch (key) {
            // increment coverage for branch lines
            case 'b':
                Object.keys(dict2).forEach(function (key) {
                    dict2[key].forEach(function (count, ii) {
                        dict1[key][ii] += count;
                    });
                });
                break;
            // increment coverage for function and statement lines
            case 'f':
            case 's':
                Object.keys(dict2).forEach(function (key) {
                    dict1[key] += dict2[key];
                });
                break;
            }
        });
    });
    return coverage1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.istanbulCoverageReportCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulCoverageReportCreate ()](#apidoc.element.n_.context.utility2.istanbulCoverageReportCreate)
- description and source-code
```javascript
istanbulCoverageReportCreate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. print coverage in text-format to stdout
 * 2. write coverage in html-format to filesystem
 * 3. return coverage in html-format as single document
 */
</span>    var options;
    /* istanbul ignore next */
    if (!local.global.__coverage__) {
        return '';
    }
    options = {};
    options.dir = process.cwd() + '/tmp/build/coverage.html';
    // merge previous coverage
    if (local.modeJs === 'node' && process.env.npm_config_mode_coverage_merge) {
        console.log('merging file://' + options.dir + '/coverage.json to coverage');
        try {
            local.coverageMerge(
                local.global.__coverage__,
                JSON.parse(
                    local._fs.readFileSync(options.dir + '/coverage.json', 'utf8')
                )
            );
        } catch (ignore) {
        }
        try {
            options.coverageCodeDict = JSON.parse(local._fs.readFileSync(
                options.dir + '/coverage.code-dict.json',
                'utf8'
            ));
            Object.keys(options.coverageCodeDict).forEach(function (key) {
                local.global.__coverageCodeDict__[key] =
                    local.global.__coverageCodeDict__[key] ||
                    options.coverageCodeDict[key];
            });
        } catch (ignore) {
        }
    }
    // init writer
    local.coverageReportHtml = '';
    local.coverageReportHtml += '<div class="coverageReportDiv">\n' +
        '<h1>coverage-report</h1>\n' +
        '<div ' +
        'style="background: #fff; border: 1px solid #000; margin 0; padding: 0;">\n';
    local.writerData = '';
    options.sourceStore = {};
    options.writer = local.writer;
    // 1. print coverage in text-format to stdout
    new local.TextReport(options).writeReport(local.collector);
    // 2. write coverage in html-format to filesystem
    new local.HtmlReport(options).writeReport(local.collector);
    local.writer.writeFile('', local.nop);
    // write coverage.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.json',
        JSON.stringify(local.global.__coverage__)
    );
    // write coverage.code-dict.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.code-dict.json',
        JSON.stringify(local.global.__coverageCodeDict__)
    );
    // write coverage.badge.svg
    options.pct = local.coverageReportSummary.root.metrics.lines.pct;
    local.fsWriteFileWithMkdirpSync2(
        local.path.dirname(options.dir) + '/coverage.badge.svg',
        local.templateCoverageBadgeSvg
            // edit coverage badge percent
            .replace((/100.0/g), options.pct)
            // edit coverage badge color
            .replace(
                (/0d0/g),
                ('0' + Math.round((100 - options.pct) * 2.21).toString(16)).slice(-2) +
                    ('0' + Math.round(options.pct * 2.21).toString(16)).slice(-2) + '00'
            )
    );
    console.log('created coverage file://' + options.dir + '/index.html');
    // 3. return coverage in html-format as a single document
    local.coverageReportHtml += '</div>\n</div>\n';
    // write coverage.rollup.html
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.rollup.html',
        local.coverageReportHtml
    );
    return local.coverageReportHtml;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.istanbulInstrumentInPackage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulInstrumentInPackage (code, file)](#apidoc.element.n_.context.utility2.istanbulInstrumentInPackage)
- description and source-code
```javascript
istanbulInstrumentInPackage = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will instrument the code
 * only if the macro /\* istanbul instrument in package $npm_package_nameAlias *\/
 * exists in the code
 */
</span>    return process.env.npm_config_mode_coverage &&
        code.indexOf('/* istanbul ignore all */\n') < 0 && (
            process.env.npm_config_mode_coverage === 'all' ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_package_nameAlias + ' */\n') >= 0 ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_config_mode_coverage + ' */\n') >= 0
        )
        ? local.instrumentSync(code, file)
        : code;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.istanbulInstrumentSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>istanbulInstrumentSync (code, file)](#apidoc.element.n_.context.utility2.istanbulInstrumentSync)
- description and source-code
```javascript
istanbulInstrumentSync = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. normalize the file
 * 2. save code to __coverageCodeDict__[file] for future html-report
 * 3. return instrumented code
 */
</span>    // 1. normalize the file
    file = local.path.resolve('/', file);
    // 2. save code to __coverageCodeDict__[file] for future html-report
    local.global.__coverageCodeDict__[file] = code;
    // 3. return instrumented code
    return new local.Instrumenter({
        embedSource: true,
        noAutoWrap: true
    }).instrumentSync(code, file).trimLeft();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jslintAndPrint"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintAndPrint (script, file)](#apidoc.element.n_.context.utility2.jslintAndPrint)
- description and source-code
```javascript
jslintAndPrint = function (script, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will jslint / csslint the script and print any errors to stderr
 */
</span>    var ignoreDict, lineno, scriptParsed;
    // cleanup errors
    local.errorCounter = 0;
    local.errorText = '';
    // do nothing for empty script
    if (!script.length) {
        return script;
    }
    // init ignoreDict
    ignoreDict = {};
    // init lineno
    lineno = 0;
    // parse script
    scriptParsed = script
        // indent text-block
        // /* jslint-indent-begin */ ... /* jslint-indent-end */
        .replace(
/* jslint-indent-begin 20 */
(function () {
    /*jslint maxlen: 256*/
    return (/^ *?\/\* jslint-indent-begin (\d+?) \*\/$[\S\s]+?^ *?\/\* jslint-indent-end \*\/$/gm);
}()),
/* jslint-indent-end */
            function (match0, match1) {
                return match0.replace(
                    (/(^ *\S)/gm),
                    new Array(Number(match1) + 1).join(' ') + '$1'
                );
            }
        )
        // ignore text-block
        // /* jslint-ignore-begin */ ... /* jslint-ignore-end */
        .replace(
/* jslint-ignore-begin */
(/^ *?\/\* jslint-ignore-begin \*\/$[\S\s]+?^ *?\/\* jslint-ignore-end \*\/$/gm),
/* jslint-ignore-end */
            function (match0) {
                return match0.replace((/.*/g), '');
            }
        )
        // ignore next-line
        // /* jslint-ignore-next-line */
        .replace(
/* jslint-ignore-next-line */
(/^ *?\/\* jslint-ignore-next-line \*\/\n.*/gm),
            function (match0) {
                return match0.replace((/.*/g), '');
            }
        );
    // csslint script
    if (file.slice(-4) === '.css') {
        scriptParsed = scriptParsed.replace(new RegExp([
            // handle flexbox
            ' display: flex;',
            ' flex: .+?;',
            ' flex-.+?: .+?;'
        ].join('|'), 'g'), function () {
            return ' background: url(' + Math.random() + ');';
        });
        local.CSSLint.errors = local.CSSLint.verify(scriptParsed).messages
            .filter(function (error) {
                return !ignoreDict[error.rule.id];
            });
        // if error occurred, then print colorized error messages
        if (!local.CSSLint.errors.length) {
            return script;
        }
        local.errorText = '\n\u001b[1m' + file + '\u001b[22m\n';
        local.CSSLint.errors
            .filter(function (error) {
                return error;
            })
            .forEach(function (error) {
                local.errorCounter += 1;
                lineno += 1;
                local.errorText +=
                    (' #' + String(lineno) + ' ').slice(-4) +
                    '\u001b[33m' + error.type + ' - ' + error.rule.id +
                    ' - ' + error.message + '\n    ' + error.rule.desc +
                    '\u001b[39m\n    ' + String(error.evidence).trim() +
                    '\u001b[90m \/\/ line ' + error.line +
                    ', col ' + error.col + '\u001b[39m\n';
            });
    // jslint es6-script
    } else if ((/^\/\*jslint\b[\s\w,:]*?\bes6: true\b/m)
            .test(scriptParsed.slice(0, 0x1000))) {
        // comment shebang
        scriptParsed = scriptParsed.replace((/^#!/), '//');
        local.jslintEs6.errors = local.jslintEs6(scriptParsed).warnings;
        if (!local.jslintEs6.errors.length) {
            return script;
        }
        // if error occurred, then print colorized error messages
        local.errorText = '\n\u001b[1m' + file + '\u001b[22m\n';
        local.jslintEs6.errors
            .filter(function (error) {
                return error;
            })
            .forEach(function (error) {
                local.errorCounter += 1;
                lineno += 1;
                local.errorText +=
                    (' #' + String(lineno) + ' ').slice(-4) +
                    '\u001b[33m' + error.message +
                    '\u001b[39m\n    ' + String(error.a).trim() +
                    '\u001b[90m \/\/ Line ' + (error.line + 1) +
                    ', Pos ' + (error.column + 1) + '\u001 ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jslintAndPrintConditional"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintAndPrintConditional (script, file, mode)](#apidoc.element.n_.context.utility2.jslintAndPrintConditional)
- description and source-code
```javascript
jslintAndPrintConditional = function (script, file, mode) {
<span class="apidocCodeCommentSpan">/*
 * this function will jslint / csslint the script and print any errors to stderr,
 * conditionally
 */
</span>    var extname;
    // cleanup errors
    local.jslint.errorCounter = 0;
    local.jslint.errorText = '';
    // optimization - ignore uglified/rollup files
    if ((/\bmin\b|\brollup\b/).test(file)) {
        return script;
    }
    extname = (/\.\w+$/).exec(file);
    extname = extname && extname[0];
    switch (extname) {
    case '.css':
        if (script.indexOf('/*csslint') >= 0 || mode === 'force') {
            local.jslintAndPrint(script, file);
        }
        break;
    case '.html':
        // csslint <style> tag
        script.replace(
            (/<style>([\S\s]+?)<\/style>/g),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                match1 = text.slice(0, ii).replace((/.+/g), '') + match1;
                local.jslintAndPrintConditional(match1, file + '.css', mode);
            }
        );
        // jslint <script> tag
        script.replace(
            (/<script>([\S\s]+?)<\/script>/g),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                match1 = text.slice(0, ii).replace((/.+/g), '') + match1;
                local.jslintAndPrintConditional(match1, file + '.js', mode);
            }
        );
        break;
    case '.js':
        if ((script.indexOf('/*jslint') >= 0 &&
                !local.global.__coverage__) || mode === 'force') {
            local.jslintAndPrint(script, file);
        }
        break;
    }
    return script;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jslintEs6"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jslintEs6 (e, i, s)](#apidoc.element.n_.context.utility2.jslintEs6)
- description and source-code
```javascript
jslintEs6 = function (e, i, s){try{ft=[],Y=i||t(),H="anonymous",j=[],F=t(),q=!0,I=[],R=!0,U=t(
),z=[],W=Y.fudge?1:0,V=[],$={id:"(global)",body:!0,context:t(),from:0,level:0,line
:0,live:[],loop:0,"switch":0,thru:0},B=$,X=$,J=!1,et=!1,Q=!1,G=$,Z=t(),tt=[],ot=
undefined,rt=$,it=0,at=undefined,n(F,a,!1),s!==undefined&&n(F,s,!1),Object.keys(
Y).forEach(function(e){if(Y[e]===!0){var t=r[e];Array.isArray(t)&&n(F,t,!1)}}),gt
(e),Et(),J?(ut=St(),Et("(end)")):(Y.browser?G.id===";"&&Et(";"):G.value==="use strict"&&
($.strict=G,Et("(string)"),Et(";")),ut=Ot(),Et("(end)"),X=$,on(ut),Q&&$.strict!==
undefined&&vt("unexpected_a",$.strict),gn(),Y.white||yn()),Y.browser||I.forEach(
function(e){e.directive==="global"&&vt("missing_browser",e)}),R=!1}catch(o){o.name!=="JSLintError"&&
ft.push(o)}return{directives:I,edition:"2016-10-24",exports:U,froms:z,functions:
V,global:$,id:"(JSLint)",json:J,lines:K,module:Q===!0,ok:ft.length===0&&!R,option
:Y,property:Z,stop:R,tokens:st,tree:ut,warnings:ft.sort(function(e,t){return e.line-
t.line||e.column-t.column})}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jsonCopy"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jsonCopy (arg)](#apidoc.element.n_.context.utility2.jsonCopy)
- description and source-code
```javascript
jsonCopy = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a deep-copy of the JSON-arg
 */
</span>    return arg === undefined
        ? undefined
        : JSON.parse(JSON.stringify(arg));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jsonStringifyOrdered"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jsonStringifyOrdered (element, replacer, space)](#apidoc.element.n_.context.utility2.jsonStringifyOrdered)
- description and source-code
```javascript
jsonStringifyOrdered = function (element, replacer, space) {
<span class="apidocCodeCommentSpan">/*
 * this function will JSON.stringify the element,
 * with object-keys sorted and circular-references removed
 */
</span>    var circularList, stringify, tmp;
    stringify = function (element) {
    /*
     * this function will recursively JSON.stringify the element,
     * with object-keys sorted and circular-references removed
     */
        // if element is an object, then recurse its items with object-keys sorted
        if (element &&
                typeof element === 'object' &&
                typeof element.toJSON !== 'function') {
            // ignore circular-reference
            if (circularList.indexOf(element) >= 0) {
                return;
            }
            circularList.push(element);
            // if element is an array, then recurse its elements
            if (Array.isArray(element)) {
                return '[' + element.map(function (element) {
                    // recurse
                    tmp = stringify(element);
                    return typeof tmp === 'string'
                        ? tmp
                        : 'null';
                }).join(',') + ']';
            }
            return '{' + Object.keys(element)
                // sort object-keys
                .sort()
                .map(function (key) {
                    // recurse
                    tmp = stringify(element[key]);
                    if (typeof tmp === 'string') {
                        return JSON.stringify(key) + ':' + tmp;
                    }
                })
                .filter(function (element) {
                    return typeof element === 'string';
                })
                .join(',') + '}';
        }
        // else JSON.stringify as normal
        return JSON.stringify(element);
    };
    circularList = [];
    return JSON.stringify(element && typeof element === 'object'
        // recurse
        ? JSON.parse(stringify(element))
        : element, replacer, space);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtA256GcmDecrypt"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtA256GcmDecrypt (token, key)](#apidoc.element.n_.context.utility2.jwtA256GcmDecrypt)
- description and source-code
```javascript
jwtA256GcmDecrypt = function (token, key) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7516
 * this function will use json-web-encryption to
 * aes-256-gcm-decrypt the token with the given base64url-encoded key
 */
</span>    return local.tryCatchOnError(function () {
        token = token
            .replace((/-/g), '+')
            .replace((/_/g), '/')
            .split('.');
        token = local.sjcl.decrypt(local.sjcl.codec.base64url.toBits(
            local.jwtAes256KeyInit(key)
        ), JSON.stringify({
            adata: token[4],
            ct: token[3],
            iv: token[2],
            ks: 256,
            mode: 'gcm'
        }));
        return local.jwtHs256Decode(token, key);
    }, local.nop) || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtA256GcmEncrypt"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtA256GcmEncrypt (data, key)](#apidoc.element.n_.context.utility2.jwtA256GcmEncrypt)
- description and source-code
```javascript
jwtA256GcmEncrypt = function (data, key) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7516
 * this function will use json-web-encryption to
 * aes-256-gcm-encrypt the data with the given base64url-encoded key
 */
</span>    var adata;
    adata = local.jwtAes256KeyCreate();
    data = local.jwtHs256Encode(data, key);
    data = JSON.parse(local.sjcl.encrypt(
        local.sjcl.codec.base64url.toBits(local.jwtAes256KeyInit(key)),
        data,
        { adata: local.sjcl.codec.base64url.toBits(adata), ks: 256, mode: 'gcm' }
    ));
    return local.jwtBase64UrlNormalize('eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4R0NNIn0..' +
        data.iv + '.' + data.ct + '.' + adata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtAes256KeyCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtAes256KeyCreate ()](#apidoc.element.n_.context.utility2.jwtAes256KeyCreate)
- description and source-code
```javascript
jwtAes256KeyCreate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random, aes-256-base64url-jwt-key
 */
</span>    return local.jwtBase64UrlNormalize(
        local.base64FromBuffer(local.bufferRandomBytes(32))
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtAes256KeyInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtAes256KeyInit (key)](#apidoc.element.n_.context.utility2.jwtAes256KeyInit)
- description and source-code
```javascript
jwtAes256KeyInit = function (key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will init the aes-256-base64url-jwt-key
 */
</span>    // init npm_config_jwtAes256Key
    local.env.npm_config_jwtAes256Key = local.env.npm_config_jwtAes256Key ||
        'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA';
    return key || local.env.npm_config_jwtAes256Key;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtBase64UrlNormalize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtBase64UrlNormalize (text)](#apidoc.element.n_.context.utility2.jwtBase64UrlNormalize)
- description and source-code
```javascript
jwtBase64UrlNormalize = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will normlize the text to base64url format
 */
</span>    return text
        .replace((/\=/g), '')
        .replace((/\+/g), '-')
        .replace((/\//g), '_');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtHs256Decode"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtHs256Decode (token, key)](#apidoc.element.n_.context.utility2.jwtHs256Decode)
- description and source-code
```javascript
jwtHs256Decode = function (token, key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will decode the json-web-token with the given base64-encode key
 */
</span>    var timeNow;
    timeNow = Date.now() / 1000;
    // try to decode the token
    return local.tryCatchOnError(function () {
        token = token.split('.');
        // validate header
        local.assert(token[0] === 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9', token);
        // validate signature
        local.assert(local.sjcl.codec.base64url.fromBits(
            new local.sjcl.misc.hmac(local.sjcl.codec.base64url.toBits(
                local.jwtAes256KeyInit(key)
            )).encrypt(token[0] + '.' + token[1])
        ) === token[2]);
        // return decoded data
        token = JSON.parse(local.base64ToString(token[1]));
        // https://tools.ietf.org/html/rfc7519#section-4.1
        // validate jwt-registered-headers
        local.assert(!token.exp || token.exp >= timeNow);
        local.assert(!token.nbf || token.nbf <= timeNow);
        return token;
    }, local.nop) || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtHs256Encode"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtHs256Encode (data, key)](#apidoc.element.n_.context.utility2.jwtHs256Encode)
- description and source-code
```javascript
jwtHs256Encode = function (data, key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will encode the data into a json-web-token
 * with the given base64-encode key
 */
</span>    data = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.' +
        local.jwtBase64UrlNormalize(local.base64FromString(JSON.stringify(data)));
    return data + '.' + local.sjcl.codec.base64url.fromBits(
        new local.sjcl.misc.hmac(local.sjcl.codec.base64url.toBits(
            local.jwtAes256KeyInit(key)
        )).encrypt(data)
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.jwtNormalize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>jwtNormalize (data)](#apidoc.element.n_.context.utility2.jwtNormalize)
- description and source-code
```javascript
jwtNormalize = function (data) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7519#section-4.1
 * this function will normalize the jwt-data with registered-headers
 */
</span>    var timeNow;
    timeNow = Date.now() / 1000;
    return local.objectSetDefault(data, {
        exp: timeNow + 5 * 60,
        iat: timeNow,
        jti: Math.random().toString(16).slice(2),
        nbf: timeNow
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.listGetElementRandom"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>listGetElementRandom (list)](#apidoc.element.n_.context.utility2.listGetElementRandom)
- description and source-code
```javascript
listGetElementRandom = function (list) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a random element from the list
 */
</span>    return list[Math.floor(list.length * Math.random())];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.listShuffle"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>listShuffle (list)](#apidoc.element.n_.context.utility2.listShuffle)
- description and source-code
```javascript
listShuffle = function (list) {
<span class="apidocCodeCommentSpan">/*
 * https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle
 * this function will inplace shuffle the list, via fisher-yates algorithm
 */
</span>    var ii, random, swap;
    for (ii = list.length - 1; ii > 0; ii -= 1) {
        // coerce to finite integer
        random = (Math.random() * (ii + 1)) | 0;
        swap = list[ii];
        list[ii] = list[random];
        list[random] = swap;
    }
    return list;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.make_string"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>make_string (e, t)](#apidoc.element.n_.context.utility2.make_string)
- description and source-code
```javascript
function make_string(e, t){var n=0,r=0;return e=
e.replace(/[\\\b\f\n\r\t\x22\x27\u2028\u2029\0]/g,function(e){switch(e){case"\\"
:return"\\\\";case"\b":return"\\b";case"\f":return"\\f";case"\n":return"\\n";case"\r"
:return"\\r";case"\u2028":return"\\u2028";case"\u2029":return"\\u2029";case'"':return++
n,'"';case"'":return++r,"'";case"\0":return"\\0"}return e}),t&&(e=to_ascii(e)),n>
r?"'"+e.replace(/\x27/g,"\\'")+"'":'"'+e.replace(/\x22/g,'\\"')+'"'}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.member"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>member (e, t)](#apidoc.element.n_.context.utility2.member)
- description and source-code
```javascript
function member(e, t){for(
var n=t.length;--n>=0;)if(t[n]==e)return!0;return!1}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareAssetsCached"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareAssetsCached (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareAssetsCached)
- description and source-code
```javascript
middlewareAssetsCached = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will serve cached-assets
 */
</span>    var options;
    options = {};
    local.onNext(options, function (error, data) {
        options.result = options.result || local.assetsDict[request.urlParsed.pathname];
        if (options.result === undefined) {
            nextMiddleware(error);
            return;
        }
        switch (options.modeNext) {
        case 1:
            // skip gzip
            if (response.headersSent ||
                    !(/\bgzip\b/).test(request.headers['accept-encoding'])) {
                options.modeNext += 1;
                options.onNext();
                return;
            }
            // gzip and cache result
            local.taskCreateCached({
                cacheDict: 'middlewareAssetsCachedGzip',
                key: request.urlParsed.pathname
            }, function (onError) {
                local.zlib.gzip(options.result, function (error, data) {
                    onError(error, !error && data.toString('base64'));
                });
            }, options.onNext);
            break;
        case 2:
            // set gzip header
            options.result = local.base64ToBuffer(data);
            response.setHeader('Content-Encoding', 'gzip');
            response.setHeader('Content-Length', options.result.length);
            options.onNext();
            break;
        case 3:
            local.middlewareCacheControlLastModified(request, response, options.onNext);
            break;
        case 4:
            response.end(options.result);
            break;
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareBodyParse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareBodyParse (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareBodyParse)
- description and source-code
```javascript
middlewareBodyParse = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will parse request.bodyRaw
 */
</span>    var ii, jj, options;
    // jslint-hack
    local.nop(response);
    // if request is already parsed, then goto nextMiddleware
    if (!local.isNullOrUndefined(request.swgg.bodyParsed)) {
        nextMiddleware();
        return;
    }
    switch (String(request.headers['content-type']).split(';')[0]) {
    // parse application/x-www-form-urlencoded, e.g.
    // aa=hello%20world&bb=bye%20world
    case 'application/x-www-form-urlencoded':
        request.swgg.bodyParsed = local.bufferToString(request.bodyRaw);
        request.swgg.bodyParsed =
            local.urlParse('?' + request.swgg.bodyParsed, true).query;
        break;
    /*
     * https://tools.ietf.org/html/rfc7578
     * parse multipart/form-data, e.g.
     * --Boundary\r\n
     * Content-Disposition: form-data; name="key"\r\n
     * \r\n
     * value\r\n
     * --Boundary\r\n
     * Content-Disposition: form-data; name="input1"; filename="file1.png"\r\n
     * Content-Type: image/jpeg\r\n
     * \r\n
     * <data1>\r\n
     * --Boundary\r\n
     * Content-Disposition: form-data; name="input2"; filename="file2.png"\r\n
     * Content-Type: image/jpeg\r\n
     * \r\n
     * <data2>\r\n
     * --Boundary--\r\n
     */
    case 'multipart/form-data':
        request.swgg.isMultipartFormData = true;
        request.swgg.bodyParsed = {};
        request.swgg.bodyMeta = {};
        options = {};
        options.crlf = local.bufferCreate([0x0d, 0x0a]);
        // init boundary
        ii = 0;
        jj = local.bufferIndexOfSubBuffer(request.bodyRaw, options.crlf, ii);
        if (jj <= 0) {
            break;
        }
        options.boundary = local.bufferConcat([
            options.crlf,
            request.bodyRaw.slice(ii, jj)
        ]);
        ii = jj + 2;
        while (true) {
            jj = local.bufferIndexOfSubBuffer(
                request.bodyRaw,
                options.boundary,
                ii
            );
            if (jj < 0) {
                break;
            }
            options.header = local.bufferToString(request.bodyRaw.slice(ii, ii + 1024))
                .split('\r\n').slice(0, 2).join('\r\n');
            options.contentType = (/^content-type:(.*)/im).exec(options.header);
            options.contentType = options.contentType && options.contentType[1].trim();
            options.filename = (/^content-disposition:.*?\bfilename="([^"]+)/im)
                .exec(options.header);
            options.filename = options.filename && options.filename[1];
            options.name = (/^content-disposition:.*?\bname="([^"]+)/im)
                .exec(options.header);
            options.name = options.name && options.name[1];
            ii = local.bufferIndexOfSubBuffer(
                request.bodyRaw,
                [0x0d, 0x0a, 0x0d, 0x0a],
                ii + 2
            ) + 4;
            options.data = request.bodyRaw.slice(ii, jj);
            request.swgg.bodyParsed[options.name] = options.data;
            request.swgg.bodyMeta[options.name] = {
                contentType: options.contentType,
                filename: options.filename,
                name: options.name
            };
            ii = jj + options.boundary.length + 2;
        }
        break;
    default:
        request.swgg.bodyParsed = local.bufferToString(request.bodyRaw);
        // try to JSON.parse the string
        local.tryCatchOnError(function () {
            request.swgg.bodyParsed = JSON.parse(request.swgg.bodyParsed);
        }, local.nop);
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareBodyRead"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareBodyRead (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareBodyRead)
- description and source-code
```javascript
middlewareBodyRead = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * read and save the request-body to request.bodyRaw
 */
</span>    // jslint-hack
    local.nop(response);
    // if request is already read, then goto nextMiddleware
    if (!request.readable) {
        nextMiddleware();
        return;
    }
    local.streamReadAll(request, function (error, data) {
        request.bodyRaw = request.bodyRaw || data;
        nextMiddleware(error);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareCacheControlLastModified"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCacheControlLastModified ( request, response, nextMiddleware )](#apidoc.element.n_.context.utility2.middlewareCacheControlLastModified)
- description and source-code
```javascript
middlewareCacheControlLastModified = function ( request, response, nextMiddleware ) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will update the Last-Modified header
 */
</span>    // do not cache if headers already sent or url has '?' search indicator
    if (!(response.headersSent || request.url.indexOf('?') >= 0)) {
        // init serverResponseHeaderLastModified
        local.serverResponseHeaderLastModified =
            local.serverResponseHeaderLastModified ||
            // resolve to 1000 ms
            new Date(new Date(Math.floor(Date.now() / 1000) * 1000).toGMTString());
        // respond with 304 If-Modified-Since serverResponseHeaderLastModified
        if (new Date(request.headers['if-modified-since']) >=
                local.serverResponseHeaderLastModified) {
            response.statusCode = 304;
            response.end();
            return;
        }
        response.setHeader('Cache-Control', 'no-cache');
        response.setHeader(
            'Last-Modified',
            local.serverResponseHeaderLastModified.toGMTString()
        );
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareCrudBuiltin"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCrudBuiltin (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareCrudBuiltin)
- description and source-code
```javascript
middlewareCrudBuiltin = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * run the builtin crud-operations backed by db-lite
 */
</span>    var crud, onParallel, options, tmp, user;
    options = {};
    local.onNext(options, function (error, data, meta) {
        switch (options.modeNext) {
        case 1:
            crud = request.swgg.crud;
            user = request.swgg.user;
            switch (crud.operationId.split('.')[0]) {
            case 'crudCountManyByQuery':
                crud.dbTable.crudCountManyByQuery(crud.queryWhere, options.onNext);
                break;
            case 'crudSetManyById':
                crud.dbTable.crudSetManyById(crud.body, options.onNext);
                break;
            case 'crudSetOneById':
                // replace idField with idAlias in body
                delete crud.body.id;
                delete crud.body[crud.idField];
                crud.body[crud.idAlias] = crud.data[crud.idField];
                crud.dbTable.crudSetOneById(crud.body, options.onNext);
                break;
            case 'crudUpdateOneById':
                // replace idField with idAlias in body
                delete crud.body.id;
                delete crud.body[crud.idField];
                crud.body[crud.idAlias] = crud.data[crud.idField];
                crud.dbTable.crudUpdateOneById(crud.body, options.onNext);
                break;
            // coverage-hack - test error handling-behavior
            case 'crudErrorDelete':
            case 'crudErrorGet':
            case 'crudErrorHead':
            case 'crudErrorOptions':
            case 'crudErrorPatch':
            case 'crudErrorPost':
            case 'crudErrorPut':
                options.onNext(local.errorDefault);
                break;
            case 'crudGetManyByQuery':
                onParallel = local.onParallel(options.onNext);
                onParallel.counter += 1;
                crud.dbTable.crudGetManyByQuery({
                    fieldList: crud.queryFields,
                    limit: crud.queryLimit,
                    query: crud.queryWhere,
                    skip: crud.querySkip,
                    sort: crud.querySort
                }, function (error, data) {
                    crud.queryData = data;
                    onParallel(error);
                });
                onParallel.counter += 1;
                crud.dbTable.crudCountAll(function (error, data) {
                    crud.paginationCountTotal = data;
                    onParallel(error);
                });
                break;
            case 'crudGetOneById':
                crud.dbTable.crudGetOneById(crud.queryById, options.onNext);
                break;
            case 'crudGetOneByQuery':
                crud.dbTable.crudGetOneByQuery({
                    query: crud.queryWhere
                }, options.onNext);
                break;
            case 'crudNullDelete':
            case 'crudNullGet':
            case 'crudNullHead':
            case 'crudNullOptions':
            case 'crudNullPatch':
            case 'crudNullPost':
            case 'crudNullPut':
                options.onNext();
                break;
            case 'crudRemoveManyByQuery':
                crud.dbTable.crudRemoveManyByQuery(crud.queryWhere, options.onNext);
                break;
            case 'crudRemoveOneById':
                crud.dbTable.crudRemoveOneById(crud.queryById, options.onNext);
                break;
            case 'fileGetOneById':
                local.dbTableFile = local.db.dbTableCreateOne({ name: 'File' });
                crud.dbTable.crudGetOneById(crud.queryById, options.onNext);
                break;
            case 'fileUploadManyByForm':
                local.dbTableFile = local.db.dbTableCreateOne({ name: 'File' });
                request.swgg.paramDict = {};
                Object.keys(request.swgg.bodyMeta).forEach(function (key) {
                    if (typeof request.swgg.bodyMeta[key].filename !== 'string') {
                        request.swgg.paramDi ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareCrudEnd"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareCrudEnd (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareCrudEnd)
- description and source-code
```javascript
middlewareCrudEnd = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will end the builtin crud-operations
 */
</span>    // jslint-hack
    local.nop(response);
    if (request.swgg.crud.endArgList) {
        local.serverRespondJsonapi.apply(null, request.swgg.crud.endArgList);
        return;
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareFileServer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareFileServer (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareFileServer)
- description and source-code
```javascript
middlewareFileServer = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will serve files
 */
</span>    if (request.method !== 'GET' || local.modeJs === 'browser') {
        nextMiddleware();
        return;
    }
    request.urlFile = (process.cwd() + request.urlParsed.pathname
        // security - disable parent directory lookup
        .replace((/.*\/\.\.\//g), '/'))
        // replace trailing '/' with '/index.html'
        .replace((/\/$/), '/index.html');
    // serve file from cache
    local.taskCreateCached({
        cacheDict: 'middlewareFileServer',
        key: request.urlFile
    // run background-task to re-cache file
    }, function (onError) {
        local.fs.readFile(request.urlFile, function (error, data) {
            onError(error, data && local.base64FromBuffer(data));
        });
    }, function (error, data) {
        // default to nextMiddleware
        if (error) {
            nextMiddleware();
            return;
        }
        // init response-header content-type
        request.urlParsed.contentType = (/\.[^\.]*$/).exec(request.urlParsed.pathname);
        request.urlParsed.contentType = local.contentTypeDict[
            request.urlParsed.contentType && request.urlParsed.contentType[0]
        ];
        local.serverRespondHeadSet(request, response, null, {
            'Content-Type': request.urlParsed.contentType
        });
        // serve file from cache
        response.end(local.base64ToBuffer(data));
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareForwardProxy"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareForwardProxy (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareForwardProxy)
- description and source-code
```javascript
middlewareForwardProxy = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will forward-proxy the request
 * to its destination-host
 */
</span>    var onError, options, timerTimeout;
    // handle preflight-cors
    if ((request.headers['access-control-request-headers'] || '')
            .indexOf('forward-proxy-url') >= 0) {
        // enable cors
        // http://en.wikipedia.org/wiki/Cross-origin_resource_sharing
        local.serverRespondHeadSet(request, response, null, {
            'Access-Control-Allow-Headers': 'forward-proxy-headers,forward-proxy-url',
            'Access-Control-Allow-Methods': 'DELETE,GET,HEAD,OPTIONS,PATCH,POST,PUT',
            'Access-Control-Allow-Origin': '*'
        });
        response.end();
        return;
    }
    if (!request.headers['forward-proxy-url']) {
        nextMiddleware();
        return;
    }
    // enable cors
    // http://en.wikipedia.org/wiki/Cross-origin_resource_sharing
    local.serverRespondHeadSet(request, response, null, {
        'Access-Control-Allow-Headers': 'forward-proxy-headers,forward-proxy-url',
        'Access-Control-Allow-Methods': 'DELETE,GET,HEAD,OPTIONS,PATCH,POST,PUT',
        'Access-Control-Allow-Origin': '*'
    });
    // init onError
    onError = function (error) {
        clearTimeout(timerTimeout);
        if (!error || options.done) {
            return;
        }
        options.done = true;
        // cleanup client
        local.streamListCleanup([options.clientRequest, options.clientResponse]);
        nextMiddleware(error);
    };
    // init options
    options = local.urlParse(request.headers['forward-proxy-url']);
    options.method = request.method;
    options.url = request.headers['forward-proxy-url'];
    // init timerTimeout
    timerTimeout = local.onTimeout(
        onError,
        local.timeoutDefault,
        'forward-proxy ' + options.method + ' ' + options.url
    );
    // parse headers
    options.headers = {};
    local.tryCatchOnError(function () {
        options.headers = JSON.parse(request.headers['forward-proxy-headers']);
    }, local.nop);
    // debug options
    local._debugForwardProxy = options;
    console.error(new Date().toISOString() + ' middlewareForwardProxy ' +
        JSON.stringify({
            method: options.method,
            url: options.url,
            headers: options.headers
        }));
    options.clientRequest = (options.protocol === 'https:'
        ? local.https
        : local.http).request(options, function (clientResponse) {
        options.clientResponse = clientResponse.on('error', onError);
        // pipe clientResponse to serverResponse
        options.clientResponse.pipe(response);
    }).on('error', onError);
    // init event-handling
    request.on('error', onError);
    response.on('finish', onError).on('error', onError);
    // pipe serverRequest to clientRequest
    request.pipe(options.clientRequest);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareGroupCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareGroupCreate (middlewareList)](#apidoc.element.n_.context.utility2.middlewareGroupCreate)
- description and source-code
```javascript
middlewareGroupCreate = function (middlewareList) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a middleware that will
 * sequentially run the sub-middlewares in middlewareList
 */
</span>    var self;
    self = function (request, response, nextMiddleware) {
        var options;
        options = {};
        local.onNext(options, function (error) {
            // recurse with next middleware in middlewareList
            if (options.modeNext < self.middlewareList.length) {
                // run the sub-middleware
                self.middlewareList[options.modeNext](
                    request,
                    response,
                    options.onNext
                );
                return;
            }
            // default to nextMiddleware
            nextMiddleware(error);
        });
        options.modeNext = -1;
        options.onNext();
    };
    self.middlewareList = middlewareList;
    return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareInit)
- description and source-code
```javascript
middlewareInit = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will init the request and response
 */
</span>    // debug server-request
    local._debugServerRequest = request;
    // debug server-response
    local._debugServerResponse = response;
    // init timerTimeout
    local.serverRespondTimeoutDefault(request, response, local.timeoutDefault);
    // init request.urlParsed
    request.urlParsed = local.urlParse(request.url);
    // init response-header content-type
    request.urlParsed.contentType = (/\.[^\.]*$/).exec(request.urlParsed.pathname);
    request.urlParsed.contentType = local.contentTypeDict[
        request.urlParsed.contentType && request.urlParsed.contentType[0]
    ];
    local.serverRespondHeadSet(request, response, null, {
        'Content-Type': request.urlParsed.contentType
    });
    // set main-page content-type to text/html
    if (request.urlParsed.pathname === '/') {
        local.serverRespondHeadSet(request, response, null, {
            'Content-Type': 'text/html; charset=UTF-8'
        });
    }
    // init response.end and response.write to accept Uint8Array instance
    ['end', 'write'].forEach(function (key) {
        response['_' + key] = response['_' + key] || response[key];
        response[key] = function () {
            var args;
            args = Array.from(arguments);
            args[0] = local.bufferToNodeBuffer(args[0]);
            response['_' + key].apply(response, args);
        };
    });
    // default to nextMiddleware
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareRouter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareRouter (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareRouter)
- description and source-code
```javascript
middlewareRouter = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * map the request's method-path to swagger's tags[0]-operationId
 */
</span>    var tmp;
    // jslint-hack
    local.nop(response);
    // init swgg object
    local.objectSetDefault(
        request,
        { swgg: { crud: { operationId: '' }, user: {} } },
        2
    );
    // if request.url is not prefixed with swaggerJson.basePath,
    // then default to nextMiddleware
    if (request.urlParsed.pathname.indexOf(local.swaggerJson.basePath) !== 0) {
        nextMiddleware();
        return;
    }
    // init pathname
    request.swgg.pathname = request.method + ' ' + request.urlParsed.pathname
        .replace(local.swaggerJson.basePath, '');
    // init pathObject
    while (request.swgg.pathname !== tmp) {
        request.swgg.pathObject =
            local.apiDict[request.swgg.pathname] ||
            // handle /foo/{id}/bar case
            local.apiDict[request.swgg.pathname
                .replace((/\/[^\/]+\/([^\/]*?)$/), '//$1')];
        // if pathObject exists, then break
        if (request.swgg.pathObject) {
            request.swgg.pathObject = local.jsonCopy(request.swgg.pathObject);
            request.swgg.pathname = request.swgg.pathObject._keyPath;
            // init crud.operationId
            request.swgg.crud.operationId = request.swgg.pathObject._operationId;
            break;
        }
        tmp = request.swgg.pathname;
        request.swgg.pathname = request.swgg.pathname
            .replace((/\/[^\/]+?(\/*?)$/), '/$1');
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareUserLogin"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareUserLogin (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareUserLogin)
- description and source-code
```javascript
middlewareUserLogin = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will handle user login
 */
</span>    var crud, options, user;
    options = {};
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            local.dbTableUser = local.db.dbTableCreateOne({ name: 'User' });
            crud = request.swgg.crud;
            user = request.swgg.user = {};
            user.jwtEncrypted = request.headers.authorization &&
                request.headers.authorization.replace('Bearer ', '');
            user.jwtDecrypted = local.jwtA256GcmDecrypt(user.jwtEncrypted);
            switch (crud.operationId.split('.')[0]) {
            // coverage-hack - test error handling-behavior
            case 'crudErrorLogin':
                options.onNext(local.errorDefault);
                return;
            case 'userLoginByPassword':
                user.password = request.urlParsed.query.password;
                user.username = request.urlParsed.query.username;
                if (user.password && user.username) {
                    local.dbTableUser.crudGetOneById({
                        username: user.username
                    }, options.onNext);
                    return;
                }
                break;
            default:
                if (user.jwtDecrypted.sub) {
                    // init username
                    user.username = user.jwtDecrypted.sub;
                    local.dbTableUser.crudGetOneById({
                        username: user.username
                    }, options.onNext);
                    return;
                }
            }
            options.modeNext = Infinity;
            options.onNext();
            break;
        case 2:
            switch (crud.operationId.split('.')[0]) {
            case 'userLoginByPassword':
                user.data = data;
                if (!local.sjclHashScryptValidate(
                        user.password,
                        user.data && user.data.password
                    )) {
                    options.modeNext = Infinity;
                    options.onNext();
                    return;
                }
                // init isAuthenticated
                user.isAuthenticated = true;
                // https://tools.ietf.org/html/rfc7519
                // create JSON Web Token (JWT)
                user.jwtDecrypted = {};
                user.jwtDecrypted.sub = user.data.username;
                // update jwtEncrypted in client
                user.jwtEncrypted = local.jwtA256GcmEncrypt(user.jwtDecrypted);
                local.serverRespondHeadSet(request, response, null, {
                    'swgg-jwt-encrypted': user.jwtEncrypted
                });
                // update jwtEncrypted in dbTableUser
                local.dbTableUser.crudUpdateOneById({
                    jwtEncrypted: user.jwtEncrypted,
                    username: user.jwtDecrypted.sub
                }, options.onNext);
                return;
            default:
                data = user.data = data || {};
                if (data.jwtEncrypted) {
                    // init isAuthenticated
                    user.isAuthenticated = true;
                    // update jwtEncrypted in client
                    if (data.jwtEncrypted !== user.jwtEncrypted) {
                        user.jwtEncrypted = data.jwtEncrypted;
                        user.jwtDecrypted = local.jwtA256GcmDecrypt(user.jwtEncrypted);
                        local.serverRespondHeadSet(request, response, null, {
                            'swgg-jwt-encrypted': user.jwtEncrypted
                        });
                    }
                }
            }
            options.onNext();
            break;
        default:
            nextMiddleware(error);
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.middlewareValidate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>middlewareValidate (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2.middlewareValidate)
- description and source-code
```javascript
middlewareValidate = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will validate the swagger-request
 */
</span>    var crud, modeNext, onNext, tmp;
    modeNext = 0;
    onNext = function () {
        modeNext += 1;
        switch (modeNext) {
        case 1:
            // serve swagger.json
            if (request.method + ' ' + request.urlParsed.pathname ===
                    'GET ' + local.swaggerJson.basePath + '/swagger.json') {
                response.end(JSON.stringify(local.swaggerJson));
                return;
            }
            if (!request.swgg.pathObject) {
                modeNext = Infinity;
                onNext();
                return;
            }
            // init paramDict
            request.swgg.paramDict = {};
            // parse path param
            tmp = request.urlParsed.pathname
                .replace(local.swaggerJson.basePath, '').split('/');
            request.swgg.pathObject._path.split('/').forEach(function (key, ii) {
                if ((/^\{\S*?\}$/).test(key)) {
                    request.swgg.paramDict[key.slice(1, -1)] =
                        decodeURIComponent(tmp[ii]);
                }
            });
            request.swgg.pathObject.parameters.forEach(function (paramDef) {
                switch (paramDef.in) {
                // parse body param
                case 'body':
                    request.swgg.paramDict[paramDef.name] = request.swgg.bodyParsed ||
                        undefined;
                    break;
                // parse formData param
                case 'formData':
                    switch (String(request.headers['content-type']).split(';')[0]) {
                    case 'application/x-www-form-urlencoded':
                        request.swgg.paramDict[paramDef.name] =
                            request.swgg.bodyParsed[paramDef.name];
                        break;
                    }
                    break;
                // parse header param
                case 'header':
                    request.swgg.paramDict[paramDef.name] =
                        request.headers[paramDef.name.toLowerCase()];
                    break;
                // parse query param
                case 'query':
                    request.swgg.paramDict[paramDef.name] =
                        request.urlParsed.query[paramDef.name];
                    break;
                }
                // parse array-multi
                if (request.swgg.paramDict[paramDef.name] &&
                        paramDef.type === 'array' &&
                        paramDef.collectionFormat === 'multi') {
                    tmp = '';
                    request.swgg.paramDict[paramDef.name].forEach(function (value) {
                        tmp += '&' + encodeURIComponent(paramDef.name) + '=' +
                            encodeURIComponent(value);
                    });
                    request.swgg.paramDict[paramDef.name] = tmp.slice(1);
                }
                // init default param
                if (local.isNullOrUndefined(request.swgg.paramDict[paramDef.name]) &&
                        paramDef.default !== undefined) {
                    request.swgg.paramDict[paramDef.name] =
                        local.jsonCopy(paramDef.default);
                }
            });
            // normalize paramDict
            local.normalizeParamDictSwagger(
                request.swgg.paramDict,
                request.swgg.pathObject
            );
            // validate paramDict
            local.validateByParamDefList({
                data: request.swgg.paramDict,
                key: request.swgg.pathname,
                paramDefList: request.swgg.pathObject.parameters
            });
            onNext();
            break;
        case 2:
            // init crud
            crud = request.swgg.crud;
            // init crud.dbTable
            crud.dbTable = request.swgg.pathObject &&
                request.swgg.pathObject._schemaName &&
                local.db.dbTableCreateOne({ ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.moduleDirname"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>moduleDirname (module, modulePathList)](#apidoc.element.n_.context.utility2.moduleDirname)
- description and source-code
```javascript
moduleDirname = function (module, modulePathList) {
<span class="apidocCodeCommentSpan">/*
 * this function will search modulePathList for the module's __dirname
 */
</span>    var result, tmp;
    // search process.cwd()
    if (!module || module === '.' || module.indexOf('/') >= 0) {
        return require('path').resolve(process.cwd(), module || '');
    }
    // search builtin
    if (Object.keys(process.binding('natives')).indexOf(module) >= 0) {
        return module;
    }
    // search modulePathList
    [
        ['node_modules'],
        modulePathList,
        require('module').globalPaths
    ].some(function (modulePathList) {
        modulePathList.some(function (modulePath) {
            try {
                tmp = require('path').resolve(
                    process.cwd(),
                    modulePath + '/' + module
                );
                result = require('fs').statSync(tmp).isDirectory() && tmp;
                return result;
            } catch (ignore) {
            }
        });
        return result;
    });
    return result || '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.nop"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>nop ()](#apidoc.element.n_.context.utility2.nop)
- description and source-code
```javascript
nop = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.normalizeDict"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeDict (dict)](#apidoc.element.n_.context.utility2.normalizeDict)
- description and source-code
```javascript
normalizeDict = function (dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the dict
 */
</span>    return dict && typeof dict === 'object' && !Array.isArray(dict)
        ? dict
        : {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.normalizeList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeList (list)](#apidoc.element.n_.context.utility2.normalizeList)
- description and source-code
```javascript
normalizeList = function (list) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the list
 */
</span>    return Array.isArray(list)
        ? list
        : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.normalizeParamDictSwagger"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeParamDictSwagger (data, pathObject)](#apidoc.element.n_.context.utility2.normalizeParamDictSwagger)
- description and source-code
```javascript
normalizeParamDictSwagger = function (data, pathObject) {
<span class="apidocCodeCommentSpan">/*
 * this function will parse the data according to pathObject.parameters
 */
</span>    var tmp;
    pathObject.parameters.forEach(function (paramDef) {
        tmp = data[paramDef.name];
        // init default value
        if (local.isNullOrUndefined(tmp) && paramDef.default !== undefined) {
            tmp = local.jsonCopy(paramDef.default);
        }
        // parse array
        if (paramDef.type === 'array' && paramDef.in !== 'body') {
            if (typeof tmp === 'string') {
                switch (paramDef.collectionFormat) {
                case 'json':
                    local.tryCatchOnError(function () {
                        tmp = JSON.parse(tmp);
                    }, local.nop);
                    data[paramDef.name] = tmp;
                    return;
                case 'multi':
                    tmp = local.urlParse('?' + tmp, true).query[paramDef.name];
                    break;
                case 'pipes':
                    tmp = tmp.split('|');
                    break;
                case 'ssv':
                    tmp = tmp.split(' ');
                    break;
                case 'tsv':
                    tmp = tmp.split('\t');
                    break;
                // default to csv
                default:
                    tmp = tmp.split(',');
                }
                if (paramDef.items && paramDef.items.type !== 'string') {
                    // try to JSON.parse the string
                    local.tryCatchOnError(function () {
                        tmp = tmp.map(function (element) {
                            return JSON.parse(element);
                        });
                    }, local.nop);
                }
            }
        // JSON.parse paramDict
        } else if (paramDef.type !== 'file' &&
                paramDef.type !== 'string' &&
                (typeof tmp === 'string' || tmp instanceof local.global.Uint8Array)) {
            // try to JSON.parse the string
            local.tryCatchOnError(function () {
                tmp = JSON.parse(local.bufferToString(tmp));
            }, local.nop);
        }
        data[paramDef.name] = tmp;
    });
    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.normalizeText"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>normalizeText (text)](#apidoc.element.n_.context.utility2.normalizeText)
- description and source-code
```javascript
normalizeText = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the text
 */
</span>    return typeof text === 'string'
        ? text
        : '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectGetElementFirst"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectGetElementFirst (arg)](#apidoc.element.n_.context.utility2.objectGetElementFirst)
- description and source-code
```javascript
objectGetElementFirst = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the first element of the arg
 */
</span>    var item;
    item = {};
    item.key = Object.keys(arg)[0];
    item.value = arg[item.key];
    return item;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectKeysTypeof"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectKeysTypeof (arg)](#apidoc.element.n_.context.utility2.objectKeysTypeof)
- description and source-code
```javascript
objectKeysTypeof = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a list of the arg's keys, sorted by item-type
 */
</span>    return Object.keys(arg).map(function (key) {
        return typeof arg[key] + ' ' + key;
    }).sort().join('\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectLiteralize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectLiteralize (arg)](#apidoc.element.n_.context.utility2.objectLiteralize)
- description and source-code
```javascript
objectLiteralize = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will traverse arg, and replace every encounter of the magical key '$[]'
 * with its object literal [key, value]
 */
</span>    local.objectTraverse(arg, function (element) {
        if (element && typeof element === 'object' && !Array.isArray(element)) {
            Object.keys(element).forEach(function (key) {
                if (key.indexOf('$[]') === 0) {
                    element[element[key][0]] = element[key][1];
                    delete element[key];
                }
            });
        }
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectSetDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectSetDefault (arg, defaults, depth)](#apidoc.element.n_.context.utility2.objectSetDefault)
- description and source-code
```javascript
objectSetDefault = function (arg, defaults, depth) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively set defaults for undefined-items in the arg
 */
</span>    arg = arg || {};
    defaults = defaults || {};
    Object.keys(defaults).forEach(function (key) {
        var arg2, defaults2;
        arg2 = arg[key];
        // handle misbehaving getter
        try {
            defaults2 = defaults[key];
        } catch (ignore) {
        }
        if (defaults2 === undefined) {
            return;
        }
        // init arg[key] to default value defaults[key]
        if (!arg2) {
            arg[key] = defaults2;
            return;
        }
        // if arg2 and defaults2 are both non-null and non-array objects,
        // then recurse with arg2 and defaults2
        if (depth > 1 &&
                // arg2 is a non-null and non-array object
                arg2 &&
                typeof arg2 === 'object' &&
                !Array.isArray(arg2) &&
                // defaults2 is a non-null and non-array object
                defaults2 &&
                typeof defaults2 === 'object' &&
                !Array.isArray(defaults2)) {
            // recurse
            local.objectSetDefault(arg2, defaults2, depth - 1);
        }
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectSetOverride"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectSetOverride (arg, overrides, depth, env)](#apidoc.element.n_.context.utility2.objectSetOverride)
- description and source-code
```javascript
objectSetOverride = function (arg, overrides, depth, env) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively set overrides for items in the arg
 */
</span>    arg = arg || {};
    env = env || (typeof process === 'object' && process.env) || {};
    overrides = overrides || {};
    Object.keys(overrides).forEach(function (key) {
        var arg2, overrides2;
        arg2 = arg[key];
        overrides2 = overrides[key];
        if (overrides2 === undefined) {
            return;
        }
        // if both arg2 and overrides2 are non-null and non-array objects,
        // then recurse with arg2 and overrides2
        if (depth > 1 &&
                // arg2 is a non-null and non-array object
                (arg2 &&
                typeof arg2 === 'object' &&
                !Array.isArray(arg2)) &&
                // overrides2 is a non-null and non-array object
                (overrides2 &&
                typeof overrides2 === 'object' &&
                !Array.isArray(overrides2))) {
            local.objectSetOverride(arg2, overrides2, depth - 1, env);
            return;
        }
        // else set arg[key] with overrides[key]
        arg[key] = arg === env
            // if arg is env, then overrides falsey value with empty string
            ? overrides2 || ''
            : overrides2;
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.objectTraverse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>objectTraverse (arg, onSelf, circularList)](#apidoc.element.n_.context.utility2.objectTraverse)
- description and source-code
```javascript
objectTraverse = function (arg, onSelf, circularList) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively traverse the arg,
 * and run onSelf with the arg's properties
 */
</span>    onSelf(arg);
    circularList = circularList || [];
    if (arg &&
            typeof arg === 'object' &&
            circularList.indexOf(arg) < 0) {
        circularList.push(arg);
        Object.keys(arg).forEach(function (key) {
            // recurse with arg[key]
            local.objectTraverse(arg[key], onSelf, circularList);
        });
    }
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onErrorDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorDefault (error)](#apidoc.element.n_.context.utility2.onErrorDefault)
- description and source-code
```javascript
onErrorDefault = function (error) {
<span class="apidocCodeCommentSpan">/*
 * this function will if error exists, then print error.stack to stderr
 */
</span>    if (error && !local.global.__coverage__) {
        console.error(error.stack);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onErrorJsonapi"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorJsonapi (onError)](#apidoc.element.n_.context.utility2.onErrorJsonapi)
- description and source-code
```javascript
onErrorJsonapi = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * http://jsonapi.org/format/#errors
 * http://jsonapi.org/format/#document-structure-resource-objects
 * this function will normalize the error and data to jsonapi format,
 * and pass them to onError
 */
</span>    return function (error, data, meta) {
        data = [error, data].map(function (data, ii) {
            // if no error occurred, then return
            if ((ii === 0 && !data) ||
                    // if data is already normalized, then return it
                    (data && data.meta && data.meta.isJsonapiResponse)) {
                return data;
            }
            // normalize data-list
            if (!Array.isArray(data)) {
                data = [data];
            }
            // normalize error-list to contain non-null objects
            if (ii === 0) {
                // normalize error-list to be non-empty
                if (!data.length) {
                    data.push(null);
                }
                data = data.map(function (element) {
                    if (!(element && typeof element === 'object')) {
                        element = { message: String(element) };
                    }
                    // normalize error-object to plain json-object
                    error = local.jsonCopy(element);
                    error.message = element.message;
                    error.stack = element.stack;
                    error.statusCode = Number(error.statusCode) || 500;
                    return error;
                });
                error = local.jsonCopy(data[0]);
                error.errors = data;
                return error;
            }
            return { data: data };
        });
        // init data.meta
        data.forEach(function (data, ii) {
            if (!data) {
                return;
            }
            data.meta = local.jsonCopy(meta || {});
            data.meta.isJsonapiResponse = true;
            if (ii === 0) {
                data.meta.errorsLength = (data.errors && data.errors.length) | 0;
            } else {
                data.meta.dataLength = (data.data && data.data.length) | 0;
            }
            data.meta.statusCode = Number(data.meta.statusCode) ||
                Number(data.statusCode) ||
                0;
        });
        onError(data[0], data[1]);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onErrorThrow"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorThrow (error)](#apidoc.element.n_.context.utility2.onErrorThrow)
- description and source-code
```javascript
onErrorThrow = function (error) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert no error occurred
 */
</span>    if (error) {
        throw error;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onErrorWithStack"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onErrorWithStack (onError)](#apidoc.element.n_.context.utility2.onErrorWithStack)
- description and source-code
```javascript
onErrorWithStack = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a new callback that will call onError,
 * and append the current stack to any error
 */
</span>    var stack;
    stack = new Error().stack.replace((/(.*?)\n.*?$/m), '$1');
    return function (error, data, meta) {
        if (error &&
                error !== local.errorDefault &&
                String(error.stack).indexOf(stack.split('\n')[2]) < 0) {
            // append the current stack to error.stack
            error.stack += '\n' + stack;
        }
        onError(error, data, meta);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onFileModifiedRestart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onFileModifiedRestart (file)](#apidoc.element.n_.context.utility2.onFileModifiedRestart)
- description and source-code
```javascript
onFileModifiedRestart = function (file) {
<span class="apidocCodeCommentSpan">/*
 * this function will watch the file, and if modified, then restart the process
 */
</span>    if (local.env.npm_config_mode_auto_restart &&
            local.fs.existsSync(file) &&
            local.fs.statSync(file).isFile()) {
        local.fs.watchFile(file, {
            interval: 1000,
            persistent: false
        }, function (stat2, stat1) {
            if (stat2.mtime > stat1.mtime) {
                console.error('file modified - ' + file);
                local.exit(77);
            }
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onNext"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onNext (options, onError)](#apidoc.element.n_.context.utility2.onNext)
- description and source-code
```javascript
onNext = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will wrap onError inside the recursive function options.onNext,
 * and append the current stack to any error
 */
</span>    options.onNext = local.onErrorWithStack(function (error, data, meta) {
        try {
            options.modeNext = error && !options.modeErrorIgnore
                ? Infinity
                : options.modeNext + 1;
            onError(error, data, meta);
        } catch (errorCaught) {
            // throw errorCaught to break infinite recursion-loop
            if (options.errorCaught) {
                throw options.errorCaught;
            }
            options.errorCaught = errorCaught;
            options.onNext(errorCaught, data, meta);
        }
    });
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onParallel"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onParallel (onError, onEach, onRetry)](#apidoc.element.n_.context.utility2.onParallel)
- description and source-code
```javascript
onParallel = function (onError, onEach, onRetry) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a function that will
 * 1. run async tasks in parallel
 * 2. if counter === 0 or error occurred, then call onError with error
 */
</span>    var onParallel;
    onError = local.onErrorWithStack(onError);
    onEach = onEach || local.nop;
    onRetry = onRetry || local.nop;
    onParallel = function (error, data) {
        if (onRetry(error, data)) {
            return;
        }
        // decrement counter
        onParallel.counter -= 1;
        // validate counter
        console.assert(onParallel.counter >= 0 || error || onParallel.error);
        // ensure onError is run only once
        if (onParallel.counter < 0) {
            return;
        }
        // handle error
        if (error) {
            onParallel.error = error;
            // ensure counter <= 0
            onParallel.counter = -Math.abs(onParallel.counter);
        }
        // call onError when done
        if (onParallel.counter <= 0) {
            onError(error, data);
            return;
        }
        onEach();
    };
    // init counter
    onParallel.counter = 0;
    // return callback
    return onParallel;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onParallelList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onParallelList (options, onEach, onError)](#apidoc.element.n_.context.utility2.onParallelList)
- description and source-code
```javascript
onParallelList = function (options, onEach, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. async-run onEach in parallel,
 *    with the given options.rateLimit and options.retryLimit
 * 2. call onError when done
 */
</span>    var ii, onEach2, onParallel;
    onEach2 = function () {
        while (ii + 1 < options.list.length && onParallel.counter < options.rateLimit) {
            ii += 1;
            onParallel.ii += 1;
            onParallel.remaining -= 1;
            onEach({
                element: options.list[ii],
                ii: ii,
                list: options.list,
                retry: 0
            }, onParallel);
        }
    };
    onParallel = local.onParallel(onError, onEach2, function (error, data) {
        if (error && data && data.retry < options.retryLimit) {
            local.onErrorDefault(error);
            data.retry += 1;
            setTimeout(function () {
                onParallel.counter -= 1;
                onEach(data, onParallel);
            }, 1000);
            return true;
        }
    });
    onParallel.counter += 1;
    ii = -1;
    onParallel.ii = -1;
    onParallel.remaining = options.list.length;
    options.rateLimit = Number(options.rateLimit) || 4;
    options.rateLimit = Math.max(options.rateLimit, 3);
    options.retryLimit = Number(options.retryLimit) || 2;
    onEach2();
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onReadyAfter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onReadyAfter (onError)](#apidoc.element.n_.context.utility2.onReadyAfter)
- description and source-code
```javascript
onReadyAfter = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will call onError when onReadyBefore.counter === 0
 */
</span>    local.onReadyBefore.counter += 1;
    local.taskCreate({ key: 'utility2.onReadyAfter' }, null, onError);
    local.onResetAfter(local.onReadyBefore);
    return onError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onReadyBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onReadyBefore (error, data)](#apidoc.element.n_.context.utility2.onReadyBefore)
- description and source-code
```javascript
onReadyBefore = function (error, data) {
    if (onRetry(error, data)) {
        return;
    }
    // decrement counter
    onParallel.counter -= 1;
    // validate counter
    console.assert(onParallel.counter >= 0 || error || onParallel.error);
    // ensure onError is run only once
    if (onParallel.counter < 0) {
        return;
    }
    // handle error
    if (error) {
        onParallel.error = error;
        // ensure counter <= 0
        onParallel.counter = -Math.abs(onParallel.counter);
    }
    // call onError when done
    if (onParallel.counter <= 0) {
        onError(error, data);
        return;
    }
    onEach();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onResetAfter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onResetAfter (onError)](#apidoc.element.n_.context.utility2.onResetAfter)
- description and source-code
```javascript
onResetAfter = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will call onError when onResetBefore.counter === 0
 */
</span>    local.onResetBefore.counter += 1;
    // visual notification - onResetAfter
    local.ajaxProgressUpdate();
    local.taskCreate({ key: 'utility2.onResetAfter' }, null, onError);
    setTimeout(local.onResetBefore);
    return onError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onResetBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onResetBefore (error, data)](#apidoc.element.n_.context.utility2.onResetBefore)
- description and source-code
```javascript
onResetBefore = function (error, data) {
    if (onRetry(error, data)) {
        return;
    }
    // decrement counter
    onParallel.counter -= 1;
    // validate counter
    console.assert(onParallel.counter >= 0 || error || onParallel.error);
    // ensure onError is run only once
    if (onParallel.counter < 0) {
        return;
    }
    // handle error
    if (error) {
        onParallel.error = error;
        // ensure counter <= 0
        onParallel.counter = -Math.abs(onParallel.counter);
    }
    // call onError when done
    if (onParallel.counter <= 0) {
        onError(error, data);
        return;
    }
    onEach();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.onTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>onTimeout (onError, timeout, message)](#apidoc.element.n_.context.utility2.onTimeout)
- description and source-code
```javascript
onTimeout = function (onError, timeout, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a timeout-error-handler,
 * that will append the current stack to any error encountered
 */
</span>    onError = local.onErrorWithStack(onError);
    // create timeout timer
    return setTimeout(function () {
        onError(new Error('onTimeout - timeout-error - ' +
            timeout + ' ms - ' + (typeof message === 'function'
            ? message()
            : message)));
    // coerce to finite integer
    }, timeout | 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.parse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>parse (e, t, n)](#apidoc.element.n_.context.utility2.parse)
- description and source-code
```javascript
function parse(e, t, n){function i(e,t){return is_token(r.token,e,t)}function s(){return r.peeked||
(r.peeked=r.input())}function o(){return r.prev=r.token,r.peeked?(r.token=r.peeked
,r.peeked=null):r.token=r.input(),r.in_directives=r.in_directives&&(r.token.type=="string"||
i("punc",";")),r.token}function u(){return r.prev}function a(e,t,n,i){var s=r.input
.context();js_error(e,t!=null?t:s.tokline,n!=null?n:s.tokcol,i!=null?i:s.tokpos)
}function f(e,t){a(t,e.line,e.col)}function l(e){e==null&&(e=r.token),f(e,"Unexpected token: "+
e.type+" ("+e.value+")")}function c(e,t){if(i(e,t))return o();f(r.token,"Unexpected token "+
r.token.type+", expected "+e)}function h(e){return c("punc",e)}function p(){return!
t&&(r.token.nlb||i("eof")||i("punc","}"))}function d(){i("punc",";")?o():p()||l(
)}function v(){return slice(arguments)}function m(){h("(");var e=K();return h(")"
),e}function g(e,t,n){return e instanceof NodeWithToken?e:new NodeWithToken(e,t,
n)}function y(e){return n?function(){var t=r.token,n=e.apply(this,arguments);return n
[0]=g(n[0],t,u()),n}:e}function w(e){r.labels.push(e);var n=r.token,i=b();return t&&!
HOP(STATEMENTS_WITH_LABELS,i[0])&&l(n),r.labels.pop(),v("label",e,i)}function E(
){return v("stat",prog1(K,d))}function S(e){var t;return p()||(t=i("name")?r.token
.value:null),t!=null?(o(),member(t,r.labels)||a("Label "+t+" without matching loop or statement"
)):r.in_loop==0&&a(e+" not inside a loop or switch"),d(),v(e,t)}function x(){h("("
);var e=null;if(!i("punc",";")){e=i("keyword","var")?(o(),_(!0)):K(!0,!0);if(i("operator"
,"in"))return e[0]=="var"&&e[1].length>1&&a("Only one variable declaration allowed in for..in loop"
),N(e)}return T(e)}function T(e){h(";");var t=i("punc",";")?null:K();h(";");var n=
i("punc",")")?null:K();return h(")"),v("for",e,t,n,Q(b))}function N(e){var t=e[0
]=="var"?v("name",e[1][0]):e;o();var n=K();return h(")"),v("for-in",e,t,n,Q(b))}
function k(){var e=m(),t=b(),n;return i("keyword","else")&&(o(),n=b()),v("if",e,
t,n)}function L(){h("{");var e=[];while(!i("punc","}"))i("eof")&&l(),e.push(b())
;return o(),e}function O(){var e=L(),t,n;if(i("keyword","catch")){o(),h("("),i("name"
)||a("Name expected");var s=r.token.value;o(),h(")"),t=[s,L()]}return i("keyword"
,"finally")&&(o(),n=L()),!t&&!n&&a("Missing catch/finally blocks"),v("try",e,t,n
)}function M(e){var t=[];for(;;){i("name")||l();var n=r.token.value;o(),i("operator"
,"=")?(o(),t.push([n,K(!1,e)])):t.push([n]);if(!i("punc",","))break;o()}return t
}function _(e){return v("var",M(e))}function D(){return v("const",M())}function P
(){var e=H(!1),t;return i("punc","(")?(o(),t=B(")")):t=[],R(v("new",e,t),!0)}function B
(e,t,n){var r=!0,s=[];while(!i("punc",e)){r?r=!1:h(",");if(t&&i("punc",e))break;
i("punc",",")&&n?s.push(["atom","undefined"]):s.push(K(!1))}return o(),s}function j
(){return v("array",B("]",!t,!0))}function F(){var e=!0,n=[];while(!i("punc","}"
)){e?e=!1:h(",");if(!t&&i("punc","}"))break;var s=r.token.type,u=I();s!="name"||
u!="get"&&u!="set"||!!i("punc",":")?(h(":"),n.push([u,K(!1)])):n.push([q(),C(!1)
,u])}return o(),v("object",n)}function I(){switch(r.token.type){case"num":case"string"
:return prog1(r.token.value,o)}return q()}function q(){switch(r.token.type){case"name"
:case"operator":case"keyword":case"atom":return prog1(r.token.value,o);default:l
()}}function R(e,t){return i("punc",".")?(o(),R(v("dot",e,q()),t)):i("punc","[")?
(o(),R(v("sub",e,prog1(K,curry(h,"]"))),t)):t&&i("punc","(")?(o(),R(v("call",e,B
(")")),!0)):e}function U(e){if(i("operator")&&HOP(UNARY_PREFIX,r.token.value))return z
("unary-prefix",prog1(r.token.value,o),U(e));var t=H(e);while(i("operator")&&HOP
(UNARY_POSTFIX,r.token.value)&&!r.token.nlb)t=z("unary-postfix",r.token.value,t)
,o();return t}function z(e,t,n){return(t=="++"||t=="--")&&!$(n)&&a("Invalid use of "+
t+" operator"),v(e,t,n)}function W(e,t,n){var s=i("operator")?r.token.value:null
;s&&s=="in"&&n&&(s=null);var u=s!=null?PRECEDENCE[s]:null;if(u!=null&&u>t){o();var a=
W(U(!0),u,n);return W(v("binary",s,e,a),t,n)}return e}function X(e){return W(U(!0
),0,e)}function V(e){var t=X(e); ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.processSpawnWithTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>processSpawnWithTimeout ()](#apidoc.element.n_.context.utility2.processSpawnWithTimeout)
- description and source-code
```javascript
processSpawnWithTimeout = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will run like child_process.spawn,
 * but with auto-timeout after timeoutDefault milliseconds
 */
</span>    var childProcess;
    // spawn childProcess
    childProcess = local.child_process.spawn.apply(local.child_process, arguments)
        .on('exit', function () {
            // try to kill timerTimeout childProcess
            local.tryCatchOnError(function () {
                process.kill(childProcess.timerTimeout.pid);
            }, local.nop);
        });
    // init failsafe timerTimeout
    childProcess.timerTimeout = local.child_process.spawn('/bin/sh', ['-c', 'sleep ' +
        // coerce to finite integer
        (((0.001 * local.timeoutDefault) | 0) +
        // add 2 second delay to failsafe timerTimeout
        2) + '; kill -9 ' + childProcess.pid + ' 2>/dev/null'], { stdio: 'ignore' });
    return childProcess;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.profile"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>profile (fnc, onError)](#apidoc.element.n_.context.utility2.profile)
- description and source-code
```javascript
profile = function (fnc, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will profile the async fnc in milliseconds with the callback onError
 */
</span>    var timeStart;
    timeStart = Date.now();
    // run async fnc
    fnc(function (error) {
        // call onError with difference in milliseconds between Date.now() and timeStart
        onError(error, Date.now() - timeStart);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.profileSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>profileSync (fnc)](#apidoc.element.n_.context.utility2.profileSync)
- description and source-code
```javascript
profileSync = function (fnc) {
<span class="apidocCodeCommentSpan">/*
 * this function will profile the sync fnc in milliseconds
 */
</span>    var timeStart;
    timeStart = Date.now();
    // run sync fnc
    fnc();
    // return difference in milliseconds between Date.now() and timeStart
    return Date.now() - timeStart;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.replStart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>replStart ()](#apidoc.element.n_.context.utility2.replStart)
- description and source-code
```javascript
replStart = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will start the repl-debugger
 */
</span>    /*jslint evil: true*/
    var self;
    if (global.utility2_serverRepl1) {
        return;
    }
    // start replServer
    self = global.utility2_serverRepl1 = require('repl').start({ useGlobal: true });
    self.nop = function () {
    /*
     * this function will do nothing
     */
        return;
    };
    self.onError = function (error) {
    /*
     * this function will debug any repl-error
     */
        // debug error
        global.utility2_debugReplError = error;
        console.error(error.stack);
    };
    // save repl eval function
    self.evalDefault = self.eval;
    // hook custom repl eval function
    self.eval = function (script, context, file, onError) {
        var match, onError2;
        match = (/^(\S+)(.*?)\n/).exec(script);
        onError2 = function (error, data) {
            // debug error
            global.utility2_debugReplError = error || global.utility2_debugReplError;
            onError(error, data);
        };
        switch (match && match[1]) {
        // syntax sugar to run async shell command
        case '$':
            switch (match[2]) {
            // syntax sugar to run git diff
            case ' git diff':
                match[2] = ' git diff --color | cat';
                break;
            // syntax sugar to run git log
            case ' git log':
                match[2] = ' git log -n 4 | cat';
                break;
            }
            // run async shell command
            require('child_process').spawn(
                '/bin/sh',
                ['-c', match[2]],
                { stdio: ['ignore', 1, 2] }
            )
                // on shell exit, print return prompt
                .on('exit', function (exitCode) {
                    console.error('exit-code ' + exitCode);
                    self.evalDefault(
                        '\n',
                        context,
                        file,
                        onError2
                    );
                });
            script = '\n';
            break;
        // syntax sugar to grep current dir
        case 'grep':
            // run async shell command
            require('child_process').spawn(
                '/bin/sh',
                ['-c', 'find . -type f | grep -v ' +
/* jslint-ignore-begin */
'"\
/\\.\\|.*\\(\\b\\|_\\)\\(\\.\\d\\|\
archive\\|artifact\\|\
bower_component\\|build\\|\
coverage\\|\
doc\\|\
external\\|\
fixture\\|\
git_module\\|\
jquery\\|\
log\\|\
min\\|mock\\|\
node_module\\|\
rollup\\|\
swp\\|\
tmp\\|\
vendor\\)\\(\\b\\|[_s]\\)\
" ' +
/* jslint-ignore-end */
                    '| tr "\\n" "\\000" | xargs -0 grep -in "' +
                    match[2].trim() + '"'],
                { stdio: ['ignore', 1, 2] }
            )
                // on shell exit, print return prompt
                .on('exit', function (exitCode) {
                    console.error('exit-code ' + exitCode);
                    self.evalDefault(
                        '\n',
                        context,
                        file,
                        onError2
                    );
                });
            script = '\n';
            break;
        // syntax sugar to list object's keys, sorted by item-type
        case 'keys':
            script = 'console.error(Object.keys(' + match[2] +
                ').map(function (key) {' +
                'return typeof ' + match[2] + '[key] + " " + key + "\\n";' +
                '}).sort().join("") + Object.keys(' + match[2] + ').length)\n';
            break;
        // syntax sugar to print stringified arg
        case 'print':
            script = 'console.error(String(' + match[2] + '))\n';
            break;
        }
        // eval the script
        self.evalDefault(script, context, file, onError2);
    };
    self.socket = { end: self.nop, on: self.nop, write: self.nop };
    // init process.stdout
    process.stdout._writeDefault = process.stdout._writeDefault ||
        process.stdout._write;
    process.stdout._write = function (chunk, e ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.require"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>require (path)](#apidoc.element.n_.context.utility2.require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.requireExampleJsFromReadme"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>requireExampleJsFromReadme ()](#apidoc.element.n_.context.utility2.requireExampleJsFromReadme)
- description and source-code
```javascript
requireExampleJsFromReadme = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will require and export example.js embedded in README.md
 */
</span>    var module, script, tmp;
    // start the repl-debugger
    local.replStart();
    // debug dir
    [__dirname, process.cwd()].forEach(function (dir) {
        local.fs.readdirSync(dir).forEach(function (file) {
            if ((/\brollup\b/).test(file)) {
                return;
            }
            file = dir + '/' + file;
            // if the file is modified, then restart the process
            local.onFileModifiedRestart(file);
            switch (local.path.extname(file)) {
            case '.css':
            case '.html':
            case '.js':
            case '.json':
                // jslint file
                local.jslintAndPrintConditional(
                    local.tryCatchReadFile(file, 'utf8'),
                    file
                );
                break;
            }
        });
    });
    if (local.global.utility2_rollup || local.env.npm_config_mode_start) {
        // init assets
        local.assetsDict['/'] = local.assetsDict['/index.html'] = local.templateRender(
            // uncomment utility2-comment
            local.assetsDict['/assets.index.template.html'].replace(
                (/<!-- utility2-comment\b([\S\s]+?)\butility2-comment -->/g),
                '$1'
            ),
            { env: local.env, isRollup: true }
        );
        local.assetsDict['/assets.example.js'] =
            local.assetsDict['/assets.example.template.js'];
        local.assetsDict['/assets.app.js'] =
            local.fs.readFileSync(__filename, 'utf8').replace((/^#!/), '//');
        // coverage-hack
        local.nop(local.env.npm_config_mode_start && (function () {
            local.assetsDict['/assets.app.js'] =
                local.assetsDict['/assets.utility2.rollup.begin.js'];
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.fs.readFileSync(__filename, 'utf8').replace((/^#!/), '//');
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.assetsDict['/assets.example.js'];
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.assetsDict['/assets.test.js'];
            local.global.local = local;
        }()));
        local[local.env.npm_package_nameAlias] = local;
        return local;
    }
    // init file $npm_package_main
    tmp = process.cwd() + '/' + local.env.npm_package_main;
    global.utility2_moduleExports = require(tmp);
    local.assetsDict['/assets.' + local.env.npm_package_nameAlias + '.js'] =
        local.istanbulInstrumentInPackage(
            local.fs.readFileSync(tmp, 'utf8').replace((/^#!/), '//'),
            tmp
        );
    global.utility2_moduleExports.global = global;
    // read script from README.md
    script = local.templateRenderJslintLite(
        local.assetsDict['/assets.example.template.js'],
        {}
    );
    // coverage-hack
    local.nop(local.env.npm_package_readmeParse && (function () {
        local.fs.readFileSync('README.md', 'utf8').replace(
            (/'''\w*?(\n[\W\s]*?example\.js[\n\"][\S\s]+?)\n'''/),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                script = text.slice(0, ii).replace((/.+/g), '') + match1;
            }
        );
    }()));
    script = script
        // alias require($npm_package_name) to utility2_moduleExports;
        .replace(
            "require('" + local.env.npm_package_name + "')",
            'global.utility2_moduleExports'
        )
        .replace(
            "require('" + local.env.npm_package_nameOriginal + "')",
            'global.utility2_moduleExports'
        );
    // init example.js
    tmp = process.cwd() + '/example.js';
    // jslint script
    local.jslintAndPrintConditional(script, tmp);
    // cover script
    script = local.istanbulInstrumentInPackage(script, tmp);
    // init module
    module = require.cache[tmp] = new local.Module(tmp);
    // load script into module
    mo ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.schemaNormalizeAndCopy"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>schemaNormalizeAndCopy (schema)](#apidoc.element.n_.context.utility2.schemaNormalizeAndCopy)
- description and source-code
```javascript
schemaNormalizeAndCopy = function (schema) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a normalized copy the schema
 */
</span>    var tmp;
    // dereference $ref
    if (schema.$ref) {
        [local.swaggerJson, local.swaggerSchemaJson].some(function (options) {
            local.tryCatchOnError(function () {
                schema.$ref.replace(
                    (/#\/(.*?)\/(.*?)$/),
                    function (match0, match1, match2) {
                        // jslint-hack - nop
                        local.nop(match0);
                        tmp = options[match1][match2];
                    }
                );
            }, local.nop);
            return tmp;
        });
        // validate schema
        local.assert(tmp, schema.$ref);
        // recurse
        schema = local.schemaNormalizeAndCopy(tmp);
    }
    // inherit allOf
    if (schema.allOf) {
        tmp = local.jsonCopy(schema);
        delete tmp.allOf;
        schema.allOf.reverse().forEach(function (element) {
            // recurse
            local.objectSetDefault(tmp, local.schemaNormalizeAndCopy(element), 2);
        });
        schema = tmp;
    }
    schema = local.jsonCopy(schema);
    if (schema.type === 'object') {
        schema.properties = local.normalizeDict(schema.properties);
    }
    return schema;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.serverRespondDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondDefault (request, response, statusCode, error)](#apidoc.element.n_.context.utility2.serverRespondDefault)
- description and source-code
```javascript
serverRespondDefault = function (request, response, statusCode, error) {
<span class="apidocCodeCommentSpan">/*
 * this function will respond with a default message,
 * or error.stack for the given statusCode
 */
</span>    // init statusCode and contentType
    local.serverRespondHeadSet(
        request,
        response,
        statusCode,
        { 'Content-Type': 'text/plain; charset=utf-8' }
    );
    if (error) {
        // debug statusCode / method / url
        local.errorMessagePrepend(
            error,
            response.statusCode + ' ' + request.method + ' ' + request.url + '\n'
        );
        // print error.stack to stderr
        local.onErrorDefault(error);
        // end response with error.stack
        response.end(error.stack);
        return;
    }
    // end response with default statusCode message
    response.end(
        statusCode + ' ' + local.http.STATUS_CODES[statusCode]
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.serverRespondEcho"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondEcho (request, response)](#apidoc.element.n_.context.utility2.serverRespondEcho)
- description and source-code
```javascript
serverRespondEcho = function (request, response) {
<span class="apidocCodeCommentSpan">/*
 * this function will respond with debug info
 */
</span>    response.write(request.method + ' ' + request.url +
        ' HTTP/' + request.httpVersion + '\r\n' +
        Object.keys(request.headers).map(function (key) {
            return key + ': ' + request.headers[key] + '\r\n';
        }).join('') + '\r\n');
    request.pipe(response);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.serverRespondHeadSet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondHeadSet (request, response, statusCode, headers)](#apidoc.element.n_.context.utility2.serverRespondHeadSet)
- description and source-code
```javascript
serverRespondHeadSet = function (request, response, statusCode, headers) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the response object's statusCode / headers
 */
</span>    // jslint-hack
    local.nop(request);
    if (response.headersSent) {
        return;
    }
    // init response.statusCode
    if (Number(statusCode)) {
        response.statusCode = Number(statusCode);
    }
    Object.keys(headers).forEach(function (key) {
        if (headers[key]) {
            response.setHeader(key, headers[key]);
        }
    });
    return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.serverRespondJsonapi"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondJsonapi (request, response, error, data, meta)](#apidoc.element.n_.context.utility2.serverRespondJsonapi)
- description and source-code
```javascript
serverRespondJsonapi = function (request, response, error, data, meta) {
<span class="apidocCodeCommentSpan">/*
 * http://jsonapi.org/format/#errors
 * http://jsonapi.org/format/#document-structure-resource-objects
 * this function will respond in jsonapi format
 */
</span>    local.onErrorJsonapi(function (error, data) {
        local.serverRespondHeadSet(request, response, error && error.statusCode, {
            'Content-Type': 'application/json; charset=UTF-8'
        });
        if (error) {
            // debug statusCode / method / url
            local.errorMessagePrepend(error, response.statusCode + ' ' +
                request.method + ' ' + request.url + '\n');
            // print error.stack to stderr
            local.onErrorDefault(error);
        }
        data = error || data;
        data.meta.statusCode = response.statusCode =
            data.meta.statusCode || response.statusCode;
        response.end(JSON.stringify(data));
    })(error, data, meta);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.serverRespondTimeoutDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>serverRespondTimeoutDefault (request, response, timeout)](#apidoc.element.n_.context.utility2.serverRespondTimeoutDefault)
- description and source-code
```javascript
serverRespondTimeoutDefault = function (request, response, timeout) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a timeout-error-handler for the server-request
 */
</span>    request.onTimeout = request.onTimeout || function (error) {
        local.serverRespondDefault(request, response, 500, error);
        setTimeout(function () {
            // cleanup request and response
            local.streamListCleanup([request, response]);
        }, 1000);
    };
    request.timerTimeout = local.onTimeout(
        request.onTimeout,
        timeout || local.timeoutDefault,
        'server ' + request.method + ' ' + request.url
    );
    response.on('finish', function () {
        // cleanup timerTimeout
        clearTimeout(request.timerTimeout);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.setTimeoutOnError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>setTimeoutOnError (onError, error, data)](#apidoc.element.n_.context.utility2.setTimeoutOnError)
- description and source-code
```javascript
setTimeoutOnError = function (onError, error, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will async-call onError
 */
</span>    if (typeof onError === 'function') {
        setTimeout(function () {
            onError(error, data);
        });
    }
    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.set_logger"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>set_logger (e)](#apidoc.element.n_.context.utility2.set_logger)
- description and source-code
```javascript
set_logger = function (e){warn=e}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.sjclHashScryptCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashScryptCreate (password, options)](#apidoc.element.n_.context.utility2.sjclHashScryptCreate)
- description and source-code
```javascript
sjclHashScryptCreate = function (password, options) {
<span class="apidocCodeCommentSpan">/*
 * https://github.com/wg/scrypt
 * this function will create a scrypt-hash of the password
 * with the given options (default = $s0$10801)
 * e.g. $s0$e0801$epIxT/h6HbbwHaehFnh/bw==$7H0vsXlY8UxxyW/BWx/9GuY7jEvGjT71GFd6O4SZND0=
 */
</span>    // init options
    options = (options || '$s0$10801').split('$');
    // init salt
    if (!options[3]) {
        options[3] = local.sjcl.codec.base64.fromBits(
            local.sjcl.random.randomWords(4, 0)
        );
    }
    // init hash
    options[4] = local.sjcl.codec.base64.fromBits(
        local.sjcl.misc.scrypt(
            password || '',
            local.sjcl.codec.base64.toBits(options[3]),
            Math.pow(2, parseInt(options[2].slice(0, 1), 16)),
            parseInt(options[2].slice(1, 2), 16),
            parseInt(options[2].slice(3, 4), 16)
        )
    );
    return options.slice(0, 5).join('$');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.sjclHashScryptValidate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashScryptValidate (password, hash)](#apidoc.element.n_.context.utility2.sjclHashScryptValidate)
- description and source-code
```javascript
sjclHashScryptValidate = function (password, hash) {
<span class="apidocCodeCommentSpan">/*
 * https://github.com/wg/scrypt
 * this function will validate the password against the scrypt-hash
 */
</span>    return local.sjclHashScryptCreate(password, hash) === hash;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.sjclHashSha256Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHashSha256Create (data)](#apidoc.element.n_.context.utility2.sjclHashSha256Create)
- description and source-code
```javascript
sjclHashSha256Create = function (data) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a base64-encoded sha-256 hash of the string data
 */
</span>    return local.sjcl.codec.base64.fromBits(local.sjcl.hash.sha256.hash(data));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.sjclHmacSha256Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>sjclHmacSha256Create (key, data)](#apidoc.element.n_.context.utility2.sjclHmacSha256Create)
- description and source-code
```javascript
sjclHmacSha256Create = function (key, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a base64-encoded sha-256 hmac
 * from the base64-encoded key and string data
 */
</span>    return local.sjcl.codec.base64.fromBits(
        (new local.sjcl.misc.hmac(
            local.sjcl.codec.base64.toBits(key),
            local.sjcl.hash.sha256
        )).mac(local.sjcl.codec.utf8String.toBits(data))
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.slice"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>slice (e, t)](#apidoc.element.n_.context.utility2.slice)
- description and source-code
```javascript
function slice(e, t){return Array.prototype.slice
.call(e,t||0)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.sortCompare"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>sortCompare (aa, bb)](#apidoc.element.n_.context.utility2.sortCompare)
- description and source-code
```javascript
sortCompare = function (aa, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will compare aa vs bb and return:
 * -1 if aa < bb
 *  0 if aa === bb
 *  1 if aa > bb
 * the priority for comparing different typeof's is:
 * null < boolean < number < string < object < undefined
 */
</span>    var typeof1, typeof2;
    if (aa === bb) {
        return 0;
    }
    if (aa === null) {
        return -1;
    }
    if (bb === null) {
        return 1;
    }
    typeof1 = typeof aa;
    typeof2 = typeof bb;
    if (typeof1 === typeof2) {
        return typeof1 === 'object'
            ? 0
            : aa > bb
            ? 1
            : -1;
    }
    if (typeof1 === 'boolean') {
        return -1;
    }
    if (typeof2 === 'boolean') {
        return 1;
    }
    if (typeof1 === 'number') {
        return -1;
    }
    if (typeof2 === 'number') {
        return 1;
    }
    if (typeof1 === 'string') {
        return -1;
    }
    if (typeof2 === 'string') {
        return 1;
    }
    return 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.split_lines"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>split_lines (e, t)](#apidoc.element.n_.context.utility2.split_lines)
- description and source-code
```javascript
function split_lines(e, t){var n=[0];return jsp
.parse(function(){function o(e){return e.pos-i}function u(e){i=e.pos,n.push(i)}function a
(){var e=r.apply(this,arguments);e:{if(s&&s.type=="keyword")break e;if(o(e)>t)switch(
e.type){case"keyword":case"atom":case"name":case"punc":u(e);break e}}return s=e,
e}var r=jsp.tokenizer(e),i=0,s;return a.context=function(){return r.context.apply
(this,arguments)},a}()),n.map(function(t,r){return e.substring(t,n[r+1]||e.length
)}).join("\n")}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageClear"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageClear (onError)](#apidoc.element.n_.context.utility2.storageClear)
- description and source-code
```javascript
storageClear = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will clear storage
 */
</span>    defer({ action: 'clear' }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageDefer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageDefer (options, onError)](#apidoc.element.n_.context.utility2.storageDefer)
- description and source-code
```javascript
storageDefer = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will defer options.action until storage is ready
 */
</span>    var data, done, objectStore, onError2, request, tmp;
    onError = onError || function (error) {
        // validate no error occurred
        console.assert(!error, error);
    };
    if (!storage) {
        deferList.push(function () {
            defer(options, onError);
        });
        init();
        return;
    }
    switch (modeJs) {
    case 'browser':
        onError2 = function () {
            /* istanbul ignore next */
            if (done) {
                return;
            }
            done = true;
            onError(
                request && (request.error || request.transaction.error),
                data || request.result || ''
            );
        };
        switch (options.action) {
        case 'clear':
        case 'removeItem':
        case 'setItem':
            objectStore = storage
                .transaction(storageDir, 'readwrite')
                .objectStore(storageDir);
            break;
        default:
            objectStore = storage
                .transaction(storageDir, 'readonly')
                .objectStore(storageDir);
        }
        switch (options.action) {
        case 'clear':
            request = objectStore.clear();
            break;
        case 'getItem':
            request = objectStore.get(String(options.key));
            break;
        case 'keys':
            data = [];
            request = objectStore.openCursor();
            request.onsuccess = function () {
                if (!request.result) {
                    onError2();
                    return;
                }
                data.push(request.result.key);
                request.result.continue();
            };
            break;
        case 'length':
            request = objectStore.count();
            break;
        case 'removeItem':
            request = objectStore.delete(String(options.key));
            break;
        case 'setItem':
            request = objectStore.put(options.value, String(options.key));
            break;
        }
        ['onabort', 'onerror', 'onsuccess'].forEach(function (handler) {
            request[handler] = request[handler] || onError2;
        });
        // debug request
        local._debugStorageRequest = request;
        break;
    case 'node':
        switch (options.action) {
        case 'clear':
            child_process.spawnSync(
                'sh',
                ['-c', 'rm -f ' + storage + '/*'],
                { stdio: ['ignore', 1, 2] }
            );
            setTimeout(onError);
            break;
        case 'getItem':
            fs.readFile(
                storage + '/' + encodeURIComponent(String(options.key)),
                'utf8',
                // ignore error
                function (error, data) {
                    onError(error && null, data || '');
                }
            );
            break;
        case 'keys':
            fs.readdir(storage, function (error, data) {
                onError(error, data && data.map(decodeURIComponent));
            });
            break;
        case 'length':
            fs.readdir(storage, function (error, data) {
                onError(error, data && data.length);
            });
            break;
        case 'removeItem':
            fs.unlink(
                storage + '/' + encodeURIComponent(String(options.key)),
                // ignore error
                function () {
                    onError();
                }
            );
            break;
        case 'setItem':
            tmp = os.tmpdir() + '/' + Date.now() + Math.random();
            // save to tmp
            fs.writeFile(tmp, options.value, function (error) {
                // validate no error occurred
                console.assert(!error, error);
                // rename tmp to key
                fs.rename(
                    tmp,
                    storage + '/' + encodeURIComponent(String(options.key)),
                    onError
                ); ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageGetItem"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageGetItem (key, onError)](#apidoc.element.n_.context.utility2.storageGetItem)
- description and source-code
```javascript
storageGetItem = function (key, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the item with the given key from storage
 */
</span>    defer({ action: 'getItem', key: key }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageInit ()](#apidoc.element.n_.context.utility2.storageInit)
- description and source-code
```javascript
storageInit = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will init storage
 */
</span>    var onError, request;
    onError = function (error) {
        // validate no error occurred
        console.assert(!error, error);
        if (modeJs === 'browser') {
            storage = window[storageDir];
        }
        while (deferList.length) {
            deferList.shift()();
        }
    };
    if (modeJs === 'browser') {
        storage = window[storageDir];
    }
    if (storage) {
        onError();
        return;
    }
    switch (modeJs) {
    case 'browser':
        // init indexedDB
        try {
            request = window.indexedDB.open(storageDir);
            // debug request
            local._debugStorageRequestIndexedDB = request;
            request.onerror = onError;
            request.onsuccess = function () {
                window[storageDir] = request.result;
                onError();
            };
            request.onupgradeneeded = function () {
                if (!request.result.objectStoreNames.contains(storageDir)) {
                    request.result.createObjectStore(storageDir);
                }
            };
        } catch (ignore) {
        }
        break;
    case 'node':
        // mkdirp storage
        storage = storageDir;
        child_process.spawnSync(
            'mkdir',
            ['-p', storage],
            { stdio: ['ignore', 1, 2] }
        );
        onError();
        break;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageKeys"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageKeys (onError)](#apidoc.element.n_.context.utility2.storageKeys)
- description and source-code
```javascript
storageKeys = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get all the keys in storage
 */
</span>    defer({ action: 'keys' }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageLength"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageLength (onError)](#apidoc.element.n_.context.utility2.storageLength)
- description and source-code
```javascript
storageLength = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the number of items in storage
 */
</span>    defer({ action: 'length' }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageRemoveItem"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageRemoveItem (key, onError)](#apidoc.element.n_.context.utility2.storageRemoveItem)
- description and source-code
```javascript
storageRemoveItem = function (key, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the item with the given key from storage
 */
</span>    defer({ action: 'removeItem', key: key }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.storageSetItem"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>storageSetItem (key, value, onError)](#apidoc.element.n_.context.utility2.storageSetItem)
- description and source-code
```javascript
storageSetItem = function (key, value, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the item with the given key and value to storage
 */
</span>    defer({ action: 'setItem', key: key, value: value }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.streamListCleanup"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>streamListCleanup (streamList)](#apidoc.element.n_.context.utility2.streamListCleanup)
- description and source-code
```javascript
streamListCleanup = function (streamList) {
<span class="apidocCodeCommentSpan">/*
 * this function will end or destroy the streams in streamList
 */
</span>    streamList.forEach(function (stream) {
        // try to end the stream
        local.tryCatchOnError(function () {
            stream.end();
        }, function () {
            // if error, then try to destroy the stream
            local.tryCatchOnError(function () {
                stream.destroy();
            }, local.nop);
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.streamReadAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>streamReadAll (stream, onError)](#apidoc.element.n_.context.utility2.streamReadAll)
- description and source-code
```javascript
streamReadAll = function (stream, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will concat data from the stream,
 * and pass it to onError when done reading
 */
</span>    var chunkList;
    chunkList = [];
    // read data from the stream
    stream
        // on data event, push the buffer chunk to chunkList
        .on('data', function (chunk) {
            chunkList.push(chunk);
        })
        // on end event, pass concatenated read buffer to onError
        .on('end', function () {
            onError(null, local.modeJs === 'browser'
                ? chunkList[0]
                : local.bufferConcat(chunkList));
        })
        // on error event, pass error to onError
        .on('error', onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.stringHtmlSafe"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>stringHtmlSafe (text)](#apidoc.element.n_.context.utility2.stringHtmlSafe)
- description and source-code
```javascript
stringHtmlSafe = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will make the text html-safe
 */
</span>    // new RegExp('[' + '"&\'<>'.split('').sort().join('') + ']', 'g')
    return text.replace((/["&'<>]/g), function (match0) {
        return '&#x' + match0.charCodeAt(0).toString(16) + ';';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.taskCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>taskCreate (options, onTask, onError)](#apidoc.element.n_.context.utility2.taskCreate)
- description and source-code
```javascript
taskCreate = function (options, onTask, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create the task onTask named options.key, if it does not exist,
 * and push onError to its onErrorList
 */
</span>    var task;
    // init task
    task = local.taskOnTaskDict[options.key] = local.taskOnTaskDict[options.key] ||
        { onErrorList: [] };
    // push callback onError to the task
    if (onError) {
        onError = local.onErrorWithStack(onError);
        task.onErrorList.push(onError);
    }
    // if task exists, then return it
    if (!onTask || task.onTask) {
        return task;
    }
    task.onDone = function () {
        // if already done, then do nothing
        if (task.done) {
            return;
        }
        task.done = true;
        // cleanup timerTimeout
        clearTimeout(task.timerTimeout);
        // cleanup task
        delete local.taskOnTaskDict[options.key];
        // preserve error.message and error.stack
        task.result = JSON.stringify(Array.from(arguments)
            .map(function (element) {
                if (element && element.stack) {
                    element = local.objectSetDefault(local.jsonCopy(element), {
                        message: element.message,
                        name: element.name,
                        stack: element.stack
                    });
                }
                return element;
            }));
        // pass result to callbacks in onErrorList
        task.onErrorList.forEach(function (onError) {
            onError.apply(null, JSON.parse(task.result));
        });
    };
    // init timerTimeout
    task.timerTimeout = local.onTimeout(
        task.onDone,
        options.timeout || local.timeoutDefault,
        'taskCreate ' + options.key
    );
    task.onTask = onTask;
    // run onTask
    task.onTask(task.onDone);
    return task;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.taskCreateCached"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>taskCreateCached (options, onTask, onError)](#apidoc.element.n_.context.utility2.taskCreateCached)
- description and source-code
```javascript
taskCreateCached = function (options, onTask, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. if cache-hit, then call onError with cacheValue
 * 2. run onTask in background
 * 3. save onTask's result to cache
 * 4. if cache-miss, then call onError with onTask's result
 */
</span>    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        //  1. if cache-hit, then call onError with cacheValue
        case 1:
            // read cacheValue from memory-cache
            local.cacheDict[options.cacheDict] = local.cacheDict[options.cacheDict] ||
                {};
            options.cacheValue = local.cacheDict[options.cacheDict][options.key];
            if (options.cacheValue) {
                // call onError with cacheValue
                options.modeCacheHit = true;
                onError(null, JSON.parse(options.cacheValue));
                if (!options.modeCacheUpdate) {
                    break;
                }
            }
            // run background-task with lower priority for cache-hit
            setTimeout(options.onNext, options.modeCacheHit && options.cacheTtl);
            break;
        // 2. run onTask in background
        case 2:
            local.taskCreate(options, onTask, options.onNext);
            break;
        default:
            // 3. save onTask's result to cache
            // JSON.stringify data to prevent side-effects on cache
            options.cacheValue = JSON.stringify(data);
            if (!error && options.cacheValue) {
                local.cacheDict[options.cacheDict][options.key] = options.cacheValue;
            }
            // 4. if cache-miss, then call onError with onTask's result
            if (!options.modeCacheHit) {
                onError(error, options.cacheValue && JSON.parse(options.cacheValue));
            }
            (options.onCacheWrite || local.nop)();
            break;
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.templateRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>templateRender (template, dict)](#apidoc.element.n_.context.utility2.templateRender)
- description and source-code
```javascript
templateRender = function (template, dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the template with the given dict
 */
</span>    var argList, getValue, match, renderPartial, rgx, value;
    dict = dict || {};
    getValue = function (key) {
        argList = key.split(' ');
        value = dict;
        // iteratively lookup nested values in the dict
        argList[0].split('.').forEach(function (key) {
            value = value && value[key];
        });
        return value;
    };
    renderPartial = function (match0, helper, key, partial) {
        switch (helper) {
        case 'each':
            value = getValue(key);
            return Array.isArray(value)
                ? value.map(function (dict) {
                    // recurse with partial
                    return local.templateRender(partial, dict);
                }).join('')
                : '';
        case 'if':
            partial = partial.split('{{#unless ' + key + '}}');
            partial = getValue(key)
                ? partial[0]
                // handle 'unless' case
                : partial.slice(1).join('{{#unless ' + key + '}}');
            // recurse with partial
            return local.templateRender(partial, dict);
        case 'unless':
            return getValue(key)
                ? ''
                // recurse with partial
                : local.templateRender(partial, dict);
        default:
            // recurse with partial
            return match0[0] + local.templateRender(match0.slice(1), dict);
        }
    };
    // render partials
    rgx = (/\{\{#(\w+) ([^}]+?)\}\}/g);
    template = template || '';
    for (match = rgx.exec(template); match; match = rgx.exec(template)) {
        rgx.lastIndex += 1 - match[0].length;
        template = template.replace(
            new RegExp('\\{\\{#(' + match[1] + ') (' + match[2] +
                ')\\}\\}([\\S\\s]*?)\\{\\{/' + match[1] + ' ' + match[2] +
                '\\}\\}'),
            renderPartial
        );
    }
    // search for keys in the template
    return template.replace((/\{\{[^}]+?\}\}/g), function (match0) {
        getValue(match0.slice(2, -2));
        if (value === undefined) {
            return match0;
        }
        argList.slice(1).forEach(function (arg) {
            switch (arg) {
            case 'alphanumeric':
                value = value.replace((/\W/g), '_');
                break;
            case 'decodeURIComponent':
                value = decodeURIComponent(value);
                break;
            case 'encodeURIComponent':
                value = encodeURIComponent(value);
                break;
            case 'htmlSafe':
                value = value.replace((/["&'<>]/g), function (match0) {
                    return '&#x' + match0.charCodeAt(0).toString(16) + ';';
                });
                break;
            case 'jsonStringify':
                value = JSON.stringify(value);
                break;
            case 'jsonStringify4':
                value = JSON.stringify(value, null, 4);
                break;
            case 'markdownCodeSafe':
                value = value.replace((/'/g), '\'');
                break;
            default:
                value = value[arg]();
                break;
            }
        });
        return String(value);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.templateRenderJslintLite"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>templateRenderJslintLite (template, options)](#apidoc.element.n_.context.utility2.templateRenderJslintLite)
- description and source-code
```javascript
templateRenderJslintLite = function (template, options) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the jslint-lite template with the given options.packageJson
 */
</span>    options.packageJson = options.packageJson ||
        JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    local.objectSetDefault(options.packageJson, {
        nameAlias: options.packageJson.name.replace((/\W/g), '_'),
        repository: { url: 'https://github.com/kaizhu256/node-' +
            options.packageJson.name + '.git' }
    }, 2);
    options.githubRepo = options.packageJson.repository.url.split('/').slice(-2);
    options.githubRepo[1] = options.githubRepo[1].replace((/\.git$/), '');
    template = template.replace(
        (/https:\/\/kaizhu256\.github\.io\/node-jslint-lite/g),
        'https://' +  options.githubRepo[0] + '.github.io/' +  options.githubRepo[1]
    );
    template = template.replace(
        (/kaizhu256\/node-jslint-lite/g),
        options.githubRepo.join('/')
    );
    template = template.replace(
        (/kaizhu256_2Fnode-jslint-lite/g),
        options.githubRepo.join('_2F')
    );
    template = template.replace(
        (/node-jslint-lite/g),
        options.githubRepo[1]
    );
    template = template.replace((/^#!/), '//');
    template = template.replace((/jslint-lite/g), options.packageJson.name);
    template = template.replace(
        '/* istanbul instrument in package jslint */',
        '/* istanbul instrument in package ' + options.packageJson.nameAlias + ' */'
    );
    template = template.replace(
        (/\b(assets\.|lib\.|local\.|utility2_)jslint\b/g),
        '$1' + options.packageJson.nameAlias
    );
    template = template.replace(
        (/\bh1-jslint\b/g),
        'h1-' + options.packageJson.nameAlias.replace((/_/g), '-')
    );
    template = template.replace(
        'assets.{{env.npm_package_nameAlias}}',
        'assets.' + options.packageJson.nameAlias
    );
    return template;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.testMock"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>testMock (mockList, onTestCase, onError)](#apidoc.element.n_.context.utility2.testMock)
- description and source-code
```javascript
testMock = function (mockList, onTestCase, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will mock the objects in mockList while running the onTestCase
 */
</span>    var onError2;
    onError2 = function (error) {
        // restore mock[0] from mock[2]
        mockList.reverse().forEach(function (mock) {
            local.objectSetOverride(mock[0], mock[2]);
        });
        onError(error);
    };
    // try to call onError with mock-objects
    local.tryCatchOnError(function () {
        // mock-objects
        mockList.forEach(function (mock) {
            mock[2] = {};
            // backup mock[0] into mock[2]
            Object.keys(mock[1]).forEach(function (key) {
                mock[2][key] = mock[0][key];
            });
            // override mock[0] with mock[1]
            local.objectSetOverride(mock[0], mock[1]);
        });
        // run onTestCase
        onTestCase(onError2);
    }, onError2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.testReportCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>testReportCreate (testReport)](#apidoc.element.n_.context.utility2.testReportCreate)
- description and source-code
```javascript
testReportCreate = function (testReport) {
<span class="apidocCodeCommentSpan">/*
 * this function will create test-report artifacts
 */
</span>    // print test-report summary
    console.error('\n' + new Array(56).join('-') + '\n' + testReport.testPlatformList
        .filter(function (testPlatform) {
            // if testPlatform has no tests, then filter it out
            return testPlatform.testCaseList.length;
        })
        .map(function (testPlatform) {
            return '| test-report - ' + testPlatform.name + '\n|' +
                ('        ' + testPlatform.timeElapsed + ' ms     ')
                .slice(-16) +
                ('        ' + testPlatform.testsFailed + ' failed ')
                .slice(-16) +
                ('        ' + testPlatform.testsPassed + ' passed ')
                .slice(-16) + '     |\n' + new Array(56).join('-');
        })
        .join('\n') + '\n');
    // create test-report.html
    local.fs.writeFileSync(
        local.env.npm_config_dir_build + '/test-report.html',
        local.testReportMerge(testReport, {})
    );
    // create build.badge.svg
    local.fs.writeFileSync(local.env.npm_config_dir_build +
        '/build.badge.svg', local.assetsDict['/assets.buildBadge.template.svg']
        // edit branch name
        .replace((/0000-00-00 00:00:00/g),
            new Date().toISOString().slice(0, 19).replace('T', ' '))
        // edit branch name
        .replace((/- master -/g), '| ' + local.env.CI_BRANCH + ' |')
        // edit commit id
        .replace(
            (/aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa/g),
            local.env.CI_COMMIT_ID
        ));
    // create test-report.badge.svg
    local.fs.writeFileSync(
        local.env.npm_config_dir_build + '/test-report.badge.svg',
        local.assetsDict['/assets.testReportBadge.template.svg']
            // edit number of tests failed
            .replace((/999/g), testReport.testsFailed)
            // edit badge color
            .replace(
                (/d00/g),
                // coverage-hack - cover both fail and pass cases
                '0d00'.slice(!!testReport.testsFailed).slice(0, 3)
            )
    );
    console.error('created test-report file://' + local.env.npm_config_dir_build +
        '/test-report.html\n');
    // if any test failed, then exit with non-zero exit-code
    console.error('\n' + local.env.MODE_BUILD +
        ' - ' + testReport.testsFailed + ' failed tests\n');
    // exit with number of tests failed
    local.exit(testReport.testsFailed);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.testReportMerge"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>testReportMerge (testReport1, testReport2)](#apidoc.element.n_.context.utility2.testReportMerge)
- description and source-code
```javascript
testReportMerge = function (testReport1, testReport2) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. merge testReport2 into testReport1
 * 2. return testReport1 in html-format
 */
</span>    var errorStackList, testCaseNumber, testReport;
    // 1. merge testReport2 into testReport1
    [testReport1, testReport2].forEach(function (testReport, ii) {
        ii += 1;
        local.objectSetDefault(testReport, {
            date: new Date().toISOString(),
            errorStackList: [],
            testPlatformList: [],
            timeElapsed: 0
        }, 8);
        // security - handle malformed testReport
        local.assert(
            testReport && typeof testReport === 'object',
            ii + ' invalid testReport ' + typeof testReport
        );
        // validate timeElapsed
        local.assert(
            typeof testReport.timeElapsed === 'number',
            ii + ' invalid testReport.timeElapsed ' + typeof testReport.timeElapsed
        );
        // security - handle malformed testReport.testPlatformList
        testReport.testPlatformList.forEach(function (testPlatform) {
            local.objectSetDefault(testPlatform, {
                name: 'undefined',
                testCaseList: [],
                timeElapsed: 0
            }, 8);
            local.assert(
                typeof testPlatform.name === 'string',
                ii + ' invalid testPlatform.name ' + typeof testPlatform.name
            );
            // insert $MODE_BUILD into testPlatform.name
            if (local.env.MODE_BUILD) {
                testPlatform.name = testPlatform.name.replace(
                    (/^(browser|node)\b/),
                    local.env.MODE_BUILD + ' - $1'
                );
            }
            // validate timeElapsed
            local.assert(
                typeof testPlatform.timeElapsed === 'number',
                ii + ' invalid testPlatform.timeElapsed ' +
                    typeof testPlatform.timeElapsed
            );
            // security - handle malformed testPlatform.testCaseList
            testPlatform.testCaseList.forEach(function (testCase) {
                local.objectSetDefault(testCase, {
                    errorStack: '',
                    name: 'undefined',
                    timeElapsed: 0
                }, 8);
                local.assert(
                    typeof testCase.errorStack === 'string',
                    ii + ' invalid testCase.errorStack ' + typeof testCase.errorStack
                );
                local.assert(
                    typeof testCase.name === 'string',
                    ii + ' invalid testCase.name ' + typeof testCase.name
                );
                // validate timeElapsed
                local.assert(
                    typeof testCase.timeElapsed === 'number',
                    ii + ' invalid testCase.timeElapsed ' + typeof testCase.timeElapsed
                );
            });
        });
    });
    // merge testReport2.testPlatformList into testReport1.testPlatformList
    testReport2.testPlatformList.forEach(function (testPlatform2) {
        // add testPlatform2 to testReport1.testPlatformList
        testReport1.testPlatformList.push(testPlatform2);
    });
    // update testReport1.timeElapsed
    testReport1.timeElapsed += testReport2.timeElapsed;
    testReport = testReport1;
    testReport.testsFailed = 0;
    testReport.testsPassed = 0;
    testReport.testsPending = 0;
    testReport.testPlatformList.forEach(function (testPlatform) {
        testPlatform.testsFailed = 0;
        testPlatform.testsPassed = 0;
        testPlatform.testsPending = 0;
        testPlatform.testCaseList.forEach(function (testCase) {
            switch (testCase.status) {
            // update failed tests
            case 'failed':
                testPlatform.testsFailed += 1;
                testReport.testsFailed += 1;
                break;
            // update passed tests
            case 'passed':
                testPlatform.testsPassed += 1;
                testReport.testsPassed += 1;
                break;
            // update pending tests ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.testRunDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>testRunDefault (options)](#apidoc.element.n_.context.utility2.testRunDefault)
- description and source-code
```javascript
testRunDefault = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will run all tests in testPlatform.testCaseList
 */
</span>    var exit, testPlatform, testReport, testReportDiv1, timerInterval;
    // init modeTest
    local.modeTest = local.modeTest || local.env.npm_config_mode_test;
    if (!(local.modeTest || options.modeTest)) {
        return;
    }
    if (!options.testRunBeforeDone) {
        options.testRunBeforeTimer = options.testRunBeforeTimer ||
            setTimeout(function () {
                local._testRunBefore();
                local.onReadyAfter(function () {
                    options.testRunBeforeDone = true;
                    local.testRunDefault(options);
                });
            });
        return;
    }
    // reset _testRunBefore
    options.testRunBeforeDone = options.testRunBeforeTimer = null;
    // visual notification - testRun
    local.ajaxProgressUpdate();
    switch (local.modeJs) {
    case 'node':
        // mock proces.exit
        exit = process.exit;
        process.exit = local.nop;
        break;
    }
    // init modeTestCase
    local.modeTestCase = local.modeTestCase || local.env.npm_config_mode_test_case;
    // init testReport
    testReport = local.testReport;
    // init testReport timer
    local.timeElapsedStart(testReport);
    // init testPlatform
    testPlatform = local.testReport.testPlatformList[0];
    // init testPlatform timer
    local.timeElapsedStart(testPlatform);
    // reset testPlatform.testCaseList
    testPlatform.testCaseList.length = 0;
    // add tests into testPlatform.testCaseList
    Object.keys(options).forEach(function (key) {
        // add testCase options[key] to testPlatform.testCaseList
        if ((local.modeTestCase && local.modeTestCase.split(',').indexOf(key) >= 0) ||
                (!local.modeTestCase && key.indexOf('testCase_') === 0)) {
            testPlatform.testCaseList.push({
                name: key,
                status: 'pending',
                onTestCase: options[key]
            });
        }
    });
    // visual notification - update test-progress until done
    // init testReportDiv1 element
    if (local.modeJs === 'browser') {
        testReportDiv1 = document.querySelector('#testReportDiv1');
    }
    testReportDiv1 = testReportDiv1 || { style: {} };
    testReportDiv1.style.display = 'block';
    testReportDiv1.innerHTML = local.testReportMerge(testReport, {});
    // update test-report status every 1000 ms until done
    timerInterval = setInterval(function () {
        // update testReportDiv1 in browser
        testReportDiv1.innerHTML = local.testReportMerge(testReport, {});
        if (testReport.testsPending === 0) {
            // cleanup timerInterval
            clearInterval(timerInterval);
        }
    }, 1000);
    // shallow-copy testPlatform.testCaseList to prevent side-effects
    // from in-place sort from testReportMerge
    local.onParallelList({
        list: testPlatform.testCaseList.slice()
    }, function (testCase, onParallel) {
        var onError, timerTimeout;
        onError = function (error) {
            // cleanup timerTimeout
            clearTimeout(timerTimeout);
            // if testCase already done, then fail testCase with error for ending again
            if (testCase.done) {
                error = error || new Error('callback in testCase ' +
                    testCase.name + ' called multiple times');
            }
            // if error occurred, then fail testCase
            if (error) {
                testCase.status = 'failed';
                console.error('\ntestCase ' + testCase.name + ' failed\n' +
                    error.message + '\n' + error.stack);
                testCase.errorStack = testCase.errorStack ||
                    error.message + '\n' + error.stack;
                // validate errorStack is non-empty
                local.assert(
                    testCase.errorStack,
                    'invalid errorStack ' + testCase.errorStack
                );
            }
            // if already done, then do nothing
            if (testCase.done) { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.testRunServer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>testRunServer (options)](#apidoc.element.n_.context.utility2.testRunServer)
- description and source-code
```javascript
testRunServer = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. create server from local._middleware
 * 2. start server on local.env.PORT
 * 3. run tests
 */
</span>    if (local.global.utility2_serverHttp1) {
        return;
    }
    local.onReadyBefore.counter += 1;
    local._middleware = local._middleware || local.middlewareGroupCreate([
        local.middlewareInit,
        local.middlewareForwardProxy,
        local.middlewareAssetsCached,
        local._middlewareJsonpStateInit
    ]);
    // 1. create server from local._middleware
    local.serverLocalRequestHandler = function (request, response) {
        local._middleware(request, response, function (error) {
            local._middlewareError(error, request, response);
        });
    };
    local.global.utility2_serverHttp1 = local.http.createServer(
        local.serverLocalRequestHandler
    );
    // 2. start server on local.env.PORT
    console.error('server listening on http-port ' + local.env.PORT);
    local.onReadyBefore.counter += 1;
    local.global.utility2_serverHttp1.listen(local.env.PORT, local.onReadyBefore);
    // 3. run tests
    local.testRunDefault(options);
    local.onReadyBefore();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.timeElapsedPoll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>timeElapsedPoll (options)](#apidoc.element.n_.context.utility2.timeElapsedPoll)
- description and source-code
```javascript
timeElapsedPoll = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will poll options.timeElapsed
 */
</span>    options = local.timeElapsedStart(options);
    options.timeElapsed = Date.now() - options.timeStart;
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.timeElapsedStart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>timeElapsedStart (options, timeStart)](#apidoc.element.n_.context.utility2.timeElapsedStart)
- description and source-code
```javascript
timeElapsedStart = function (options, timeStart) {
<span class="apidocCodeCommentSpan">/*
 * this function will start options.timeElapsed
 */
</span>    options = options || {};
    options.timeStart = timeStart || options.timeStart || Date.now();
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.tokenizer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>tokenizer (e)](#apidoc.element.n_.context.utility2.tokenizer)
- description and source-code
```javascript
function tokenizer(e){function n
(){return t.text.charAt(t.pos)}function r(e,n){var r=t.text.charAt(t.pos++);if(e&&!
r)throw EX_EOF;return r=="\n"?(t.newline_before=t.newline_before||!n,++t.line,t.
col=0):++t.col,r}function i(){return!t.peek()}function s(e,n){var r=t.text.indexOf
(e,t.pos);if(n&&r==-1)throw EX_EOF;return r}function o(){t.tokline=t.line,t.tokcol=
t.col,t.tokpos=t.pos}function u(e,n,r){t.regex_allowed=e=="operator"&&!HOP(UNARY_POSTFIX
,n)||e=="keyword"&&HOP(KEYWORDS_BEFORE_EXPRESSION,n)||e=="punc"&&HOP(PUNC_BEFORE_EXPRESSION
,n);var i={type:e,value:n,line:t.tokline,col:t.tokcol,pos:t.tokpos,endpos:t.pos,
nlb:t.newline_before};if(!r){i.comments_before=t.comments_before,t.comments_before=
[];for(var s=0,o=i.comments_before.length;s<o;s++)i.nlb=i.nlb||i.comments_before
[s].nlb}return t.newline_before=!1,i}function a(){while(HOP(WHITESPACE_CHARS,n()
))r()}function f(e){var t="",i=n(),s=0;while(i&&e(i,s++))t+=r(),i=n();return t}function l
(e){js_error(e,t.tokline,t.tokcol,t.tokpos)}function c(e){var t=!1,n=!1,r=!1,i=e=="."
,s=f(function(s,o){return s=="x"||s=="X"?r?!1:r=!0:!!r||s!="E"&&s!="e"?s=="-"?n||
o==0&&!e?!0:!1:s=="+"?n:(n=!1,s=="."?!i&&!r&&!t?i=!0:!1:is_alphanumeric_char(s))
:t?!1:t=n=!0});e&&(s=e+s);var o=parse_js_number(s);if(!isNaN(o))return u("num",o
);l("Invalid syntax: "+s)}function h(e){var t=r(!0,e);switch(t){case"n":return"\n"
;case"r":return"\r";case"t":return"	";case"b":return"\b";case"v":return"";case"f"
:return"\f";case"0":return"\0";case"x":return String.fromCharCode(p(2));case"u":
return String.fromCharCode(p(4));case"\n":return"";default:return t}}function p(
e){var t=0;for(;e>0;--e){var n=parseInt(r(!0),16);isNaN(n)&&l("Invalid hex-character pattern in string"
),t=t<<4|n}return t}function d(){return x("Unterminated string constant",function(
){var e=r(),t="";for(;;){var n=r(!0);if(n=="\\"){var i=0,s=null;n=f(function(e){
if(e>="0"&&e<="7"){if(!s)return s=e,++i;if(s<="3"&&i<=2)return++i;if(s>="4"&&i<=1
)return++i}return!1}),i>0?n=String.fromCharCode(parseInt(n,8)):n=h(!0)}else{if(n==
e)break;if(n=="\n")throw EX_EOF}t+=n}return u("string",t)})}function v(){r();var e=
s("\n"),n;return e==-1?(n=t.text.substr(t.pos),t.pos=t.text.length):(n=t.text.substring
(t.pos,e),t.pos=e),u("comment1",n,!0)}function m(){return r(),x("Unterminated multiline comment"
,function(){var e=s("*/",!0),n=t.text.substring(t.pos,e);return t.pos=e+2,t.line+=
n.split("\n").length-1,t.newline_before=t.newline_before||n.indexOf("\n")>=0,/^@cc_on/i
.test(n)&&(warn("WARNING: at line "+t.line),warn('*** Found "conditional comment": '+
n),warn("*** UglifyJS DISCARDS ALL COMMENTS.  This means your code might no longer work properly in Internet Explorer."
)),u("comment2",n,!0)})}function g(){var e=!1,t="",i,s=!1,o;while((i=n())!=null)
if(!e)if(i=="\\")s=e=!0,r();else{if(!is_identifier_char(i))break;t+=r()}else i!="u"&&
l("Expecting UnicodeEscapeSequence -- uXXXX"),i=h(),is_identifier_char(i)||l("Unicode char: "+
i.charCodeAt(0)+" is not valid in identifier"),t+=i,e=!1;return HOP(KEYWORDS,t)&&
s&&(o=t.charCodeAt(0).toString(16).toUpperCase(),t="\\u"+"0000".substr(o.length)+
o+t.slice(1)),t}function y(e){return x("Unterminated regular expression",function(
){var t=!1,n,i=!1;while(n=r(!0))if(t)e+="\\"+n,t=!1;else if(n=="[")i=!0,e+=n;else if(
n=="]"&&i)i=!1,e+=n;else{if(n=="/"&&!i)break;n=="\\"?t=!0:e+=n}var s=g();return u
("regexp",[e,s])})}function b(e){function t(e){if(!n())return e;var i=e+n();return HOP
(OPERATORS,i)?(r(),t(i)):e}return u("operator",t(e||r()))}function w(){r();var e=
t.regex_allowed;switch(n()){case"/":return t.comments_before.push(v()),t.regex_allowed=
e,T();case"*":return t.comments_before.push(m()),t.regex_allowed=e,T()}return t.
regex_allowed?y(""):b("/")}function E(){return r(),is_digit(n())?c("."):u("punc"
,".")}function S(){var e=g();return HOP(KEYWORDS,e)?HOP(OPERATORS,e)?u("operator"
,e):HOP(KEYWORDS_ATOM,e)?u("atom",e):u("keyword",e):u("name",e)}function x(e,t){
try{return t()}catch(n){if(n!==EX_EOF)throw n;l(e)}}function T(e){if(e!=null)return y
(e);a(),o();var t=n();if(!t)return u("eof");if(is_d ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.tryCatchOnError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>tryCatchOnError (fnc, onError)](#apidoc.element.n_.context.utility2.tryCatchOnError)
- description and source-code
```javascript
tryCatchOnError = function (fnc, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to run the fnc in a try-catch block,
 * else call onError with the errorCaught
 */
</span>    // validate onError
    local.assert(typeof onError === 'function', typeof onError);
    try {
        // reset errorCaught
        local._debugTryCatchErrorCaught = null;
        return fnc();
    } catch (errorCaught) {
        // debug errorCaught
        local._debugTryCatchErrorCaught = errorCaught;
        return onError(errorCaught);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.tryCatchReadFile"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>tryCatchReadFile (file, options)](#apidoc.element.n_.context.utility2.tryCatchReadFile)
- description and source-code
```javascript
tryCatchReadFile = function (file, options) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to read the file or return an empty string
 */
</span>    var data;
    data = '';
    try {
        data = local.fs.readFileSync(file, options);
    } catch (ignore) {
    }
    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uglify"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uglify (code, file)](#apidoc.element.n_.context.utility2.uglify)
- description and source-code
```javascript
uglify = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will uglify the js-code
 */
</span>    var ast;
    // uglify css
    if ((file || '').slice(-4) === '.css') {
        return code
            // remove comment /**/
            .replace((/\/\*[\S\s]*?\*\//g), '')
            // remove comment //
            .replace((/\/\/.*/g), '')
            // remove whitespace
            .replace((/\t/g), ' ')
            .replace((/ {2,}/g), ' ')
            .replace((/ *?([\n,:;{}]) */g), '$1')
            .replace((/\n\n+/g), '\n')
            .trim();
    }
    // parse code and get the initial AST
    ast = local.parse(code
        .trim()
        // comment shebang
        .replace((/^#!/), '//'));
    // get a new AST with mangled names
    ast = local.ast_mangle(ast);
    // get an AST with compression optimizations
    ast = local.ast_squeeze(ast);
    // compressed code here
    return local.split_lines(local.gen_code(ast, { ascii_only: true }), 79);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateFadeIn"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateFadeIn (element)](#apidoc.element.n_.context.utility2.uiAnimateFadeIn)
- description and source-code
```javascript
uiAnimateFadeIn = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will fadeIn the element
 */
</span>    element.classList.add('swggAnimateFade');
    element.style.display = '';
    setTimeout(function () {
        element.style.opacity = '';
    }, 20);
    setTimeout(function () {
        element.classList.remove('swggAnimateFade');
    }, 500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateFadeOut"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateFadeOut (element)](#apidoc.element.n_.context.utility2.uiAnimateFadeOut)
- description and source-code
```javascript
uiAnimateFadeOut = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will fadeOut the element
 */
</span>    element.classList.add('swggAnimateFade');
    element.style.opacity = '0';
    setTimeout(function () {
        element.style.display = 'none';
        element.classList.remove('swggAnimateFade');
    }, 500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateScrollTo"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateScrollTo (element)](#apidoc.element.n_.context.utility2.uiAnimateScrollTo)
- description and source-code
```javascript
uiAnimateScrollTo = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will scrollTo the element
 */
</span>    var ii, timerInterval;
    ii = 0;
    timerInterval = setInterval(function () {
        ii += 0.025;
        local.global.scrollTo(0, document.body.scrollTop +
            Math.min(ii, 1) * (element.offsetTop - document.body.scrollTop) +
            -5);
    }, 25);
    setTimeout(function () {
        clearInterval(timerInterval);
    }, 1000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateShake"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateShake (element)](#apidoc.element.n_.context.utility2.uiAnimateShake)
- description and source-code
```javascript
uiAnimateShake = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will shake the dom-element
 */
</span>    element.classList.add('swggAnimateShake');
    setTimeout(function () {
        element.classList.remove('swggAnimateShake');
    }, 500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateSlideAccordian"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideAccordian (element, elementList)](#apidoc.element.n_.context.utility2.uiAnimateSlideAccordian)
- description and source-code
```javascript
uiAnimateSlideAccordian = function (element, elementList) {
<span class="apidocCodeCommentSpan">/*
 * this function will slideDown the element,
 * but slideUp all other elements in elementList
 */
</span>    // hide elements in elementList
    elementList.forEach(function (element2) {
        if (element2 !== element) {
            local.uiAnimateSlideUp(element2);
        }
    });
    // show element
    local.uiAnimateSlideDown(element);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateSlideDown"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideDown (element)](#apidoc.element.n_.context.utility2.uiAnimateSlideDown)
- description and source-code
```javascript
uiAnimateSlideDown = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will slideDown the dom-element
 */
</span>    if (element.style.display !== 'none') {
        return;
    }
    element.style.maxHeight = 0;
    element.classList.add('swggAnimateSlide');
    element.style.display = '';
    setTimeout(function () {
        element.style.maxHeight = 2 * local.global.innerHeight + 'px';
    }, 20);
    setTimeout(function () {
        element.style.maxHeight = '';
        element.classList.remove('swggAnimateSlide');
    }, 500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiAnimateSlideUp"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiAnimateSlideUp (element)](#apidoc.element.n_.context.utility2.uiAnimateSlideUp)
- description and source-code
```javascript
uiAnimateSlideUp = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will slideUp the dom-element
 */
</span>    if (element.style.display === 'none') {
        return;
    }
    element.style.maxHeight = 2 * local.global.innerHeight + 'px';
    element.classList.add('swggAnimateSlide');
    setTimeout(function () {
        element.style.maxHeight = '0px';
    }, 20);
    setTimeout(function () {
        element.style.display = 'none';
    }, 500);
    setTimeout(function () {
        element.style.maxHeight = '';
        element.classList.remove('swggAnimateSlide');
    }, 500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiDatatableRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiDatatableRender (options)](#apidoc.element.n_.context.utility2.uiDatatableRender)
- description and source-code
```javascript
uiDatatableRender = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the datatable
 */
</span>    var tmp;
    local.uiState.datatable = options;
    options.schema = local.schemaNormalizeAndCopy(options.schema);
    options.propDefList = Object.keys(options.schema.properties)
        .sort(function (aa, bb) {
            return aa === options._idAlias
                ? -1
                : bb === options._idAlias
                ? 1
                : aa < bb
                ? -1
                : 1;
        })
        .map(function (propDef) {
            tmp = propDef;
            propDef = options.schema.properties[tmp];
            propDef.name = tmp;
            local.uiParamRender(propDef);
            return propDef;
        });
    options.iiPadding = 0;
    options.dbRowList = options.responseJson.data.map(function (dbRow, ii) {
        dbRow = { paramDict: dbRow };
        dbRow.colList = options.propDefList.map(function (propDef) {
            propDef = local.jsonCopy(propDef);
            propDef.valueEncoded = dbRow.paramDict[propDef.name];
            if (propDef.valueEncoded === undefined) {
                propDef.valueEncoded = '';
            }
            if (typeof propDef.valueEncoded !== 'string') {
                propDef.valueEncoded = JSON.stringify(propDef.valueEncoded);
            }
            return propDef;
        });
        dbRow.id = dbRow.paramDict[options._idAlias];
        dbRow.ii = options.querySkip + ii + 1;
        options.iiPadding = Math.max(
            0.375 * String(dbRow.ii).length,
            options.iiPadding
        );
        return dbRow;
    });
    // init pagination
    options.pageCurrent = Math.floor(options.querySkip / options.queryLimit);
    options.pageTotal = Math.ceil(
        options.responseJson.meta.paginationCountTotal / options.queryLimit
    );
    options.pageMin = Math.max(
        Math.min(options.pageCurrent - 3, options.pageTotal - 7),
        0
    );
    options.pageMax = Math.min(options.pageMin + 7, options.pageTotal);
    options.pageList = [];
    // add first page
    options.pageList.push({
        disabled: options.pageCurrent === 0,
        pageNumber: 0,
        valueEncoded: 'first page'
    });
    for (tmp = options.pageMin; tmp < options.pageMax; tmp += 1) {
        options.pageList.push({
            disabled: tmp === options.pageCurrent,
            pageNumber: tmp,
            valueEncoded: JSON.stringify(tmp + 1)
        });
    }
    // add last page
    options.pageList.push({
        disabled: options.pageCurrent === options.pageTotal - 1,
        pageNumber: options.pageTotal - 1,
        valueEncoded: 'last page'
    });
    options.pageCurrentIsFirst = options.pageCurrent === 0;
    options.pageCurrentIsLast = options.pageCurrent + 1 === options.pageTotal;
    // templateRender datatable
    document.querySelector('.swggUiContainer .datatable').innerHTML =
        local.templateRender(local.templateUiDatatable, options);
    // init event-handling
    local.uiEventInit(document.querySelector('.swggUiContainer .datatable'));
    // show modal
    if (document.querySelector('.swggUiContainer > .modal').style.display !== 'none') {
        return;
    }
    document.body.style.overflow = 'hidden';
    local.uiAnimateFadeIn(document.querySelector('.swggUiContainer > .modal'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiEventDelegate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiEventDelegate (event)](#apidoc.element.n_.context.utility2.uiEventDelegate)
- description and source-code
```javascript
uiEventDelegate = function (event) {
    Object.keys(local.uiEventListenerDict).sort().some(function (key) {
        if (!(event.currentTarget.matches(key) || event.target.matches(key))) {
            return;
        }
        switch (event.target.tagName) {
        case 'A':
        case 'BUTTON':
        case 'FORM':
            event.preventDefault();
            break;
        }
        event.stopPropagation();
        local.uiEventListenerDict[key](event);
        return true;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiEventInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiEventInit (element)](#apidoc.element.n_.context.utility2.uiEventInit)
- description and source-code
```javascript
uiEventInit = function (element) {
<span class="apidocCodeCommentSpan">/*
 * this function will init event-handling for the dom-element
 */
</span>    ['Click', 'Submit'].forEach(function (eventType) {
        Array.from(
            element.querySelectorAll('.eventDelegate' + eventType)
        ).forEach(function (element) {
            element.addEventListener(eventType.toLowerCase(), local.uiEventDelegate);
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiParamRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiParamRender (paramDef)](#apidoc.element.n_.context.utility2.uiParamRender)
- description and source-code
```javascript
uiParamRender = function (paramDef) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the param
 */
</span>    paramDef.placeholder = paramDef.required
        ? '(required)'
        : '';
    // init input - file
    if (paramDef.type === 'file') {
        paramDef.isFile = true;
    // init input - textarea
    } else if (paramDef.in === 'body') {
        paramDef.isTextarea = true;
    // init input - select
    } else if (paramDef.enum || paramDef.type === 'boolean') {
        paramDef.enumDefault = [];
        if (paramDef.default !== undefined) {
            paramDef.enumDefault = paramDef.type === 'array'
                ? paramDef.default
                : [paramDef.default];
        }
        paramDef.isSelect = true;
        paramDef.isSelectMultiple = paramDef.type === 'array';
        paramDef.selectOptionList = (paramDef.type === 'boolean'
            ? [false, true]
            : paramDef.enum).map(function (element) {
            paramDef.hasDefault |= paramDef.enumDefault.indexOf(element) >= 0;
            return {
                id: local.idDomElementCreate('swgg_id_' + paramDef.name),
                selected: paramDef.enumDefault.indexOf(element) >= 0
                    ? 'selected'
                    : '',
                type: (paramDef.items && paramDef.items.type) || paramDef.type,
                valueDecoded: element,
                valueEncoded: typeof element === 'string'
                    ? element
                    : JSON.stringify(element)
            };
        });
        // init 'undefined' value
        if (!(paramDef.hasDefault ||
                paramDef.isSelectMultiple ||
                paramDef.required)) {
            paramDef.selectOptionList.unshift({
                id: local.idDomElementCreate('swgg_id_' + paramDef.name),
                selected: 'selected',
                type: paramDef.type,
                valueDecoded: '$swggUndefined',
                valueEncoded: '<none>'
            });
        }
        // if required, then select at least one value
        if (paramDef.required && paramDef.selectOptionList.length) {
            paramDef.selected = paramDef.selectOptionList[0];
            paramDef.selectOptionList.some(function (element) {
                if (element.selected) {
                    paramDef.selected = element.selected;
                    return true;
                }
            });
            paramDef.selected = 'selected';
        }
    // init input - textarea
    } else if (paramDef.type === 'array') {
        paramDef.isTextarea = true;
        paramDef.placeholder = 'provide multiple values in new lines' +
            (paramDef.required
                ? ' (at least one required)'
                : '');
    // init input - text
    } else {
        paramDef.isInputText = true;
    }
    // init format2 / type2
    [
        paramDef,
        paramDef.schema
    ].some(function (element) {
        local.tryCatchOnError(function () {
            paramDef.format2 = paramDef.format2 || element.format;
        }, local.nop);
        local.tryCatchOnError(function () {
            paramDef.type2 = paramDef.type2 || element.type;
        }, local.nop);
        return paramDef.type2;
    });
    paramDef.type2 = paramDef.type2 || 'object';
    // init schema2
    [
        paramDef.items,
        paramDef.schema,
        paramDef.schema && paramDef.schema.items
    ].some(function (element) {
        paramDef.schema2 = local.schemaNormalizeAndCopy(element || {}).properties;
        return paramDef.schema2;
    });
    if (paramDef.schema2) {
        paramDef.schemaText = JSON.stringify(paramDef.type2 === 'array'
            ? [paramDef.schema2]
            : paramDef.schema2, null, 4);
    }
    // init valueEncoded
    paramDef.valueEncoded = paramDef.default;
    if (paramDef.valueEncoded === undefined) {
        paramDef.valueEncoded = local.dbFieldRandomCreate({
            modeNotRandom: true,
            propDef: paramDef
        });
    }
    // init valueEncoded for array
    if (paramDef.valueEncoded && paramDef.type2 === 'array' && paramDef.in !== 'body') {
        pa ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiRender ()](#apidoc.element.n_.context.utility2.uiRender)
- description and source-code
```javascript
uiRender = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will render swagger-ui
 */
</span>    var resource, self;
    // reset state
    local.idDomElementDict = {};
    self = local.uiState = local.jsonCopy(local.swaggerJson);
    // init url
    self.url = document.querySelector('.swggUiContainer > .header > .td2').value;
    // templateRender main
    self.uiFragment = local.domFragmentRender(local.templateUiMain, self);
    local.objectSetDefault(self, {
        resourceDict: {},
        operationDict: {},
        tagDict: {}
    });
    // init tagDict
    self.tags.forEach(function (tag) {
        self.tagDict[tag.name] = tag;
    });
    // init operationDict
    Object.keys(local.apiDict).sort().forEach(function (operation) {
        // init operation
        operation = local.jsonCopy(local.apiDict[operation]);
        operation.tags.forEach(function (tag) {
            self.operationDict[operation._keyOperationId] = operation;
            // init resource
            resource = self.resourceDict[tag];
            if (!resource && self.tagDict[tag]) {
                resource = self.resourceDict[tag] = self.tagDict[tag];
                local.objectSetDefault(resource, {
                    description: 'no description available',
                    id: local.idDomElementCreate('swgg_id_' + tag),
                    name: tag,
                    operationListInnerHtml: ''
                });
            }
        });
    });
    // init resourceDict
    Object.keys(self.resourceDict).sort().forEach(function (key) {
        // templateRender resource
        self.uiFragment.querySelector('.resourceList').appendChild(
            local.domFragmentRender(local.templateUiResource, self.resourceDict[key])
        );
    });
    Object.keys(self.operationDict).sort(function (aa, bb) {
        aa = self.operationDict[aa];
        aa = aa._path + ' ' + aa._method;
        bb = self.operationDict[bb];
        bb = bb._path + ' ' + bb._method;
        return aa < bb
            ? -1
            : 1;
    }).forEach(function (operation) {
        operation = self.operationDict[operation];
        operation.id = local.idDomElementCreate('swgg_id_' + operation.operationId);
        operation.tags.forEach(function (tag) {
            operation = local.jsonCopy(operation);
            resource = self.resourceDict[tag];
            local.objectSetDefault(operation, {
                description: '',
                responseList: Object.keys(operation.responses).sort()
                    .map(function (key) {
                        return { key: key, value: operation.responses[key] };
                    }),
                summary: 'no summary available'
            });
            operation.parameters.forEach(function (element) {
                // init element.id
                element.id = local.idDomElementCreate('swgg_id_' + element.name);
                local.uiParamRender(element);
            });
            // templateRender operation
            self.uiFragment.querySelector('#' + resource.id + ' .operationList')
                .appendChild(
                    local.domFragmentRender(local.templateUiOperation, operation)
                );
        });
    });
    // overwrite swggUiContainer with uiFragment
    document.querySelector('.swggUiContainer').innerHTML = '';
    document.querySelector('.swggUiContainer').appendChild(self.uiFragment);
    /* istanbul ignore next */
    // bug-workaround - add keypress listener for <form2>
    document.querySelector('form2').addEventListener('keypress', function (event) {
        if (event.keyCode === 13) {
            local.uiEventListenerDict['.onEventUiReload']();
        }
    });
    // render valueEncoded
    Array.from(
        document.querySelectorAll('.swggUiContainer [data-value-encoded]')
    ).forEach(function (element) {
        element.value = decodeURIComponent(element.dataset.valueEncoded);
    });
    // init event-handling
    local.uiEventInit(document);
    // scrollTo location.hash
    local.uiScrollTo(location.hash);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uiScrollTo"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uiScrollTo (locationHash)](#apidoc.element.n_.context.utility2.uiScrollTo)
- description and source-code
```javascript
uiScrollTo = function (locationHash) {
<span class="apidocCodeCommentSpan">/*
 * this function will scrollTo locationHash
 */
</span>    var operation, resource;
    // init resource
    resource = locationHash.split('/')[1];
    // list operations
    resource = document.querySelector('.swggUiContainer #' + resource) ||
        document.querySelector('.swggUiContainer .resource');
    local.uiAnimateSlideDown(resource.querySelector('.operationList'));
    // init operation
    operation = locationHash.split('/')[2];
    operation = resource.querySelector('#' + operation);
    // expand operation and scroll to it
    if (operation) {
        local.uiAnimateSlideDown(operation.querySelector('.content'));
        // scroll to operation
        local.uiAnimateScrollTo(operation);
    } else {
        // scroll to resource
        local.uiAnimateScrollTo(resource);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.urlBaseGet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>urlBaseGet ()](#apidoc.element.n_.context.utility2.urlBaseGet)
- description and source-code
```javascript
urlBaseGet = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will return the base swagger url
 */
</span>    return (local.swaggerJson.schemes ||
        local.urlParse('').protocol.slice(0, -1)) + '://' +
        (local.swaggerJson.host || local.urlParse('').host) +
        local.swaggerJson.basePath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.urlParse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>urlParse (url)](#apidoc.element.n_.context.utility2.urlParse)
- description and source-code
```javascript
urlParse = function (url) {
<span class="apidocCodeCommentSpan">/*
 * https://developer.mozilla.org/en-US/docs/Web/API/URL
 * this function will parse the url according to the above spec, plus a query param
 */
</span>    var urlParsed;
    urlParsed = {};
    // try to parse the url
    local.tryCatchOnError(function () {
        // resolve host-less url
        switch (local.modeJs) {
        case 'browser':
            local.serverLocalHost = local.serverLocalHost ||
                location.protocol + '//' + location.host;
            // resolve absolute path
            if (url[0] === '/') {
                url = local.serverLocalHost + url;
            // resolve relative path
            } else if (!(/^\w+?:\/\//).test(url)) {
                url = local.serverLocalHost +
                    location.pathname.replace((/\/[^\/]*?$/), '') + '/' + url;
            }
            urlParsed = new local.global.URL(url);
            urlParsed.path = '/' + urlParsed.href
                .split('/')
                .slice(3)
                .join('/')
                .split('#')[0];
            break;
        case 'node':
            local.env.PORT = local.env.PORT || '8081';
            local.serverLocalHost = local.serverLocalHost ||
                ('http://127.0.0.1:' + local.env.PORT);
            // resolve absolute path
            if (url[0] === '/') {
                url = local.serverLocalHost + url;
            // resolve relative path
            } else if (!(/^\w+?:\/\//).test(url)) {
                url = local.serverLocalHost + '/' + url;
            }
            urlParsed = local.url.parse(url);
            break;
        }
        // init query
        urlParsed.query = {};
        urlParsed.search.slice(1).replace((/[^&]+/g), function (item) {
            item = item.split('=');
            item[0] = decodeURIComponent(item[0]);
            item[1] = decodeURIComponent(item.slice(1).join('='));
            // parse repeating query-param as an array
            if (urlParsed.query[item[0]]) {
                if (!Array.isArray(urlParsed.query[item[0]])) {
                    urlParsed.query[item[0]] = [urlParsed.query[item[0]]];
                }
                urlParsed.query[item[0]].push(item[1]);
            } else {
                urlParsed.query[item[0]] = item[1];
            }
        });
    }, local.nop);
    // https://developer.mozilla.org/en/docs/Web/API/URL#Properties
    return {
        hash: urlParsed.hash || '',
        host: urlParsed.host || '',
        hostname: urlParsed.hostname || '',
        href: urlParsed.href || '',
        path: urlParsed.path || '',
        pathname: urlParsed.pathname || '',
        port: urlParsed.port || '',
        protocol: urlParsed.protocol || '',
        query: urlParsed.query || {},
        search: urlParsed.search || ''
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.userLoginByPassword"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>userLoginByPassword (options, onError)](#apidoc.element.n_.context.utility2.userLoginByPassword)
- description and source-code
```javascript
userLoginByPassword = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will send a login-by-password request
 */
</span>    local.apiDict["GET /user/userLoginByPassword"]._ajax({
        paramDict: { password: options.password, username: options.username }
    }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.userLogout"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>userLogout (options, onError)](#apidoc.element.n_.context.utility2.userLogout)
- description and source-code
```javascript
userLogout = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will send a logout request
 */
</span>    local.apiDict["GET /user/userLogout"]._ajax(options, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.uuid4Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>uuid4Create ()](#apidoc.element.n_.context.utility2.uuid4Create)
- description and source-code
```javascript
uuid4Create = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random uuid,
 * with format 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'
 */
</span>    // code derived from http://jsperf.com/uuid4
    var id, ii;
    id = '';
    for (ii = 0; ii < 32; ii += 1) {
        switch (ii) {
        case 8:
        case 20:
            id += '-';
            // coerce to finite integer
            id += (Math.random() * 16 | 0).toString(16);
            break;
        case 12:
            id += '-';
            id += '4';
            break;
        case 16:
            id += '-';
            id += (Math.random() * 4 | 8).toString(16);
            break;
        default:
            // coerce to finite integer
            id += (Math.random() * 16 | 0).toString(16);
        }
    }
    return id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.validateByParamDefList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateByParamDefList (options)](#apidoc.element.n_.context.utility2.validateByParamDefList)
- description and source-code
```javascript
validateByParamDefList = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will validate options.data against options.paramDefList
 */
</span>    var data, key;
    local.tryCatchOnError(function () {
        data = options.data;
        // validate data
        local.assert(data && typeof data === 'object', data);
        (options.paramDefList || []).forEach(function (paramDef) {
            key = paramDef.name;
            // recurse - validateByPropDef
            local.validateByPropDef({
                circularList: options.circularList,
                data: data[key],
                dataReadonlyRemove: (options.dataReadonlyRemove || {})[key],
                key: key,
                schema: paramDef,
                required: paramDef.required,
                'x-swgg-notRequired': paramDef['x-swgg-notRequired']
            });
        });
    }, function (error) {
        error.statusCode = error.statusCode || 400;
        local.errorMessagePrepend(error, options.key + '.' + key + ' -> ');
        throw error;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.validateByPropDef"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateByPropDef (options)](#apidoc.element.n_.context.utility2.validateByPropDef)
- description and source-code
```javascript
validateByPropDef = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will validate options.data against options.schema
 */
</span>    var data, prefix, propDef, tmp;
    local.tryCatchOnError(function () {
        data = options.data;
        prefix = 'property ' + options.key;
        propDef = options.schema;
        // validate undefined data
        if (local.isNullOrUndefined(data)) {
            if (options.required && !options['x-swgg-notRequired']) {
                tmp = new Error(prefix + ' cannot be null or undefined');
                tmp.options = options;
                throw tmp;
            }
            return;
        }
        // handle $ref
        tmp = propDef.$ref || (propDef.schema && propDef.schema.$ref);
        if (tmp) {
            // recurse - validateBySchema
            local.validateBySchema({
                circularList: options.circularList,
                data: data,
                dataReadonlyRemove: options.dataReadonlyRemove,
                key: tmp,
                schema: local.schemaNormalizeAndCopy({ $ref: tmp }),
                'x-swgg-notRequired': options['x-swgg-notRequired']
            });
            return;
        }
        // handle anyOf
        if (propDef.anyOf) {
            tmp = propDef.anyOf.some(function (element) {
                local.tryCatchOnError(function () {
                    // recurse - validateBySchema
                    local.validateBySchema({
                        circularList: options.circularList,
                        data: data,
                        key: 'anyOf',
                        schema: local.schemaNormalizeAndCopy(element),
                        'x-swgg-notRequired': options['x-swgg-notRequired']
                    });
                }, local.nop);
                return !local.utility2._debugTryCatchErrorCaught;
            });
            local.assert(tmp, local.utility2._debugTryCatchErrorCaught);
            return;
        }
        // normalize propDef
        propDef = local.schemaNormalizeAndCopy(options.schema);
        // init circularList
        if (data && typeof data === 'object') {
            options.circularList = options.circularList || [];
            if (options.circularList.indexOf(data) >= 0) {
                return;
            }
            options.circularList.push(data);
        }
        // validate propDef embedded in propDef.schema.type
        if (!propDef.type && propDef.schema && propDef.schema.type) {
            propDef = propDef.schema;
        }
        // http://json-schema.org/latest/json-schema-validation.html#anchor13
        // 5.1.  Validation keywords for numeric instances (number and integer)
        if (typeof data === 'number') {
            if (typeof propDef.multipleOf === 'number') {
                local.assert(
                    data % propDef.multipleOf === 0,
                    prefix + ' must be a multiple of ' + propDef.multipleOf
                );
            }
            if (typeof propDef.maximum === 'number') {
                local.assert(
                    propDef.exclusiveMaximum
                        ? data < propDef.maximum
                        : data <= propDef.maximum,
                    prefix + ' must be ' + (propDef.exclusiveMaximum
                        ? '< '
                        : '<= ') + propDef.maximum
                );
            }
            if (typeof propDef.minimum === 'number') {
                local.assert(
                    propDef.exclusiveMinimum
                        ? data > propDef.minimum
                        : data >= propDef.minimum,
                    prefix + ' must be ' + (propDef.exclusiveMinimum
                        ? '> '
                        : '>= ') + propDef.minimum
                );
            }
        // http://json-schema.org/latest/json-schema-validation.html#anchor25
        // 5.2.  Validation keywords for strings
        } else if (typeof data === 'string') {
            if (propDef.maxLength) {
                local.assert(
                    data.length <= propDef.maxLength,
                    prefix ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.validateBySchema"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateBySchema (options)](#apidoc.element.n_.context.utility2.validateBySchema)
- description and source-code
```javascript
validateBySchema = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will validate options.data against options.schema
 */
</span>    var data, key, prefix, propDefDict, schema, tmp, validateByPropDef;
    // recurse - validateByPropDef
    local.validateByPropDef(options);
    local.tryCatchOnError(function () {
        data = options.data;
        prefix = 'schema ' + options.key;
        schema = options.schema;
        // validate schema
        local.assert(
            schema && typeof schema === 'object',
            prefix + ' must be an object (not ' + typeof schema + ')'
        );
        // init propDefDict
        propDefDict = schema.properties || {};
        // validate data
        local.assert(
            (data && typeof data === 'object') || !Object.keys(propDefDict).length,
            'data for ' + prefix + ' must be an object (not ' + typeof data + ')'
        );
        if (typeof data !== 'object') {
            return;
        }
        validateByPropDef = function (propDef) {
            // remove options.dataReadonlyRemove[key]
            if (propDef.readOnly &&
                    (options.dataReadonlyRemove || {}).hasOwnProperty(key)) {
                delete options.dataReadonlyRemove[key];
            }
            // recurse - validateByPropDef
            local.validateByPropDef({
                circularList: options.circularList,
                data: data[key],
                dataReadonlyRemove: (options.dataReadonlyRemove || {})[key],
                key: key,
                schema: propDef,
                required: schema.required && schema.required.indexOf(key) >= 0,
                'x-swgg-notRequired': options['x-swgg-notRequired']
            });
        };
        Object.keys(propDefDict).forEach(function (_) {
            key = _;
            validateByPropDef(propDefDict[key]);
        });
        Object.keys(data).forEach(function (_) {
            key = _;
            if (propDefDict[key]) {
                return;
            }
            tmp = Object.keys(schema.patternProperties || {}).some(function (_) {
                if (new RegExp(_).test(key)) {
                    validateByPropDef(schema.patternProperties[_]);
                    return true;
                }
            });
            if (tmp) {
                return;
            }
            // https://tools.ietf.org/html/draft-fge-json-schema-validation-00
            // #section-5.4.4
            // validate additionalProperties
            local.assert(
                schema.additionalProperties !== false,
                prefix + ' must not have additionalProperties - ' + key
            );
            if (schema.additionalProperties) {
                validateByPropDef(schema.additionalProperties);
            }
        });
    }, function (error) {
        local.errorMessagePrepend(error, options.key + '.' + key + ' -> ');
        throw error;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.validateBySwagger"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.</span>validateBySwagger (options)](#apidoc.element.n_.context.utility2.validateBySwagger)
- description and source-code
```javascript
validateBySwagger = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will validate the entire swagger json object
 */
</span>    var key, schema, tmp, validateDefault;
    local.validateBySchema({
        data: options,
        key: 'swaggerJson',
        schema: local.swaggerSchemaJson
    });
    // validate default
    validateDefault = function () {
        if (schema.default !== undefined) {
            return;
        }
        local.validateByPropDef({
            data: schema.default,
            key: key + '.default',
            schema: schema
        });
    };
    Object.keys(options.definitions).forEach(function (schemaName) {
        schema = options.definitions[schemaName];
        key = schemaName;
        validateDefault();
        Object.keys(options.definitions[schemaName].properties || {
        }).forEach(function (propName) {
            schema = options.definitions[schemaName].properties[propName];
            key = schemaName + '.' + propName;
            validateDefault();
        });
    });
    Object.keys(options.paths).forEach(function (pathName) {
        Object.keys(options.paths[pathName]).forEach(function (methodName) {
            tmp = options.paths[pathName][methodName];
            Object.keys(tmp.parameters).forEach(function (paramName) {
                schema = tmp.parameters[paramName];
                key = tmp.tags[0] + '.' + tmp.operationId + '.' + paramName;
                validateDefault();
            });
        });
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2.FormData.prototype"></a>[module n_.context.utility2.FormData.prototype](#apidoc.module.n_.context.utility2.FormData.prototype)

#### <a name="apidoc.element.n_.context.utility2.FormData.prototype.append"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.FormData.prototype.</span>append (name, value, filename)](#apidoc.element.n_.context.utility2.FormData.prototype.append)
- description and source-code
```javascript
append = function (name, value, filename) {
<span class="apidocCodeCommentSpan">/*
 * https://xhr.spec.whatwg.org/#dom-formdata-append
 * The append(name, value, filename) method, when invoked, must run these steps:
 * 1. If the filename argument is given, set value to a new File object
 *    whose contents are value and name is filename.
 * 2. Append a new entry whose name is name, and value is value,
 *    to context object's list of entries.
 */
</span>    if (filename) {
        // bug-workaround - chromium cannot assign name to Blob instance
        local.tryCatchOnError(function () {
            value.name = filename;
        }, local.nop);
    }
    this.entryList.push({ name: name, value: value });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.FormData.prototype.read"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.FormData.prototype.</span>read (onError)](#apidoc.element.n_.context.utility2.FormData.prototype.read)
- description and source-code
```javascript
read = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7578
 * this function will read from formData as a buffer, e.g.
 * --Boundary\r\n
 * Content-Disposition: form-data; name="key"\r\n
 * \r\n
 * value\r\n
 * --Boundary\r\n
 * Content-Disposition: form-data; name="input1"; filename="file1.png"\r\n
 * Content-Type: image/jpeg\r\n
 * \r\n
 * <data1>\r\n
 * --Boundary\r\n
 * Content-Disposition: form-data; name="input2"; filename="file2.png"\r\n
 * Content-Type: image/jpeg\r\n
 * \r\n
 * <data2>\r\n
 * --Boundary--\r\n
 */
</span>    var boundary, result;
    // handle null-case
    if (this.entryList.length === 0) {
        onError(null, local.bufferCreate());
        return;
    }
    // init boundary
    boundary = '--' + Date.now().toString(16) + Math.random().toString(16);
    // init result
    result = [];
    local.onParallelList({
        list: this.entryList
    }, function (options, onParallel) {
        var value;
        value = options.element.value;
        if (!(value instanceof local.Blob)) {
            result[options.ii] = [boundary +
                '\r\nContent-Disposition: form-data; name="' + options.element.name +
                '"\r\n\r\n', value, '\r\n'];
            onParallel.counter += 1;
            onParallel();
            return;
        }
        // read from blob in parallel
        onParallel.counter += 1;
        local.blobRead(value, 'binary', function (error, data) {
            result[options.ii] = !error && [boundary +
                '\r\nContent-Disposition: form-data; name="' + options.element.name +
                '"' +
                // read param filename
                (value && value.name
                    ? '; filename="' + value.name + '"'
                    : '') +
                '\r\n' +
                // read param Content-Type
                (value && value.type
                    ? 'Content-Type: ' + value.type + '\r\n'
                    : '') +
                '\r\n', data, '\r\n'];
            onParallel(error);
        });
    }, function (error) {
        // add closing boundary
        result.push([boundary + '--\r\n']);
        // concatenate result
        onError(
            error,
            // flatten result
            !error && local.bufferConcat(Array.prototype.concat.apply([], result))
        );
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2.HtmlReport.prototype"></a>[module n_.context.utility2.HtmlReport.prototype](#apidoc.module.n_.context.utility2.HtmlReport.prototype)

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.fillTemplate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>fillTemplate (e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.fillTemplate)
- description and source-code
```javascript
fillTemplate = function (e, t){var n=this.opts
,r=n.linkMapper;t.entity=e.name||"All files",t.metrics=e.metrics,t.reportClass=getReportClass
(e.metrics.statements,n.watermarks.statements),t.pathHtml=pathTemplate({html:this
.getPathHtml(e,r)}),t.prettify={js:r.asset(e,"prettify.js"),css:r.asset(e,"prettify.css"
)}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.getPathHtml"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>getPathHtml (e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.getPathHtml)
- description and source-code
```javascript
getPathHtml = function (e, t){var n=e.parent,r=[],i=[],s;while(n)r.
push(n),n=n.parent;for(s=0;s<r.length;s+=1)i.push('<a href="'+t.ancestor(e,s+1)+'">'+
(r[s].relativeName||"All files")+"</a>");return i.reverse(),i.length>0?i.join(" &#187; "
)+" &#187; "+e.displayShortName():""}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.standardLinkMapper"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>standardLinkMapper ()](#apidoc.element.n_.context.utility2.HtmlReport.prototype.standardLinkMapper)
- description and source-code
```javascript
standardLinkMapper = function (){return{fromParent:function(e){var t=0,n=
e.relativeName,r;if(SEP!=="/"){n="";for(t=0;t<e.relativeName.length;t+=1)r=e.relativeName
.charAt(t),r===SEP?n+="/":n+=r}return e.kind==="dir"?n+"index.html":n+".html"},ancestorHref
:function(e,t){var n="",r,i,s,o;for(s=0;s<t;s+=1){r=e.relativeName.split(SEP),i=
r.length-1;for(o=0;o<i;o+=1)n+="../";e=e.parent}return n},ancestor:function(e,t)
{return this.ancestorHref(e,t)+"index.html"},asset:function(e,t){var n=0,r=e.parent
;while(r)n+=1,r=r.parent;return this.ancestorHref(e,n)+t}}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.writeDetailPage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeDetailPage (e, t, n)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeDetailPage)
- description and source-code
```javascript
writeDetailPage = function (e, t, n){var r=this.opts,i=r.sourceStore,s=r.templateData
,o=n.code&&Array.isArray(n.code)?n.code.join("\n")+"\n":i.get(n.path),u=o.split(/(?:\r?\n)|\r/
),a=0,f=u.map(function(e){return a+=1,{line:a,covered:null,text:new InsertionText
(e,!0)}}),l;f.unshift({line:0,covered:null,text:new InsertionText("")}),this.fillTemplate
(t,s),e.write(headerTemplate(s)),e.write('<pre><table class="coverage">\n'),annotateLines
(n,f),annotateBranches(n,f),annotateFunctions(n,f),annotateStatements(n,f),f.shift
(),l={structured:f,maxLines:f.length,fileCoverage:n},e.write(detailTemplate(l)),
e.write("</table></pre>\n"),e.write(footerTemplate(s))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.writeFiles"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeFiles ( e, t, n, r)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeFiles)
- description and source-code
```javascript
writeFiles = function ( e, t, n, r){var i=this,s=path.resolve(n,"index.html"),o;this.opts.verbose&&console.
error("Writing "+s),e.writeFile(s,function(e){i.writeIndexPage(e,t)}),t.children
.forEach(function(t){t.kind==="dir"?i.writeFiles(e,t,path.resolve(n,t.relativeName
),r):(o=path.resolve(n,t.relativeName+".html"),i.opts.verbose&&console.error("Writing "+
o),e.writeFile(o,function(e){i.writeDetailPage(e,t,r.fileCoverageFor(t.fullPath(
)))}))})}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.writeIndexPage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeIndexPage ( e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeIndexPage)
- description and source-code
```javascript
writeIndexPage = function ( e, t){var n=this.opts.linkMapper,r=this.opts.templateData,i=Array.prototype.slice
.apply(t.children),s=this.opts.watermarks;i.sort(function(e,t){return e.name<t.name?-1
:1}),this.fillTemplate(t,r),e.write(headerTemplate(r)),e.write(summaryTableHeader
),i.forEach(function(t){var r=t.metrics,i={statements:getReportClass(r.statements
,s.statements),lines:getReportClass(r.lines,s.lines),functions:getReportClass(r.
functions,s.functions),branches:getReportClass(r.branches,s.branches)},o={metrics
:r,reportClasses:i,file:t.displayShortName(),output:n.fromParent(t)};e.write(summaryLineTemplate
(o)+"\n")}),e.write(summaryTableFooter),e.write(footerTemplate(r))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.HtmlReport.prototype.writeReport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.HtmlReport.prototype.</span>writeReport ( e, t)](#apidoc.element.n_.context.utility2.HtmlReport.prototype.writeReport)
- description and source-code
```javascript
writeReport = function ( e, t){var n=this.opts,r=n.dir,i=new TreeSummarizer,s=n.writer||new FileWriter(t),
o;e.files().forEach(function(t){i.addFileCoverageSummary(t,utils.summarizeFileCoverage
(e.fileCoverageFor(t)))}),o=i.getTreeSummary(),fs.readdirSync(path.resolve(__dirname
,"..","vendor")).forEach(function(e){var t=path.resolve(__dirname,"..","vendor",
e),i=path.resolve(r,e),o=fs.statSync(t);o.isFile()&&(n.verbose&&console.log("Write asset: "+
i),s.copyFile(t,i))}),this.writeFiles(s,o.root,r,e)}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2.Instrumenter.prototype"></a>[module n_.context.utility2.Instrumenter.prototype](#apidoc.module.n_.context.utility2.Instrumenter.prototype)

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.arrowBlockConverter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>arrowBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.arrowBlockConverter)
- description and source-code
```javascript
arrowBlockConverter = function (e){var t;e.expression&&(t=f.returnStatement(e.body),t.loc=e.body.loc,e
.body=this.convertToBlock(t),e.expression=!1)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.branchIncrementExprAst"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchIncrementExprAst (e, t , n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchIncrementExprAst)
- description and source-code
```javascript
branchIncrementExprAst = function (e, t , n){var r=f.postIncrement(f.subscript(f.subscript(f.dot(f.variable(this.currentState
.trackerVar),f.variable("b")),f.stringLiteral(e)),f.numericLiteral(t)),n);return r
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.branchLocationFor"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchLocationFor (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchLocationFor)
- description and source-code
```javascript
branchLocationFor = function (e, t){return this.coverState.branchMap[e]
.locations[t]}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.branchName"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>branchName (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.branchName)
- description and source-code
```javascript
branchName = function (e, t, n){var r,i=[],s=[],o,u=!!this.currentState.ignoring;this.currentState
.branch+=1,r=this.currentState.branch;for(o=0;o<n.length;o+=1)n[o].skip=n[o].skip||
u||undefined,s.push(n[o]),i.push(0);return this.coverState.b[r]=i,this.coverState
.branchMap[r]={line:t,type:e,locations:s},r}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.conditionalBranchInjector"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>conditionalBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.conditionalBranchInjector)
- description and source-code
```javascript
conditionalBranchInjector = function (e, t){var n=this.branchName
("cond-expr",t.startLineForNode(e),this.locationsForNodes([e.consequent,e.alternate
])),r=this.branchIncrementExprAst(n,0),i=this.branchIncrementExprAst(n,1);e.consequent
.preprocessor=this.maybeAddSkip(this.branchLocationFor(n,0)),e.alternate.preprocessor=
this.maybeAddSkip(this.branchLocationFor(n,1)),e.consequent=f.sequence(r,e.consequent
),e.alternate=f.sequence(i,e.alternate)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.convertToBlock"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>convertToBlock (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.convertToBlock)
- description and source-code
```javascript
convertToBlock = function (e){return e?e.type==="BlockStatement"?
e:{type:"BlockStatement",body:[e]}:{type:"BlockStatement",body:[]}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.coverFunction"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>coverFunction (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.coverFunction)
- description and source-code
```javascript
coverFunction = function (e, t){var n,r=e.body,i=r.body,s;this.maybeSkipNode(e,"next"),n=this.functionName
(e,t.startLineForNode(e),{start:e.loc.start,end:{line:e.body.loc.start.line,column
:e.body.loc.start.column}}),i.length>0&&this.isUseStrictExpression(i[0])&&(s=i.shift
()),i.unshift(f.statement(f.postIncrement(f.subscript(f.dot(f.variable(this.currentState
.trackerVar),f.variable("f")),f.stringLiteral(n))))),s&&i.unshift(s)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.coverStatement"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>coverStatement (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.coverStatement)
- description and source-code
```javascript
coverStatement = function (e, n){var r,i,s
;this.maybeSkipNode(e,"next");if(this.isUseStrictExpression(e)){s=n.ancestor(2);
if(s&&(s.node.type===t.FunctionExpression.name||s.node.type===t.FunctionDeclaration
.name)&&n.parent().node.body[0]===e)return}e.type===t.FunctionDeclaration.name?r=
this.statementName(e.loc,1):(r=this.statementName(e.loc),i=f.statement(f.postIncrement
(f.subscript(f.dot(f.variable(this.currentState.trackerVar),f.variable("s")),f.stringLiteral
(r)))),this.splice(i,e,n))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.endIgnore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>endIgnore ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.endIgnore)
- description and source-code
```javascript
endIgnore = function ()
{this.currentState.ignoring-=1}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.extractCurrentHint"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>extractCurrentHint (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.extractCurrentHint)
- description and source-code
```javascript
extractCurrentHint = function (e){if(!e.range)return;
var t=this.currentState.lastHintPosition+1,n=this.currentState.hints,r=e.range[0
],i;this.currentState.currentHint=null;while(t<n.length){i=n[t];if(!(i.end<r))break;
this.currentState.currentHint=i,this.currentState.lastHintPosition=t,t+=1}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.filterHints"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>filterHints (e )](#apidoc.element.n_.context.utility2.Instrumenter.prototype.filterHints)
- description and source-code
```javascript
filterHints = function (e ){var t=[],n,r,i;if(!e||!h(e))return t;for(n=0;n<e.length;n+=1)r=e[n],r&&r.value&&
r.range&&h(r.range)&&(i=String(r.value).match(a),i&&t.push({type:i[1],start:r.range
[0],end:r.range[1]}));return t}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.findLeaves"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>findLeaves ( e, n, r, i)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.findLeaves)
- description and source-code
```javascript
findLeaves = function ( e, n, r, i){e.type===t.LogicalExpression.name?(this.findLeaves(e.left,n,e,"left"),this
.findLeaves(e.right,n,e,"right")):n.push({node:e,parent:r,property:i})}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.fixColumnPositions"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>fixColumnPositions (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.fixColumnPositions)
- description and source-code
```javascript
fixColumnPositions = function (e){var t=o.length
,n=function(e){e.start.line===1&&(e.start.column-=t),e.end.line===1&&(e.end.column-=
t)},r,i,s,u;i=e.statementMap;for(r in i)i.hasOwnProperty(r)&&n(i[r]);i=e.fnMap;for(
r in i)i.hasOwnProperty(r)&&n(i[r].loc);i=e.branchMap;for(r in i)if(i.hasOwnProperty
(r)){u=i[r].locations;for(s=0;s<u.length;s+=1)n(u[s])}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.functionName"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>functionName (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.functionName)
- description and source-code
```javascript
functionName = function (e, t, n){this
.currentState.func+=1;var r=this.currentState.func,i=!!this.currentState.ignoring
,s=e.id?e.id.name:"(anonymous_"+r+")",o=function(e){var t=n[e]||{};return{line:t
.line,column:t.column}};return this.coverState.fnMap[r]={name:s,line:t,loc:{start
:o("start"),end:o("end")},skip:i||undefined},this.coverState.f[r]=0,r}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.getPreamble"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>getPreamble (e, t )](#apidoc.element.n_.context.utility2.Instrumenter.prototype.getPreamble)
- description and source-code
```javascript
getPreamble = function (e, t ){var n=this.opts.coverageVariable||"__coverage__",r=this.coverState.path.replace
(/\\/g,"\\\\"),i=this.currentState.trackerVar,s,o=t?'"use strict";':"",u=function(
e){return function(){return e}},a;return this.opts.noAutoWrap||this.fixColumnPositions
(this.coverState),this.opts.embedSource&&(this.coverState.code=e.split(/(?:\r?\n)|\r/
)),s=this.opts.debug?JSON.stringify(this.coverState,undefined,4):JSON.stringify(
this.coverState),a=["%STRICT%","var %VAR% = (Function('return this'))();","if (!%VAR%.%GLOBAL%) { %VAR%.%GLOBAL% = {}; }"
,"%VAR% = %VAR%.%GLOBAL%;","if (!(%VAR%['%FILE%'])) {","   %VAR%['%FILE%'] = %OBJECT%;"
,"}","%VAR% = %VAR%['%FILE%'];"].join("\n").replace(/%STRICT%/g,u(o)).replace(/%VAR%/g
,u(i)).replace(/%GLOBAL%/g,u(n)).replace(/%FILE%/g,u(r)).replace(/%OBJECT%/g,u(s
)),a}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBlockConverter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>ifBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBlockConverter)
- description and source-code
```javascript
ifBlockConverter = function (e){e
.consequent=this.convertToBlock(e.consequent),e.alternate=this.convertToBlock(e.
alternate)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBranchInjector"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>ifBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.ifBranchInjector)
- description and source-code
```javascript
ifBranchInjector = function (e, t){var n=!!this.currentState.ignoring,r=
this.currentState.currentHint,i=!n&&r&&r.type==="if",s=!n&&r&&r.type==="else",o=
e.loc.start.line,u=e.loc.start.column,a=function(){return{line:o,column:u}},l=this
.branchName("if",t.startLineForNode(e),[{start:a(),end:a(),skip:i||undefined},{start
:a(),end:a(),skip:s||undefined}]),c=e.consequent.body,h=e.alternate.body,p;c.unshift
(f.statement(this.branchIncrementExprAst(l,0))),h.unshift(f.statement(this.branchIncrementExprAst
(l,1))),i&&(p=e.consequent,p.preprocessor=this.startIgnore,p.postprocessor=this.
endIgnore),s&&(p=e.alternate,p.preprocessor=this.startIgnore,p.postprocessor=this
.endIgnore)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.instrument"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrument (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrument)
- description and source-code
```javascript
instrument = function (e, t, n){!n&&typeof t=="function"&&(n=t,t=null);try{n(null,this.instrumentSync
(e,t))}catch(r){n(r)}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentASTSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrumentASTSync (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentASTSync)
- description and source-code
```javascript
instrumentASTSync = function (e, t, n){var r=!1,s,o,u,a,f;t=t||String((new Date).getTime())+".js",this
.sourceMap=null,this.coverState={path:t,s:{},b:{},f:{},fnMap:{},statementMap:{},
branchMap:{}},this.currentState={trackerVar:p(t,this.omitTrackerSuffix),func:0,branch
:0,variable:0,statement:0,hints:this.filterHints(e.comments),currentHint:null,lastHintPosition
:-1,ignoring:0},e.body&&e.body.length>0&&this.isUseStrictExpression(e.body[0])&&
(e.body.shift(),r=!0),this.walker.startWalk(e),s=this.opts.codeGenerationOptions||
{format:{compact:!this.opts.noCompact}},s.comment=this.opts.preserveComments,o=i
.generate(e,s),u=this.getPreamble(n||"",r);if(o.map&&o.code){a=u.split(/\r\n|\r|\n/
).length;for(f=0;f<o.map._mappings._array.length;f+=1)o.map._mappings._array[f].
generatedLine+=a;this.sourceMap=o.map,o=o.code}return u+"\n"+o+"\n"}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>instrumentSync (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.instrumentSync)
- description and source-code
```javascript
instrumentSync = function (e, n){var s;if(typeof e!="string")throw new
Error("Code must be string");return e.charAt(0)==="#"&&(e="//"+e),this.opts.noAutoWrap||
(e=o+e+u),s=r.parse(e,{loc:!0,range:!0,tokens:this.opts.preserveComments,comment
:!0}),this.opts.preserveComments&&(s=i.attachComments(s,s.comments,s.tokens)),this
.opts.noAutoWrap||(s={type:t.Program.name,body:s.body[0].expression.callee.body.
body,comments:s.comments}),this.instrumentASTSync(s,n,e)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.isUseStrictExpression"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>isUseStrictExpression (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.isUseStrictExpression)
- description and source-code
```javascript
isUseStrictExpression = function (e){return e&&e.type===
t.ExpressionStatement.name&&e.expression&&e.expression.type===t.Literal.name&&e.
expression.value==="use strict"}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.lastFileCoverage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>lastFileCoverage ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.lastFileCoverage)
- description and source-code
```javascript
lastFileCoverage = function (){return this.coverState}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.lastSourceMap"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>lastSourceMap ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.lastSourceMap)
- description and source-code
```javascript
lastSourceMap = function (){return this.sourceMap}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.locationsForNodes"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>locationsForNodes (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.locationsForNodes)
- description and source-code
```javascript
locationsForNodes = function (e){var t=[],n;for(n=0;n<e.length;n+=1)t.push(e[n].loc
);return t}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.logicalExpressionBranchInjector"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>logicalExpressionBranchInjector (e, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.logicalExpressionBranchInjector)
- description and source-code
```javascript
logicalExpressionBranchInjector = function (e, n){var r=n.parent(),i=[],s,
o,u;this.maybeSkipNode(e,"next");if(r&&r.node.type===t.LogicalExpression.name)return;
this.findLeaves(e,i),s=this.branchName("binary-expr",n.startLineForNode(e),this.
locationsForNodes(i.map(function(e){return e.node})));for(u=0;u<i.length;u+=1)o=
i[u],o.parent[o.property]=f.sequence(this.branchIncrementExprAst(s,u),o.node),o.
node.preprocessor=this.maybeAddSkip(this.branchLocationFor(s,u))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.loopBlockConverter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>loopBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.loopBlockConverter)
- description and source-code
```javascript
loopBlockConverter = function (e){e.body=this.convertToBlock(e.body)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddSkip"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeAddSkip (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddSkip)
- description and source-code
```javascript
maybeAddSkip = function (e){return function(
t){var n=!!this.currentState.ignoring,r=this.currentState.currentHint,i=!n&&r&&r
.type==="next";i&&(this.startIgnore(),t.postprocessor=this.endIgnore);if(i||n)e.
skip=!0}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddType"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeAddType (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeAddType)
- description and source-code
```javascript
maybeAddType = function (e){var n=e.properties,r,i;for(r=0;r<n.length;r+=1)i=n[r],i.type||(i.type=
t.Property.name)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeSkipNode"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>maybeSkipNode (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.maybeSkipNode)
- description and source-code
```javascript
maybeSkipNode = function (e, t){var n=!!this.currentState
.ignoring,r=this.currentState.currentHint,i=!n&&r&&r.type===t;return i?(this.startIgnore
(),e.postprocessor=this.endIgnore,!0):!1}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.paranoidHandlerCheck"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>paranoidHandlerCheck (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.paranoidHandlerCheck)
- description and source-code
```javascript
paranoidHandlerCheck = function (e){!
e.handler&&e.handlers&&(e.handler=e.handlers[0])}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.skipInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>skipInit (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.skipInit)
- description and source-code
```javascript
skipInit = function (e){e.init&&(e.init.skipWalk=!0)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.skipLeft"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>skipLeft (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.skipLeft)
- description and source-code
```javascript
skipLeft = function (e){e.left.skipWalk=!0}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.splice"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>splice (e, t, n)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.splice)
- description and source-code
```javascript
splice = function (e, t, n){var r=n.isLabeled()?n.parent(
).node:t;r.prepend=r.prepend||[],d(r.prepend,e)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.startIgnore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>startIgnore ()](#apidoc.element.n_.context.utility2.Instrumenter.prototype.startIgnore)
- description and source-code
```javascript
startIgnore = function (){this.currentState.ignoring+=1}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.statementName"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>statementName (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.statementName)
- description and source-code
```javascript
statementName = function (e, t){var n
,r=!!this.currentState.ignoring;return e.skip=r||undefined,t=t||0,this.currentState
.statement+=1,n=this.currentState.statement,this.coverState.statementMap[n]=e,this
.coverState.s[n]=t,n}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.switchBranchInjector"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>switchBranchInjector (e, t)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.switchBranchInjector)
- description and source-code
```javascript
switchBranchInjector = function (e, t){var n=e.cases,r,i;if(!(n&&n.length>0
))return;r=this.branchName("switch",t.startLineForNode(e),this.locationsForNodes
(n));for(i=0;i<n.length;i+=1)n[i].branchLocation=this.branchLocationFor(r,i),n[i
].consequent.unshift(f.statement(this.branchIncrementExprAst(r,i)))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.switchCaseInjector"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>switchCaseInjector (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.switchCaseInjector)
- description and source-code
```javascript
switchCaseInjector = function (e){var t=e.branchLocation;delete e.branchLocation,this.maybeSkipNode(e
,"next")&&(t.skip=!0)}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2.Instrumenter.prototype.withBlockConverter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.Instrumenter.prototype.</span>withBlockConverter (e)](#apidoc.element.n_.context.utility2.Instrumenter.prototype.withBlockConverter)
- description and source-code
```javascript
withBlockConverter = function (e){e.body=this.convertToBlock(e.body)}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2.TextReport.prototype"></a>[module n_.context.utility2.TextReport.prototype](#apidoc.module.n_.context.utility2.TextReport.prototype)

#### <a name="apidoc.element.n_.context.utility2.TextReport.prototype.writeReport"></a>[function <span class="apidocSignatureSpan">n_.context.utility2.TextReport.prototype.</span>writeReport (e)](#apidoc.element.n_.context.utility2.TextReport.prototype.writeReport)
- description and source-code
```javascript
writeReport = function (e){var t=new TreeSummarizer,n,r,i,s=4*(PCT_COLS+2),o,u=[]
,a;e.files().forEach(function(n){t.addFileCoverageSummary(n,utils.summarizeFileCoverage
(e.fileCoverageFor(n)))}),n=t.getTreeSummary(),r=n.root,i=findNameWidth(r),this.
maxCols>0&&(o=this.maxCols-s-2,i>o&&(i=o)),walk(r,i,u,0,this.watermarks),a=u.join
("\n")+"\n",this.file?(mkdirp.sync(this.dir),fs.writeFileSync(path.join(this.dir
,this.file),a,"utf8")):console.log(a)}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2._DbTable.prototype"></a>[module n_.context.utility2._DbTable.prototype](#apidoc.module.n_.context.utility2._DbTable.prototype)

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._cleanup"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_cleanup ()](#apidoc.element.n_.context.utility2._DbTable.prototype._cleanup)
- description and source-code
```javascript
_cleanup = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will cleanup soft-deleted records from the dbTable
 */
</span>    var dbRow, ii, list, ttl;
    ttl = Date.now();
    if (!(this.isDirty ||
          // cleanup ttl every minute
          (this.ttl && this.ttlLast + this.ttl < ttl))) {
        return;
    }
    this.isDirty = null;
    this.ttlLast = ttl;
    // cleanup dbRowList
    list = this.dbRowList;
    this.dbRowList = [];
    // optimization - for-loop
    for (ii = 0; ii < list.length; ii += 1) {
        dbRow = list[ii];
        // cleanup ttl
        if (this.ttl && dbRow.$meta.ttl < ttl) {
            this._crudRemoveOneById(dbRow);
        // cleanup isRemoved
        } else if (!dbRow.$meta.isRemoved) {
            this.dbRowList.push(dbRow);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._crudGetManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudGetManyByQuery (query)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudGetManyByQuery)
- description and source-code
```javascript
_crudGetManyByQuery = function (query) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow's in the dbTable with the given query
 */
</span>    return local.dbRowListGetManyByQuery(this.dbRowList, local.normalizeDict(query));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._crudGetOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudGetOneById (idDict)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudGetOneById)
- description and source-code
```javascript
_crudGetOneById = function (idDict) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow in the dbTable with the given idDict
 */
</span>    var id, result;
    idDict = local.normalizeDict(idDict);
    result = null;
    this.idIndexList.some(function (idIndex) {
        id = idDict[idIndex.name];
        // optimization - hasOwnProperty
        if (idIndex.dict.hasOwnProperty(id)) {
            result = idIndex.dict[id];
            return result;
        }
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._crudRemoveOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudRemoveOneById (idDict, circularList)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudRemoveOneById)
- description and source-code
```javascript
_crudRemoveOneById = function (idDict, circularList) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the dbRow from the dbTable with the given idDict
 */
</span>    var id, result, self;
    if (!idDict) {
        return null;
    }
    self = this;
    circularList = circularList || [idDict];
    result = null;
    self.idIndexList.forEach(function (idIndex) {
        id = idDict[idIndex.name];
        // optimization - hasOwnProperty
        if (!idIndex.dict.hasOwnProperty(id)) {
            return;
        }
        result = idIndex.dict[id];
        delete idIndex.dict[id];
        // optimization - soft-delete
        result.$meta.isRemoved = true;
        self.isDirty = true;
        if (circularList.indexOf(result) >= 0) {
            return;
        }
        circularList.push(result);
        // recurse
        self._crudRemoveOneById(result, circularList);
    });
    self.save();
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._crudSetOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudSetOneById (dbRow)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudSetOneById)
- description and source-code
```javascript
_crudSetOneById = function (dbRow) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the dbRow into the dbTable with the given dbRow._id
 * WARNING - existing dbRow with conflicting dbRow._id will be removed
 */
</span>    var existing, id, normalize, timeNow;
    normalize = function (dbRow) {
    /*
     * this function will recursively normalize dbRow
     */
        if (dbRow && typeof dbRow === 'object') {
            Object.keys(dbRow).forEach(function (key) {
                // remove invalid property
                if (key[0] === '$' || key.indexOf('.') >= 0 || dbRow[key] === null) {
                    // optimization - soft-delete
                    dbRow[key] = undefined;
                    return;
                }
                // recurse
                normalize(dbRow[key]);
            });
        }
    };
    dbRow = local.jsonCopy(dbRow && typeof dbRow === 'object'
        ? dbRow
        : {});
    // update timestamp
    timeNow = new Date().toISOString();
    dbRow._timeCreated = dbRow._timeCreated || timeNow;
    if (!local.modeImport) {
        dbRow._timeUpdated = timeNow;
    }
    // normalize
    normalize(dbRow);
    dbRow = local.jsonCopy(dbRow);
    // remove existing dbRow
    existing = this._crudRemoveOneById(dbRow) || dbRow;
    // init meta
    dbRow.$meta = { isRemoved: null, ttl: this.ttl + Date.now() };
    this.idIndexList.forEach(function (idIndex) {
        // auto-set id
        id = local.dbRowSetId(existing, idIndex);
        // copy id from existing to dbRow
        dbRow[idIndex.name] = id;
        // set dbRow
        idIndex.dict[id] = dbRow;
    });
    // update dbRowList
    this.dbRowList.push(dbRow);
    this.save();
    return dbRow;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype._crudUpdateOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>_crudUpdateOneById (dbRow)](#apidoc.element.n_.context.utility2._DbTable.prototype._crudUpdateOneById)
- description and source-code
```javascript
_crudUpdateOneById = function (dbRow) {
<span class="apidocCodeCommentSpan">/*
 * this function will update the dbRow in the dbTable,
 * if it exists with the given dbRow._id
 * WARNING
 * existing dbRow's with conflicting unique-keys (besides the one being updated)
 * will be removed
 */
</span>    var id, result;
    dbRow = local.jsonCopy(local.normalizeDict(dbRow));
    result = null;
    this.idIndexList.some(function (idIndex) {
        id = dbRow[idIndex.name];
        // optimization - hasOwnProperty
        if (idIndex.dict.hasOwnProperty(id)) {
            result = idIndex.dict[id];
            return true;
        }
    });
    result = result || {};
    // remove existing dbRow
    this._crudRemoveOneById(result);
    // update dbRow
    dbRow._timeCreated = undefined;
    local.objectSetOverride(result, dbRow, Infinity);
    // replace dbRow
    result = this._crudSetOneById(result);
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudCountAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudCountAll (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudCountAll)
- description and source-code
```javascript
crudCountAll = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will count all of dbRow's in the dbTable
 */
</span>    this._cleanup();
    return local.setTimeoutOnError(onError, null, this.dbRowList.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudCountManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudCountManyByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudCountManyByQuery)
- description and source-code
```javascript
crudCountManyByQuery = function (query, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will count the number of dbRow's in the dbTable with the given query
 */
</span>    this._cleanup();
    return local.setTimeoutOnError(
        onError,
        null,
        this._crudGetManyByQuery(query).length
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetManyById (idDictList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyById)
- description and source-code
```javascript
crudGetManyById = function (idDictList, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow's in the dbTable with the given idDictList
 */
</span>    var self;
    this._cleanup();
    self = this;
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        local.normalizeList(idDictList).map(function (idDict) {
            return self._crudGetOneById(idDict);
        })
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetManyByQuery)
- description and source-code
```javascript
crudGetManyByQuery = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow's in the dbTable with the given options.query
 */
</span>    var result;
    this._cleanup();
    options = local.normalizeDict(options);
    // get dbRow's with the given options.query
    result = this._crudGetManyByQuery(options.query);
    // sort dbRow's with the given options.sort
    local.normalizeList(options.sort || this.sortDefault).forEach(function (element) {
        if (element.isDescending) {
            result.sort(function (aa, bb) {
                return -local.sortCompare(
                    local.dbRowGetItem(aa, element.fieldName),
                    local.dbRowGetItem(bb, element.fieldName)
                );
            });
        } else {
            result.sort(function (aa, bb) {
                return local.sortCompare(
                    local.dbRowGetItem(aa, element.fieldName),
                    local.dbRowGetItem(bb, element.fieldName)
                );
            });
        }
    });
    // skip and limit dbRow's with the given options.skip and options.limit
    result = result.slice(
        options.skip || 0,
        (options.skip || 0) + (options.limit || Infinity)
    );
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        result,
        options.fieldList
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneById (idDict, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneById)
- description and source-code
```javascript
crudGetOneById = function (idDict, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow in the dbTable with the given idDict
 */
</span>    this._cleanup();
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        this._crudGetOneById(idDict)
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByQuery)
- description and source-code
```javascript
crudGetOneByQuery = function (query, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the dbRow in the dbTable with the given query
 */
</span>    var ii, result;
    this._cleanup();
    // optimization - for-loop
    for (ii = 0; ii < this.dbRowList.length; ii += 1) {
        result = local.dbRowListGetManyByQuery([this.dbRowList[ii]], query)[0];
        if (result) {
            break;
        }
    }
    return local.setTimeoutOnError(onError, null, local.dbRowProject(result));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByRandom"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudGetOneByRandom (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudGetOneByRandom)
- description and source-code
```javascript
crudGetOneByRandom = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will get a random dbRow in the dbTable
 */
</span>    this._cleanup();
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        this.dbRowList[Math.floor(Math.random() * this.dbRowList.length)]
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveAll (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveAll)
- description and source-code
```javascript
crudRemoveAll = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove all of the dbRow's from the dbTable
 */
</span>    var idIndexList;
    // save idIndexList
    idIndexList = this.idIndexList;
    // reset dbTable
    local._DbTable.call(this, this);
    // restore idIndexList
    local.dbTableCreateOne({
        name: this.name,
        idIndexCreateList: idIndexList
    }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveManyById (idDictList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyById)
- description and source-code
```javascript
crudRemoveManyById = function (idDictList, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the dbRow's from the dbTable with the given idDictList
 */
</span>    var self;
    self = this;
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        local.normalizeList(idDictList).map(function (dbRow) {
            return self._crudRemoveOneById(dbRow);
        })
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveManyByQuery (query, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveManyByQuery)
- description and source-code
```javascript
crudRemoveManyByQuery = function (query, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the dbRow's from the dbTable with the given query
 */
</span>    var self;
    self = this;
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        self._crudGetManyByQuery(query).map(function (dbRow) {
            return self._crudRemoveOneById(dbRow);
        })
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudRemoveOneById (idDict, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudRemoveOneById)
- description and source-code
```javascript
crudRemoveOneById = function (idDict, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the dbRow from the dbTable with the given idDict
 */
</span>    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        this._crudRemoveOneById(idDict)
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudSetManyById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudSetManyById (dbRowList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudSetManyById)
- description and source-code
```javascript
crudSetManyById = function (dbRowList, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the dbRowList into the dbTable
 */
</span>    var self;
    self = this;
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        local.normalizeList(dbRowList).map(function (dbRow) {
            return self._crudSetOneById(dbRow);
        })
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudSetOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudSetOneById (dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudSetOneById)
- description and source-code
```javascript
crudSetOneById = function (dbRow, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the dbRow into the dbTable with the given dbRow._id
 */
</span>    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        this._crudSetOneById(dbRow)
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateManyById (dbRowList, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyById)
- description and source-code
```javascript
crudUpdateManyById = function (dbRowList, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will update the dbRowList in the dbTable,
 * if they exist with the given dbRow._id's
 */
</span>    var self;
    self = this;
    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        local.normalizeList(dbRowList).map(function (dbRow) {
            return self._crudUpdateOneById(dbRow);
        })
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateManyByQuery (query, dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateManyByQuery)
- description and source-code
```javascript
crudUpdateManyByQuery = function (query, dbRow, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will update the dbRow's in the dbTable with the given query
 */
</span>    var result, self, tmp;
    self = this;
    tmp = local.jsonCopy(local.normalizeDict(dbRow));
    result = self._crudGetManyByQuery(query).map(function (dbRow) {
        tmp._id = dbRow._id;
        return self._crudUpdateOneById(tmp);
    });
    return local.setTimeoutOnError(onError, null, result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateOneById"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>crudUpdateOneById (dbRow, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.crudUpdateOneById)
- description and source-code
```javascript
crudUpdateOneById = function (dbRow, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will update the dbRow in the dbTable,
 * if it exists with the given dbRow._id
 */
</span>    return local.setTimeoutOnError(onError, null, local.dbRowProject(
        this._crudUpdateOneById(dbRow)
    ));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.drop"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>drop (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.drop)
- description and source-code
```javascript
drop = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will drop the dbTable
 */
</span>    console.error('dropping dbTable ' + this.name + ' ...');
    // cancel pending save
    this.timerSave = null;
    while (this.onSaveList.length) {
        this.onSaveList.shift()();
    }
    // reset dbTable
    local._DbTable.call(this, this);
    // clear persistence
    local.storageRemoveItem('dbTable.' + this.name, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.export"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>export (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.export)
- description and source-code
```javascript
export = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will export the db
 */
</span>    var result, self;
    this._cleanup();
    self = this;
    result = '';
    result += self.name + ' ttlSet ' + self.ttl + '\n';
    self.idIndexList.forEach(function (idIndex) {
        result += self.name + ' idIndexCreate ' + JSON.stringify({
            isInteger: idIndex.isInteger,
            name: idIndex.name
        }) + '\n';
    });
    result += self.name + ' sortDefault ' + JSON.stringify(self.sortDefault) + '\n';
    self.crudGetManyByQuery({}).forEach(function (dbRow) {
        result += self.name + ' dbRowSet ' + JSON.stringify(dbRow) + '\n';
    });
    return local.setTimeoutOnError(onError, null, result.trim());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.idIndexCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>idIndexCreate (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.idIndexCreate)
- description and source-code
```javascript
idIndexCreate = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create an idIndex with the given options.name
 */
</span>    var dbRow, idIndex, ii, name;
    options = local.normalizeDict(options);
    name = String(options.name);
    // disallow idIndex with dot-name
    if (name.indexOf('.') >= 0 || name === '_id') {
        return local.setTimeoutOnError(onError);
    }
    // remove existing idIndex
    this.idIndexRemove(options);
    // init idIndex
    idIndex = {
        dict: {},
        isInteger: options.isInteger,
        name: options.name
    };
    this.idIndexList.push(idIndex);
    // populate idIndex with dbRowList
    // optimization - for-loop
    for (ii = 0; ii < this.dbRowList.length; ii += 1) {
        dbRow = this.dbRowList[ii];
        // auto-set id
        if (!dbRow.$meta.isRemoved) {
            idIndex.dict[local.dbRowSetId(dbRow, idIndex)] = dbRow;
        }
    }
    this.save();
    return local.setTimeoutOnError(onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.idIndexRemove"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>idIndexRemove (options, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.idIndexRemove)
- description and source-code
```javascript
idIndexRemove = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the idIndex with the given options.name
 */
</span>    var name;
    options = local.normalizeDict(options);
    name = String(options.name);
    this.idIndexList = this.idIndexList.filter(function (idIndex) {
        return idIndex.name !== name || idIndex.name === '_id';
    });
    this.save();
    return local.setTimeoutOnError(onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.save"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>save (onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.save)
- description and source-code
```javascript
save = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will save the dbTable to storage
 */
</span>    var self;
    self = this;
    if (local.modeImport) {
        return;
    }
    if (onError) {
        self.onSaveList.push(onError);
    }
    // throttle storage-writes to once every 1000 ms
    self.timerSave = self.timerSave || setTimeout(function () {
        self.timerSave = null;
        local.storageSetItem('dbTable.' + self.name + '.json', self.export(), function (
            error
        ) {
            while (self.onSaveList.length) {
                self.onSaveList.shift()(error);
            }
        });
    }, 1000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2._DbTable.prototype.ttlSet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2._DbTable.prototype.</span>ttlSet (ttl, onError)](#apidoc.element.n_.context.utility2._DbTable.prototype.ttlSet)
- description and source-code
```javascript
ttlSet = function (ttl, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the ttl in milliseconds
 */
</span>    var ii;
    // set ttl in milliseconds
    this.ttl = ttl;
    // update dbRowList
    ttl += Date.now();
    // optimization - for-loop
    for (ii = 0; ii < this.dbRowList.length; ii += 1) {
        this.dbRowList[ii].$meta.ttl = ttl;
    }
    this.save();
    return local.setTimeoutOnError(onError);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2_moduleExports"></a>[module n_.context.utility2_moduleExports](#apidoc.module.n_.context.utility2_moduleExports)

#### <a name="apidoc.element.n_.context.utility2_moduleExports.Blob"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>Blob (array, options)](#apidoc.element.n_.context.utility2_moduleExports.Blob)
- description and source-code
```javascript
Blob = function (array, options) {
<span class="apidocCodeCommentSpan">  /*
   * this function will create a node-compatible Blob instance
   */
</span>    this.bff = local.bufferConcat(array);
    this.type = options && options.type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.FormData"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>FormData ()](#apidoc.element.n_.context.utility2_moduleExports.FormData)
- description and source-code
```javascript
FormData = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a serverLocal-compatible FormData instance
 * https://xhr.spec.whatwg.org/#dom-formdata
 * The FormData(form) constructor must run these steps:
 * 1. Let fd be a new FormData object.
 * 2. If form is given, set fd's entries to the result
 *    of constructing the form data set for form. (not implemented)
 * 3. Return fd.
 */
</span>    this.entryList = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.Module"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>Module (id, parent)](#apidoc.element.n_.context.utility2_moduleExports.Module)
- description and source-code
```javascript
function Module(id, parent) {
  this.id = id;
  this.exports = {};
  this.parent = parent;
  if (parent && parent.children) {
    parent.children.push(this);
  }

  this.filename = null;
  this.loaded = false;
  this.children = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.__require"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>__require (path)](#apidoc.element.n_.context.utility2_moduleExports.__require)
- description and source-code
```javascript
function require(path) {
  try {
    exports.requireDepth += 1;
    return self.require(path);
  } finally {
    exports.requireDepth -= 1;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports._middlewareError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_middlewareError (error, request, response)](#apidoc.element.n_.context.utility2_moduleExports._middlewareError)
- description and source-code
```javascript
_middlewareError = function (error, request, response) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will handle errors
 */
</span>    // if error occurred, then respond with '500 Internal Server Error',
    // else respond with '404 Not Found'
    local.serverRespondDefault(request, response, error
        ? (error.statusCode >= 400 && error.statusCode < 600
            ? error.statusCode
            : 500)
        : 404, error);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports._middlewareJsonpStateInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_middlewareJsonpStateInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports._middlewareJsonpStateInit)
- description and source-code
```javascript
_middlewareJsonpStateInit = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * serve the browser-state wrapped in the given jsonp-callback
 */
</span>    var state;
    if (request._stateInit || (request.urlParsed &&
            request.urlParsed.pathname === '/jsonp.utility2._stateInit')) {
        state = { utility2: { assetsDict: {
            '/assets.index.template.html':
                local.assetsDict['/assets.index.template.html']
        } } };
        local.objectSetDefault(state, { utility2: { env: {
            NODE_ENV: local.env.NODE_ENV,
            npm_config_mode_backend: local.env.npm_config_mode_backend,
            npm_package_description: local.env.npm_package_description,
            npm_package_homepage: local.env.npm_package_homepage,
            npm_package_name: local.env.npm_package_name,
            npm_package_nameAlias: local.env.npm_package_nameAlias,
            npm_package_version: local.env.npm_package_version
        } } }, 3);
        if (request._stateInit) {
            return state;
        }
        response.end(
            request.urlParsed.query.callback + '(' + JSON.stringify(state) + ');'
        );
        return;
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports._serverLocalUrlTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_serverLocalUrlTest ()](#apidoc.element.n_.context.utility2_moduleExports._serverLocalUrlTest)
- description and source-code
```javascript
_serverLocalUrlTest = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports._stateInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_stateInit (options)](#apidoc.element.n_.context.utility2_moduleExports._stateInit)
- description and source-code
```javascript
_stateInit = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will init the state-options
 */
</span>    local.objectSetOverride(local, options, 10);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports._testRunBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>_testRunBefore ()](#apidoc.element.n_.context.utility2_moduleExports._testRunBefore)
- description and source-code
```javascript
_testRunBefore = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.ajax"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajax (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.ajax)
- description and source-code
```javascript
ajax = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will send an ajax-request with error-handling and timeout
 */
</span>    var timerTimeout, tmp, xhr;
    onError = local.onErrorWithStack(onError);
    // init modeServerLocal
    if (!local.env.npm_config_mode_backend && local._serverLocalUrlTest(options.url)) {
        xhr = new local._http.XMLHttpRequest();
    }
    // init xhr
    xhr = xhr || (local.modeJs === 'browser'
        ? new local.global.XMLHttpRequest()
        : new local._http.XMLHttpRequest());
    // debug xhr
    local._debugXhr = xhr;
    // init options
    local.objectSetOverride(xhr, options);
    // init headers
    xhr.headers = {};
    Object.keys(options.headers || {}).forEach(function (key) {
        xhr.headers[key.toLowerCase()] = options.headers[key];
    });
    // init method
    xhr.method = xhr.method || 'GET';
    // init timeout
    xhr.timeout = xhr.timeout || local.timeoutDefault;
    // init timerTimeout
    timerTimeout = local.onTimeout(function (error) {
        xhr.error = xhr.error || error;
        xhr.abort();
        // cleanup requestStream and responseStream
        local.streamListCleanup([xhr.requestStream, xhr.responseStream]);
    }, xhr.timeout, 'ajax ' + xhr.method + ' ' + xhr.url);
    // init event handling
    xhr.onEvent = function (event) {
        // init statusCode
        xhr.statusCode = xhr.status;
        switch (event.type) {
        case 'abort':
        case 'error':
        case 'load':
            // do not run more than once
            if (xhr.done) {
                return;
            }
            xhr.done = true;
            // cleanup timerTimeout
            clearTimeout(timerTimeout);
            // cleanup requestStream and responseStream
            setTimeout(function () {
                local.streamListCleanup([xhr.requestStream, xhr.responseStream]);
            });
            // decrement ajaxProgressCounter
            local.ajaxProgressCounter -= 1;
            // handle abort or error event
            if (!xhr.error &&
                    (event.type === 'abort' ||
                    event.type === 'error' ||
                    xhr.statusCode >= 400)) {
                xhr.error = new Error(event.type);
            }
            // handle completed xhr request
            if (xhr.readyState === 4) {
                // debug xhr
                if (xhr.modeDebug) {
                    console.error(new Date().toISOString(
                    ) + ' ajax-response ' + JSON.stringify({
                        statusCode: xhr.statusCode,
                        method: xhr.method,
                        url: xhr.url,
                        responseText: local.tryCatchOnError(function () {
                            return xhr.responseText.slice(0, 256);
                        }, local.nop)
                    }));
                }
                // handle string data
                if (xhr.error) {
                    // debug statusCode
                    xhr.error.statusCode = xhr.statusCode;
                    // debug statusCode / method / url
                    tmp = local.modeJs + ' - ' + xhr.statusCode + ' ' + xhr.method +
                        ' ' + xhr.url + '\n';
                    // try to debug responseText
                    local.tryCatchOnError(function () {
                        tmp += '    ' + JSON.stringify(xhr.responseText.slice(0, 256) +
                            '...') + '\n';
                    }, local.nop);
                    local.errorMessagePrepend(xhr.error, tmp);
                }
            }
            onError(xhr.error, xhr);
            break;
        }
        local.ajaxProgressUpdate();
    };
    // increment ajaxProgressCounter
    local.ajaxProgressCounter += 1;
    xhr.addEventListener('abort', xhr.onEvent);
    xhr.addEventListener('error', xhr.onEvent);
    xhr.addEventListener('load', xhr.onEvent);
    xhr.addEventListener('loadstart', local.ajaxProgressUpdate);
    xhr.addEventListener('progress', local.ajaxProgressUpdate);
    xhr.upload.addEventListener('progress', local.a ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.ajaxProgressUpdate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>ajaxProgressUpdate ()](#apidoc.element.n_.context.utility2_moduleExports.ajaxProgressUpdate)
- description and source-code
```javascript
ajaxProgressUpdate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will update ajaxProgress
 */
</span>    var ajaxProgressDiv1;
    ajaxProgressDiv1 = local.modeJs === 'browser' &&
        document.querySelector('#ajaxProgressDiv1');
    if (!ajaxProgressDiv1) {
        return;
    }
    // init ajaxProgressDiv1StyleBackground
    local.ajaxProgressDiv1StyleBackground = local.ajaxProgressDiv1StyleBackground ||
        ajaxProgressDiv1.style.background;
    // show ajaxProgress
    if (ajaxProgressDiv1.style.background === 'transparent') {
        ajaxProgressDiv1.style.background = local.ajaxProgressDiv1StyleBackground;
    }
    // cleanup timerTimeout
    clearTimeout(local.timerTimeoutAjaxProgressHide);
    // increment ajaxProgress
    if (local.ajaxProgressCounter > 0) {
        // this algorithm will indefinitely increment the ajaxProgressBar
        // with successively smaller increments without ever reaching 100%
        local.ajaxProgressState += 1;
        ajaxProgressDiv1.style.width =
            100 - 75 * Math.exp(-0.125 * local.ajaxProgressState) + '%';
        return;
    }
    // finish ajaxProgress
    ajaxProgressDiv1.style.width = '100%';
    // hide ajaxProgress
    local.timerTimeoutAjaxProgressHide = setTimeout(function () {
        ajaxProgressDiv1.style.background = 'transparent';
        // reset ajaxProgress
        setTimeout(function () {
            local.ajaxProgressCounter = 0;
            local.ajaxProgressState = 0;
            ajaxProgressDiv1.style.width = '25%';
        }, 500);
    }, 1500);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.apidocCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>apidocCreate (options)](#apidoc.element.n_.context.utility2_moduleExports.apidocCreate)
- description and source-code
```javascript
apidocCreate = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will create the apidoc from options.dir
 */
</span>    var elementCreate, module, moduleMain, readExample, tmp, trimLeft;
    elementCreate = function (module, prefix, key) {
    /*
     * this function will create the apidoc-element in the given module
     */
        var element;
        element = {};
        element.moduleName = prefix.split('.');
        // handle case where module is a function
        if (element.moduleName.slice(-1)[0] === key) {
            element.moduleName.pop();
        }
        element.moduleName = element.moduleName.join('.');
        element.id = encodeURIComponent('apidoc.element.' + prefix + '.' + key);
        element.typeof = typeof module[key];
        element.name = (element.typeof + ' <span class="apidocSignatureSpan">' +
            element.moduleName + '.</span>' + key)
            // handle case where module is a function
            .replace('>.<', '><');
        if (element.typeof !== 'function') {
            return element;
        }
        // init source
        element.source = 'n/a';
        // bug-workaround - catch and ignore error
        // "Function.prototype.toString is not generic"
        try {
            element.source = trimLeft(module[key].toString());
        } catch (ignore) {
        }
        if (element.source.length > 4096) {
            element.source = element.source.slice(0, 4096).trimRight() + ' ...';
        }
        element.source = (options.template === local.templateApidocHtml
            ? local.stringHtmlSafe(element.source)
            : element.source)
            .replace((/\([\S\s]*?\)/), function (match0) {
                // init signature
                element.signature = match0
                    .replace((/ *?\/\*[\S\s]*?\*\/ */g), '')
                    .replace((/,/g), ', ')
                    .replace((/\s+/g), ' ');
                return element.signature;
            })
            .replace(
                (/( *?\/\*[\S\s]*?\*\/\n)/),
                '<span class="apidocCodeCommentSpan">$1</span>'
            )
            .replace((/^function \(/), key + ' = function (');
        // init example
        options.exampleList.some(function (example) {
            example.replace(
                new RegExp('((?:\n.*?){8}\\.)(' + key + ')(\\((?:.*?\n){8})'),
                function (match0, match1, match2, match3) {
                    element.example = '...' + trimLeft(
                        options.template === local.templateApidocHtml
                            ?  local.stringHtmlSafe(match1) +
                                '<span class="apidocCodeKeywordSpan">' +
                                local.stringHtmlSafe(match2) +
                                '</span>' +
                                local.stringHtmlSafe(match3)
                            : match0
                    ).trimRight() + '\n...';
                }
            );
            return element.example;
        });
        element.example = element.example || 'n/a';
        return element;
    };
    readExample = function (file) {
    /*
     * this function will read the example from the given file
     */
        try {
            return ('\n\n\n\n\n\n\n\n' +
                local.fs.readFileSync(local.path.resolve(options.dir, file), 'utf8') +
                '\n\n\n\n\n\n\n\n').replace((/\r\n*/g), '\n');
        } catch (errorCaught) {
            return '';
        }
    };
    trimLeft = function (text) {
    /*
     * this function will normalize the whitespace around the text
     */
        var whitespace;
        whitespace = '';
        text.trim().replace((/^ */gm), function (match0) {
            if (!whitespace || match0.length < whitespace.length) {
                whitespace = match0;
            }
        });
        text = text.replace(new RegExp('^' + whitespace, 'gm'), '');
        // enforce 128 character column limit
        text = text.replace((/^.{128}[^\\\n]+/gm), function (match0) {
            return match0.replace((/(.{128}(?:\b|\w+))/g), '$1\n').trimRight();
        });
        r ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.assert"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assert (passed, message)](#apidoc.element.n_.context.utility2_moduleExports.assert)
- description and source-code
```javascript
assert = function (passed, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will throw the error message if passed is falsey
 */
</span>    var error;
    if (passed) {
        return;
    }
    error = message && message.message
        // if message is an error-object, then leave it as is
        ? message
        : new Error(typeof message === 'string'
            // if message is a string, then leave it as is
            ? message
            // else JSON.stringify message
            : JSON.stringify(message));
    throw error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.assertJsonEqual"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assertJsonEqual (aa, bb)](#apidoc.element.n_.context.utility2_moduleExports.assertJsonEqual)
- description and source-code
```javascript
assertJsonEqual = function (aa, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert
 * utility2.jsonStringifyOrdered(aa) === JSON.stringify(bb)
 */
</span>    aa = local.jsonStringifyOrdered(aa);
    bb = JSON.stringify(bb);
    local.assert(aa === bb, [aa, bb]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.assertJsonNotEqual"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>assertJsonNotEqual (aa, bb)](#apidoc.element.n_.context.utility2_moduleExports.assertJsonNotEqual)
- description and source-code
```javascript
assertJsonNotEqual = function (aa, bb) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert
 * utility2.jsonStringifyOrdered(aa) !== JSON.stringify(bb)
 */
</span>    aa = local.jsonStringifyOrdered(aa);
    bb = JSON.stringify(bb);
    local.assert(aa !== bb, [aa, bb]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64FromBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromBuffer (bff)](#apidoc.element.n_.context.utility2_moduleExports.base64FromBuffer)
- description and source-code
```javascript
base64FromBuffer = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * https://developer.mozilla.org/en-US/Add-ons/Code_snippets/StringView#The_code
 * this function will convert the Uint8Array-bff to base64-encoded-text
 */
</span>    var ii, mod3, text, uint24, uint6ToB64;
    text = '';
    uint24 = 0;
    uint6ToB64 = function (uint6) {
        return uint6 < 26
            ? uint6 + 65
            : uint6 < 52
            ? uint6 + 71
            : uint6 < 62
            ? uint6 - 4
            : uint6 === 62
            ? 43
            : 47;
    };
    for (ii = 0; ii < bff.length; ii += 1) {
        mod3 = ii % 3;
        uint24 |= bff[ii] << (16 >>> mod3 & 24);
        if (mod3 === 2 || bff.length - ii === 1) {
            text += String.fromCharCode(
                uint6ToB64(uint24 >>> 18 & 63),
                uint6ToB64(uint24 >>> 12 & 63),
                uint6ToB64(uint24 >>> 6 & 63),
                uint6ToB64(uint24 & 63)
            );
            uint24 = 0;
        }
    }
    return text.replace(/A(?=A$|$)/g, '=');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64FromHex"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromHex (text)](#apidoc.element.n_.context.utility2_moduleExports.base64FromHex)
- description and source-code
```javascript
base64FromHex = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the hex-text to base64-encoded-text
 */
</span>    var bff, ii;
    bff = [];
    for (ii = 0; ii < text.length; ii += 2) {
        bff.push(parseInt(text[ii] + text[ii + 1], 16));
    }
    return local.base64FromBuffer(bff);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64FromString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64FromString (text)](#apidoc.element.n_.context.utility2_moduleExports.base64FromString)
- description and source-code
```javascript
base64FromString = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the utf8-text to base64-encoded-text
 */
</span>    return local.base64FromBuffer(local.bufferCreate(text));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64ToBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToBuffer (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToBuffer)
- description and source-code
```javascript
base64ToBuffer = function (text) {
<span class="apidocCodeCommentSpan">/*
 * https://gist.github.com/wang-bin/7332335
 * this function will convert the base64-encoded text to Uint8Array
 */
</span>    var de = new Uint8Array(text.length); //3/4
    var u = 0, q = '', x = '', c;
    var map64 = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/";
    for (var r=0; c=text[x++]; ~c&&(u=q%4?u*64+c:c,q++%4)?de[r++]=(255&u>>(-2*q&6)):0)
        c = map64.indexOf(c);
    return de.subarray(0, r);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64ToHex"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToHex (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToHex)
- description and source-code
```javascript
base64ToHex = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the base64-encoded-text to hex-text
 */
</span>    var bff, ii;
    bff = local.base64ToBuffer(text);
    text = '';
    for (ii = 0; ii < bff.length; ii += 1) {
        text += (0x100 + bff[ii]).toString(16).slice(-2);
    }
    return text;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.base64ToString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>base64ToString (text)](#apidoc.element.n_.context.utility2_moduleExports.base64ToString)
- description and source-code
```javascript
base64ToString = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the base64-encoded text to utf8-text
 */
</span>    return local.bufferToString(local.base64ToBuffer(text));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.blobRead"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>blobRead (blob, encoding, onError)](#apidoc.element.n_.context.utility2_moduleExports.blobRead)
- description and source-code
```javascript
blobRead = function (blob, encoding, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will read from the blob with the given encoding
 * possible encodings are:
 * - Uint8Array (default)
 * - dataURL
 * - text
 */
</span>    var data, done, reader;
    if (local.modeJs === 'node') {
        switch (encoding) {
        // readAsDataURL
        case 'dataURL':
            data = 'data:' + (blob.type || '') + ';base64,' +
                local.base64FromBuffer(blob.bff);
            break;
        // readAsText
        case 'text':
            data = local.bufferToString(blob.bff);
            break;
        // readAsArrayBuffer
        default:
            data = local.bufferCreate(blob.bff);
        }
        onError(null, data);
        return;
    }
    reader = new local.global.FileReader();
    reader.onabort = reader.onerror = reader.onload = function (event) {
        if (done) {
            return;
        }
        done = true;
        switch (event.type) {
        case 'abort':
        case 'error':
            onError(new Error('blobRead - ' + event.type));
            break;
        case 'load':
            onError(null, reader.result instanceof local.global.ArrayBuffer
                // convert ArrayBuffer to Uint8Array
                ? local.bufferCreate(reader.result)
                : reader.result);
            break;
        }
    };
    switch (encoding) {
    // readAsDataURL
    case 'dataURL':
        reader.readAsDataURL(blob);
        break;
    // readAsText
    case 'text':
        reader.readAsText(blob);
        break;
    // readAsArrayBuffer
    default:
        reader.readAsArrayBuffer(blob);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.browserTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>browserTest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.browserTest)
- description and source-code
```javascript
browserTest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will spawn an electron process to test options.url
 */
</span>    var done, modeNext, onNext, onParallel, timerTimeout;
    if (typeof local === 'object' && local && local.modeJs === 'node') {
        local.objectSetDefault(options, local.envSanitize(local.env));
        options.timeoutDefault = options.timeoutDefault || local.timeoutDefault;
    }
    modeNext = Number(options.modeNext || 0);
    onNext = function (error, data) {
        modeNext = error instanceof Error
            ? Infinity
            : modeNext + 1;
        switch (modeNext) {
        // run node code
        case 1:
            // init options
            if (!(/^\w+:\/\//).test(options.url)) {
                options.url = local.path.resolve(process.cwd(), options.url);
            }
            options.testName = local.env.MODE_BUILD + '.browser.' +
                encodeURIComponent(local.urlParse(options.url).pathname
                    .replace(
                        '/build..' + local.env.CI_BRANCH + '..' + local.env.CI_HOST,
                        '/build'
                    ));
            local.objectSetDefault(options, {
                fileCoverage: local.env.npm_config_dir_tmp +
                    '/coverage.' + options.testName + '.json',
                fileScreenCapture: (local.env.npm_config_dir_build +
                    '/screenCapture.' + options.testName + '.png')
                    .replace((/%/g), '_')
                    .replace((/_2F\.png$/), '.png'),
                fileTestReport: local.env.npm_config_dir_tmp +
                    '/test-report.' + options.testName + '.json',
                modeBrowserTest: 'test',
                timeExit: Date.now() + options.timeoutDefault,
                timeoutScreenCapture: Number(options.timeoutScreenCapture || 10000)
            }, 1);
            // init timerTimeout
            timerTimeout = local.onTimeout(
                onNext,
                options.timeoutDefault,
                options.testName
            );
            // init file fileElectronHtml
            options.browserTestScript = local.browserTest
                .toString()
                .replace((/<\//g), '<\\/')
                // coverage-hack - un-instrument
                .replace((/\b__cov_.*?\+\+/g), '0');
            options.modeNext = 20;
            options.fileElectronHtml = local.env.npm_config_dir_tmp + '/electron.' +
                Date.now().toString(16) + Math.random().toString(16) + '.html';
            local.fsWriteFileWithMkdirpSync(options.fileElectronHtml, '<style>body {' +
                    'border: 1px solid black;' +
                    'margin: 0;' +
                    'padding: 0;' +
                '}</style>' +
                '<webview id=webview1 preload="' + options.fileElectronHtml +
                '.preload.js" src="' +
                options.url.replace('{{timeExit}}', options.timeExit) +
                '" style="' +
                    'border: none;' +
                    'height: 100%;' +
                    'margin: 0;' +
                    'padding: 0;' +
                    'width: 100%;' +
                '"></webview>' +
                '<script>window.local = {}; (' + options.browserTestScript +
                '(' + JSON.stringify(options) + '))</script>');
            console.error('\nbrowserTest - created electron entry-page ' +
                options.fileElectronHtml + '\n');
            // init file fileElectronHtml.preload.js
            options.modeNext = 30;
            local.fsWriteFileWithMkdirpSync(
                options.fileElectronHtml + '.preload.js',
                '(' + options.browserTestScript + '(' + JSON.stringify(options) +
                    '))'
            );
            // spawn an electron process to test a url
            options.modeNext = 10;
            local.processSpawnWithTimeout('electron', [
                __filename,
                'browserTest',
                '--disable-overlay-scrollbar',
                '--enable-logging'
            ], { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferConcat"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferConcat (bufferList)](#apidoc.element.n_.context.utility2_moduleExports.bufferConcat)
- description and source-code
```javascript
bufferConcat = function (bufferList) {
<span class="apidocCodeCommentSpan">/*
 * this function will emulate node's Buffer.concat for Uint8Array in the browser
 */
</span>    var ii, jj, length, result;
    length = 0;
    bufferList = bufferList
        .filter(function (element) {
            return element || element === 0;
        })
        .map(function (element) {
            // convert number to string
            if (typeof element === 'number') {
                element = String(element);
            }
            // convert non-Uint8Array to Uint8Array
            element = local.bufferCreateIfNotBuffer(element);
            length += element.length;
            return element;
        });
    result = local.bufferCreate(length);
    ii = 0;
    bufferList.forEach(function (element) {
        for (jj = 0; jj < element.length; ii += 1, jj += 1) {
            result[ii] = element[jj];
        }
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferCreate (text)](#apidoc.element.n_.context.utility2_moduleExports.bufferCreate)
- description and source-code
```javascript
bufferCreate = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a Uint8Array from the text,
 * with either 'utf8' (default) or 'base64' encoding
 */
</span>    if (typeof text === 'string') {
        if (local.modeJs === 'node') {
            return new Buffer(text);
        }
        if (local.global.TextEncoder) {
            return new local.global.TextEncoder('utf-8').encode(text);
        }
// bug-workaround - TextEncoder.encode polyfill
/* jslint-ignore-begin */
// utility2-uglifyjs https://github.com/feross/buffer/blob/v4.9.1/index.js#L1670
/* istanbul ignore next */
function utf8ToBytes(e,t){t=t||Infinity;var n,r=e.length,i=null,s=[];for(var o=0
;o<r;++o){n=e.charCodeAt(o);if(n>55295&&n<57344){if(!i){if(n>56319){(t-=3)>-1&&s
.push(239,191,189);continue}if(o+1===r){(t-=3)>-1&&s.push(239,191,189);continue}
i=n;continue}if(n<56320){(t-=3)>-1&&s.push(239,191,189),i=n;continue}n=(i-55296<<10|
n-56320)+65536}else i&&(t-=3)>-1&&s.push(239,191,189);i=null;if(n<128){if((t-=1)<0
)break;s.push(n)}else if(n<2048){if((t-=2)<0)break;s.push(n>>6|192,n&63|128)}else if(
n<65536){if((t-=3)<0)break;s.push(n>>12|224,n>>6&63|128,n&63|128)}else{if(!(n<1114112
))throw new Error("Invalid code point");if((t-=4)<0)break;s.push(n>>18|240,n>>12&63|128
,n>>6&63|128,n&63|128)}}return s}
return new local.global.Uint8Array(utf8ToBytes(text));
/* jslint-ignore-end */
    }
    return new local.global.Uint8Array(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferCreateIfNotBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferCreateIfNotBuffer (text)](#apidoc.element.n_.context.utility2_moduleExports.bufferCreateIfNotBuffer)
- description and source-code
```javascript
bufferCreateIfNotBuffer = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a Uint8Array from the text with the given encoding,
 * if it is not already a Uint8Array
 */
</span>    return text instanceof local.global.Uint8Array
        ? text
        : local.bufferCreate(text);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferIndexOfSubBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferIndexOfSubBuffer (bff, subBff, fromIndex)](#apidoc.element.n_.context.utility2_moduleExports.bufferIndexOfSubBuffer)
- description and source-code
```javascript
bufferIndexOfSubBuffer = function (bff, subBff, fromIndex) {
<span class="apidocCodeCommentSpan">/*
 * this function will search bff for the indexOf-like position of the subBff
 */
</span>    var ii, jj, kk;
    for (ii = fromIndex || 0; ii < bff.length; ii += 1) {
        for (jj = 0, kk = ii; jj < subBff.length; jj += 1, kk += 1) {
            if (subBff[jj] !== bff[kk]) {
                break;
            }
        }
        if (jj === subBff.length) {
            return kk - jj;
        }
    }
    return subBff.length && -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferRandomBytes"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferRandomBytes (length)](#apidoc.element.n_.context.utility2_moduleExports.bufferRandomBytes)
- description and source-code
```javascript
bufferRandomBytes = function (length) {
<span class="apidocCodeCommentSpan">/*
 * this function will create create a Uint8Array with the given length,
 * filled with random bytes
 */
</span>    var bff, ii;
    bff = new local.global.Uint8Array(length);
    for (ii = 0; ii < bff.length; ii += 1) {
        bff[ii] = Math.random() * 0x100;
    }
    return bff;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferToNodeBuffer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferToNodeBuffer (bff)](#apidoc.element.n_.context.utility2_moduleExports.bufferToNodeBuffer)
- description and source-code
```javascript
bufferToNodeBuffer = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the Uint8Array instance to a node Buffer instance
 */
</span>    if (local.modeJs === 'node' &&
            bff instanceof local.global.Uint8Array && (!Buffer.isBuffer(bff))) {
        Object.setPrototypeOf(bff, Buffer.prototype);
    }
    return bff;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.bufferToString"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>bufferToString (bff)](#apidoc.element.n_.context.utility2_moduleExports.bufferToString)
- description and source-code
```javascript
bufferToString = function (bff) {
<span class="apidocCodeCommentSpan">/*
 * this function will convert the Uint8Array bff to a utf8 string
 */
</span>    bff = bff || '';
    if (typeof bff === 'string') {
        return bff;
    }
    bff = local.bufferCreateIfNotBuffer(bff);
    if (local.modeJs === 'node') {
        return new Buffer(bff).toString();
    }
    if (local.global.TextDecoder) {
        return new local.global.TextDecoder('utf-8').decode(bff);
    }
// bug-workaround - TextDecoder.decode polyfill
/* jslint-ignore-begin */
// http://stackoverflow.com/questions/17191945/conversion-between-utf-8-arraybuffer-and-string
function Utf8ArrayToStr(e){var t,n,r,i,s,o;t="",r=e.length,n=0;while(n<r){i=e[n++
];switch(i>>4){case 0:case 1:case 2:case 3:case 4:case 5:case 6:case 7:t+=String
.fromCharCode(i);break;case 12:case 13:s=e[n++],t+=String.fromCharCode((i&31)<<6|
s&63);break;case 14:s=e[n++],o=e[n++],t+=String.fromCharCode((i&15)<<12|(s&63)<<6|
(o&63)<<0)}}return t}
return Utf8ArrayToStr(bff);
/* jslint-ignore-end */
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildApidoc"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildApidoc (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildApidoc)
- description and source-code
```javascript
buildApidoc = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the apidoc
 */
</span>    // optimization - do not run if $npm_config_mode_coverage = all
    if (local.env.npm_config_mode_coverage === 'all') {
        onError();
        return;
    }
    local.objectSetDefault(options, { blacklistDict: local });
    // create apidoc.html
    local.fsWriteFileWithMkdirpSync(
        local.env.npm_config_dir_build + '/apidoc.html',
        local.apidocCreate(options)
    );
    console.error('created apidoc file://' + local.env.npm_config_dir_build +
        '/apidoc.html\n');
    local.browserTest({
        modeBrowserTest: 'screenCapture',
        url: local.env.npm_config_dir_build + '/apidoc.html'
    }, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildApp"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildApp (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildApp)
- description and source-code
```javascript
buildApp = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the app
 */
</span>    var writeFileSync;
    local.fsRmrSync(local.env.npm_config_dir_build + '/app');
    local.onParallelList({ list: options.concat([{
        file: '/assets.' + local.env.npm_package_nameAlias + '.js',
        url: '/assets.' + local.env.npm_package_nameAlias + '.js'
    }, {
        file: '/assets.' + local.env.npm_package_nameAlias + '.rollup.js',
        url: '/assets.' + local.env.npm_package_nameAlias + '.rollup.js'
    }, {
        file: '/assets.app.js',
        url: '/assets.app.js'
    }, {
        file: '/assets.example.js',
        url: '/assets.example.js'
    }, {
        file: '/assets.test.js',
        url: '/assets.test.js'
    }, {
        file: '/assets.utility2.rollup.js',
        url: '/assets.utility2.rollup.js'
    }, {
        file: '/index.html',
        url: '/index.html'
    }, {
        file: '/jsonp.utility2._stateInit',
        url: '/jsonp.utility2._stateInit?callback=window.utility2._stateInit'
    }]) }, function (options, onParallel) {
        options = options.element;
        onParallel.counter += 1;
        local.ajax(options, function (error, xhr) {
            // validate no error occurred
            local.assert(!error, error);
            // jslint file
            local.jslintAndPrintConditional(xhr.responseText, options.file);
            // validate no error occurred
            local.assert(!local.jslint.errorText, local.jslint.errorText);
            local.fsWriteFileWithMkdirpSync(
                local.env.npm_config_dir_build + '/app' + options.file,
                new Buffer(xhr.response)
            );
            onParallel();
        });
    }, function (error) {
        // validate no error occurred
        local.assert(!error, error);
        // coverage-hack
        writeFileSync = local.fs.writeFileSync;
        local.nop(local.global.__coverage__ && (function () {
            writeFileSync = local.nop;
        }()));
        writeFileSync(
            'assets.' + local.env.npm_package_nameAlias + '.rollup.js',
            local.assetsDict['/assets.' + local.env.npm_package_nameAlias +
                '.rollup.js']
        );
        // test standalone assets.app.js
        local.fs.writeFileSync('tmp/assets.app.js', local.assetsDict['/assets.app.js']);
        local.processSpawnWithTimeout(process.argv[0], ['assets.app.js'], {
            cwd: 'tmp',
            env: {
                PORT: (Math.random() * 0x10000) | 0x8000,
                npm_config_timeout_exit: 5000
            },
            stdio: ['ignore', 1, 2]
        })
            .once('error', onError)
            .once('exit', function (exitCode) {
                // validate exitCode
                local.assert(!exitCode, exitCode);
                onError();
            });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildLib"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildLib (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildLib)
- description and source-code
```javascript
buildLib = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the lib
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile(
            'lib.' + local.env.npm_package_nameAlias + '.js',
            'utf8'
        ),
        dataTo: local.templateRenderJslintLite(
            local.assetsDict['/assets.lib.template.js'],
            {}
        )
    });
    // search-and-replace - customize dataTo
    [
        // customize body before istanbul
        (/[\S\s]*?^\/\* istanbul instrument in package /m),
        // customize body after init exports
        (/\n {12}module.exports.module = module;\n[\S\s]*?$/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    options.customize();
    // save lib.xxx.js
    local.fs.writeFileSync(
        'lib.' + local.env.npm_package_nameAlias + '.js',
        options.dataTo
    );
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildNpmdoc"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildNpmdoc (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildNpmdoc)
- description and source-code
```javascript
buildNpmdoc = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the npmdoc
 */
</span>    var done, onError2, onParallel, packageJson;
    // ensure exit after 5 minutes
    setTimeout(process.exit, 5 * 60 * 1000);
    onError2 = function (error) {
        local.onErrorDefault(error);
        if (done) {
            return;
        }
        done = true;
        // try to recover from error
        setTimeout(onError, error && local.timeoutDefault);
    };
    // try to salvage uncaughtException
    process.on('uncaughtException', onError2);
    onParallel = local.utility2.onParallel(onError2);
    onParallel.counter += 1;
    // build package.json
    packageJson = JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    local.objectSetDefault(packageJson, local.objectLiteralize({
        devDependencies: {
            '$[]': [local.env.npm_package_buildNpmdoc, '*']
        },
        repository: {
            type: 'git',
            url: 'https://github.com/npmdoc/node-npmdoc-' +
                local.env.npm_package_buildNpmdoc + '.git'
        }
    }), 2);
    local.objectSetOverride(packageJson, local.objectLiteralize({
        keywords: ['documentation', local.env.npm_package_buildNpmdoc]
    }), 2);
    onParallel.counter += 1;
    local.buildReadme({
        dataFrom: '\n# package.json\n'''json\n' +
            JSON.stringify(packageJson) + '\n'''\n'
    }, onParallel);
    packageJson = JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    // build apidoc.html
    onParallel.counter += 1;
    local.buildApidoc({
        dir: local.env.npm_package_buildNpmdoc,
        modulePathList: options.modulePathList
    }, onParallel);
    // build README.md
    options = { modulePathList: options.modulePathList };
    options.readme = local.apidocCreate({
        dir: local.env.npm_package_buildNpmdoc,
/* jslint-ignore-begin */
header: '\
# api documentation for \
 \
n_ (v1.4.4) \
 \
[![npm package](https://img.shields.io/npm/v/npmdoc-n_.svg?style=flat-square)](https://www.npmjs.org/package
/npmdoc-n_)\
[![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-n_.svg)](https://travis-ci.org
/npmdoc/node-npmdoc-n_)\
\n\
#### lodash REPL \
\n\
\n\
[![NPM](https://nodei.co/npm/n_.png?downloads=true)](https://www.npmjs.com/package/n_)\
\n\
\n\
[![apidoc](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode
-npmdoc-n__2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-n_/
build/apidoc.html)\
\n\
\n\
![npmPackageListing](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageListing.svg) \
\n\
\n\
![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-n_/build/screenCapture.npmPackageDependencyTree
.svg)\
\n\
\n\
\n\
\n\
# package.json \
\n\
\n\
'''json \
\n\
\n\
{
    "author": {
        "name": "Boris Diakur",
        "email": "contact@borisdiakur.com",
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
            "email": "contact@borisdiakur.com",
            "url": "https://github.com/borisdiakur"
        },
        {
            "name": "John-David Dalton",
            "email": "john.david.dalton@gmail.com",
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
            "name": "borisdiakur",
            "email": "contact@borisdiakur.com"
        },
        {
            "name": "jdalton",
            "email": "john.david.dalton@gmail.com"
        }
    ],
    "name": "n_",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
} \
\n\
''' \
\n\
',
/* jslint-ignore-end */
        modulePathList: options.modulePathList,
        template: local.apidoc.templateApidocMd
    });
    local.fs.writeFileSync('README.md', options.readme);
    // re-build package.json
    packageJson.description = (/\w.*/).exec(options.readme)[0]
        .replace((/ {2,}/g), ' ')
        .trim();
    local.fs.writeFileSync(
        'package.json',
        local.jsonStringifyOrdered(packageJson, null, 4) + '\n'
    );
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildReadme"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildReadme (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildReadme)
- description and source-code
```javascript
buildReadme = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the readme in jslint-lite style
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile('README.md', 'utf8')
    });
    // init package.json
    options.rgx = (/\n# package.json\n'''json\n([\S\s]*?)\n'''\n/);
    options.dataFrom.replace(options.rgx, function (match0, match1) {
        options.packageJson = JSON.parse(match1);
        options.packageJson.description = options.dataFrom.split('\n')[1];
        local.objectSetDefault(options.packageJson, {
            nameAlias: options.packageJson.name.replace((/\W/g), '_'),
            nameOriginal: options.packageJson.name
        });
        local.objectSetDefault(
            options.packageJson,
            JSON.parse(local.templateRenderJslintLite(
                options.rgx.exec(local.assetsDict['/assets.readme.template.md'])[1],
                options
            )),
            2
        );
        // avoid npm-installing self
        delete options.packageJson.devDependencies[options.packageJson.name];
        // save package.json
        local.fs.writeFileSync(
            'package.json',
            local.jsonStringifyOrdered(options.packageJson, null, 4) + '\n'
        );
        // update dataTo
        options.dataTo = local.templateRenderJslintLite(
            local.assetsDict['/assets.readme.template.md'],
            options
        );
        options.dataTo = options.dataTo.replace(
            options.rgx,
            match0.replace(
                match1,
                local.jsonStringifyOrdered(options.packageJson, null, 4)
            )
        );
    });
    // search-and-replace - customize dataTo
    [
        // customize header
        (/.*?\n.*?\n/),
        // customize todo
        (/\n#### todo\n[\S\s]*?\n\n\n\n/),
        // customize quickstart-header
        (/\n'''javascript\n\/\*\nexample\.js\n\n[^']*?\n/),
        (/\n {8}\$ npm install [^']*? &&/),
        (/\n {12}: global;\n[^']*?\n {8}local\.global\.local = local;\n/),
        (/\n {8}local\.global\.local = local;\n[^']*?\n {4}\/\/ post-init\n/),
        new RegExp('\\n {8}local\\.testRunBrowser = function \\(event\\) \\{\\n' +
            '[^']*?^ {12}if \\(!event \\|\\| \\(event &&\\n', 'm'),
        (/\n {12}\/\/ custom-case\n[^']*?\n {12}\}\n/),
        // customize quickstart-html-style
        (/\n<\/style>\\n\\\n<style>\\n\\\n[^']*?\\n\\\n<\/style>\\n\\\n/),
        // customize quickstart-html-body
        (/\nutility2-comment -->(?:\\n\\\n){4}[^']*?^<!-- utility2-comment\\n\\\n/m),
        // customize build-script
        (/\n# internal build-script\n[\S\s]*?^- build_ci\.sh\n/m),
        (/\nshBuildCiPost\(\) \{\(set -e\n[^']*?\n\)\}\n/),
        (/\nshBuildCiPre\(\) \{\(set -e\n[^']*?\n\)\}\n/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    // customize comment
    options.dataFrom.replace(
        (/^( *?)(?:#!! |#\/\/ |\/\/!!)(.*?)$/gm),
        function (match0, match1, match2) {
            options.dataTo = options.dataTo.replace(match1 + match2, match0);
        }
    );
    options.customize();
    // save README.md
    local.fs.writeFileSync('README.md', options.dataTo);
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.buildTest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>buildTest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.buildTest)
- description and source-code
```javascript
buildTest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will build the test
 */
</span>    local.objectSetDefault(options, {
        customize: local.nop,
        dataFrom: local.tryCatchReadFile('test.js', 'utf8'),
        dataTo: local.templateRenderJslintLite(
            local.assetsDict['/assets.test.template.js'],
            {}
        )
    });
    // search-and-replace - customize dataTo
    [
        // customize js\-env code
        new RegExp('\\n {4}\\/\\/ run shared js\\-env code - pre-init\\n[\\S\\s]*?' +
            '^ {4}\\(function \\(\\) \\{\\n', 'm'),
        (/\n {8}local.global.local = local;\n[\S\s]*?^ {4}\}\(\)\);\n/m),
        (/\n {4}\/\/ run shared js\-env code - function\n[\S\s]*?\n {4}\}\(\)\);\n/),
        (/\n {4}\/\/ run browser js\-env code - function\n[\S\s]*?\n {8}break;\n/),
        (/\n {4}\/\/ run node js\-env code - function\n[\S\s]*?\n {8}break;\n/),
        new RegExp('\\n {4}\\/\\/ run browser js\\-env code - post-init\\n[\\S\\s]*?' +
            '^ {4}case \'browser\':\n', 'm'),
        (/\n {4}\/\/ run shared js\-env code - post-init\n[\S\s]*?\n {4}\}\(\)\);\n/)
    ].forEach(function (rgx) {
        // handle large string-replace
        options.dataFrom.replace(rgx, function (match0) {
            options.dataTo.replace(rgx, function (match1) {
                options.dataTo = options.dataTo.split(match1);
                options.dataTo[0] += match0;
                options.dataTo[0] += options.dataTo.splice(1, 1)[0];
                options.dataTo = options.dataTo.join(match1);
            });
        });
    });
    options.customize();
    // save test.js
    local.fs.writeFileSync('test.js', options.dataTo);
    onError();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.cookieDict"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieDict ()](#apidoc.element.n_.context.utility2_moduleExports.cookieDict)
- description and source-code
```javascript
cookieDict = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will return a dict of all cookies
 */
</span>    var result;
    result = {};
    document.cookie.replace((/(\w+)=([^;]*)/g), function (match0, match1, match2) {
        // jslint-hack
        local.nop(match0);
        result[match1] = match2;
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.cookieRemove"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieRemove (name)](#apidoc.element.n_.context.utility2_moduleExports.cookieRemove)
- description and source-code
```javascript
cookieRemove = function (name) {
<span class="apidocCodeCommentSpan">/*
 * this function will remove the cookie with the given name
 */
</span>    document.cookie = name + '=; expires=Thu, 01 Jan 1970 00:00:00 GMT';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.cookieRemoveAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieRemoveAll ()](#apidoc.element.n_.context.utility2_moduleExports.cookieRemoveAll)
- description and source-code
```javascript
cookieRemoveAll = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will remove all cookies
 */
</span>    document.cookie.replace((/(\w+)=/g), function (match0, match1) {
        // jslint-hack
        local.nop(match0);
        document.cookie = match1 + '=; expires=Thu, 01 Jan 1970 00:00:00 GMT';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.cookieSet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>cookieSet (name, value, expiresOffset)](#apidoc.element.n_.context.utility2_moduleExports.cookieSet)
- description and source-code
```javascript
cookieSet = function (name, value, expiresOffset) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the cookie with the given name, value,
 * and expiresOffset (in ms)
 */
</span>    var tmp;
    tmp = name + '=' + value + '; expires=' +
        new Date(Date.now() + expiresOffset).toUTCString();
    document.cookie = tmp;
    return tmp;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoCreate (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCreate)
- description and source-code
```javascript
dbTableTravisRepoCreate = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a persistent dbTableTravisRepo
 */
</span>    options = local.objectSetDefault(options, {
        idIndexCreateList: [{ name: 'githubRepo' }],
        sortDefault: [{
            fieldName: 'githubRepo'
        }, {
            fieldName: 'last_build_started_at'
        }],
        name: 'TravisRepo'
    });
    local.dbTableTravisRepo = local.db.dbTableCreateOne(options, onError);
    return local.dbTableTravisRepo;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCrudGetManyByQuery"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoCrudGetManyByQuery (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoCrudGetManyByQuery)
- description and source-code
```javascript
dbTableTravisRepoCrudGetManyByQuery = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will query dbTableTravisRepo
 */
</span>    options = local.objectSetDefault(options, {
        fieldList: ['githubRepo', 'last_build_started_at', 'last_build_status'],
        sort: [{ fieldName: 'last_build_started_at' }]
    });
    return local.dbTableTravisRepoCreate().crudGetManyByQuery(options, onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoUpdate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>dbTableTravisRepoUpdate (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.dbTableTravisRepoUpdate)
- description and source-code
```javascript
dbTableTravisRepoUpdate = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will update dbTableTravisRepo with active, public repos
 */
</span>    var dbRowList, self;
    options = local.objectSetDefault(options, { queryLimit: 500, rateLimit: 10 });
    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        case 1:
            local.timeElapsedStart(options);
            self = local.dbTableTravisRepo =
                local.dbTableTravisRepoCreate(options, options.onNext);
            break;
        case 2:
            self = local.dbTableTravisRepo = data;
            console.error('dbTableTravisRepoUpdate - updating ' +
                Math.min(options.queryLimit, self.crudCountAll()) +
                ' of ' + self.crudCountAll() + ' dbRows ...');
            local.ajax({
                headers: { Authorization: 'token ' + local.env.TRAVIS_ACCESS_TOKEN },
                url: 'https://api.travis-ci.org/hooks'
            }, options.onNext);
            break;
        case 3:
            // validate no error occurred
            local.assert(!error, error);
            data = JSON.parse(data.responseText)
                .filter(function (dbRow) {
                    return dbRow.active === true && dbRow.private === false;
                })
                .map(function (dbRow) {
                    dbRow.githubRepo = dbRow.uid.replace(':', '/');
                    dbRow.uid = null;
                    dbRow.url = null;
                    return dbRow;
                });
            self.crudUpdateManyById(data);
            dbRowList = local.dbTableTravisRepoCrudGetManyByQuery({
                limit: options.queryLimit
            });
            local.onParallelList({
                list: dbRowList,
                rateLimit: options.rateLimit
            }, function (dbRow, onParallel) {
                dbRow = dbRow.element;
                onParallel.counter += 1;
                local.ajax({
                    headers: {
                        Authorization: 'token ' + local.env.TRAVIS_ACCESS_TOKEN
                    },
                    url: 'https://api.travis-ci.org/repos/' + dbRow.githubRepo
                }, function (error, data) {
                    // validate no error occurred
                    local.assert(!error, error);
                    data = JSON.parse(data.responseText);
                    Object.keys(data).forEach(function (key) {
                        if (data[key] !== null) {
                            dbRow[key] = data[key];
                        }
                    });
                    // ignore extraneous data to save space
                    dbRow.description = null;
                    dbRow.last_build_duration = null;
                    dbRow.last_build_finished_at = null;
                    dbRow.last_build_id = null;
                    dbRow.last_build_number = null;
                    dbRow.last_build_result = null;
                    dbRow.public_key = null;
                    dbRow.slug = null;
                    dbRow.uid = null;
                    dbRow.url = null;
                    if (onParallel.counter === 1 || ((onParallel.ii + 1) % 10 === 0 &&
                            local.timeElapsedPoll(options).timeElapsed >= 5000)) {
                        local.timeElapsedStart(options, Date.now());
                        console.error('dbTableTravisRepoUpdate - updated ' +
                            (onParallel.ii + 1) + ' dbRows');
                    }
                    onParallel();
                });
            }, options.onNext);
            break;
        case 4:
            self.crudSetManyById(dbRowList);
            self.save(options.onNext);
            break;
        default:
            local.setTimeoutOnError(onError, error, self);
        }
    });
    options.modeNext = 0;
    options.onNext();
    return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.domFragmentRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>domFragmentRender (template, dict)](#apidoc.element.n_.context.utility2_moduleExports.domFragmentRender)
- description and source-code
```javascript
domFragmentRender = function (template, dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a dom-fragment rendered from the givent template and dict
 */
</span>    var tmp;
    tmp = document.createElement('template');
    tmp.innerHTML = local.templateRender(template, dict);
    return tmp.content;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.echo"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>echo (arg)](#apidoc.element.n_.context.utility2_moduleExports.echo)
- description and source-code
```javascript
echo = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return the arg
 */
</span>    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.envKeyIsSensitive"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>envKeyIsSensitive (key)](#apidoc.element.n_.context.utility2_moduleExports.envKeyIsSensitive)
- description and source-code
```javascript
envKeyIsSensitive = function (key) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to determine if the env-key is sensitive
 */
</span>    return (/(?:\b|_)(?:decrypt|key|pass|private|secret|token)/)
        .test(key.toLowerCase()) ||
        (/Decrypt|Key|Pass|Private|Secret|Token/).test(key);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.envSanitize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>envSanitize (env)](#apidoc.element.n_.context.utility2_moduleExports.envSanitize)
- description and source-code
```javascript
envSanitize = function (env) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a sanitized copy of the env object,
 * with sensitive env-vars removed
 */
</span>    var result;
    result = {};
    Object.keys(env).forEach(function (key) {
        if (!local.envKeyIsSensitive(key) &&
                typeof env[key] === 'string' &&
                env[key].length <= 4096) {
            result[key] = env[key];
        }
    });
    return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.errorMessagePrepend"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>errorMessagePrepend (error, message)](#apidoc.element.n_.context.utility2_moduleExports.errorMessagePrepend)
- description and source-code
```javascript
errorMessagePrepend = function (error, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will prepend the message to error.message and error.stack
 */
</span>    error.message = message + error.message;
    error.stack = message + error.stack;
    return error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.exit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>exit (exitCode)](#apidoc.element.n_.context.utility2_moduleExports.exit)
- description and source-code
```javascript
exit = function (exitCode) {
<span class="apidocCodeCommentSpan">/*
 * this function will exit the current process with the given exitCode
 */
</span>    exitCode = !exitCode || Number(exitCode) === 0
        ? 0
        : Number(exitCode) || 1;
    switch (local.modeJs) {
    case 'browser':
        console.error(local.global.fileElectronHtml + ' global_test_results ' +
            JSON.stringify({ global_test_results: local.global.global_test_results }));
        break;
    case 'node':
        process.exit(exitCode);
        break;
    }
    // reset modeTest
    local.modeTest = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.fsRmrSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>fsRmrSync (dir)](#apidoc.element.n_.context.utility2_moduleExports.fsRmrSync)
- description and source-code
```javascript
fsRmrSync = function (dir) {
<span class="apidocCodeCommentSpan">/*
 * this function will synchronously 'rm -fr' the dir
 */
</span>    local.child_process.spawnSync(
        'rm',
        ['-fr', local.path.resolve(process.cwd(), dir)],
        { stdio: ['ignore', 1, 2] }
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.fsWriteFileWithMkdirpSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>fsWriteFileWithMkdirpSync (file, data)](#apidoc.element.n_.context.utility2_moduleExports.fsWriteFileWithMkdirpSync)
- description and source-code
```javascript
fsWriteFileWithMkdirpSync = function (file, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will synchronously 'mkdir -p' and write the data to file
 */
</span>    // try to write to file
    try {
        require('fs').writeFileSync(file, data);
    } catch (errorCaught) {
        // mkdir -p
        require('child_process').spawnSync(
            'mkdir',
            ['-p', require('path').dirname(file)],
            { stdio: ['ignore', 1, 2] }
        );
        // re-write to file
        require('fs').writeFileSync(file, data);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.httpRequest"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>httpRequest (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.httpRequest)
- description and source-code
```javascript
httpRequest = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will request the data from options.url
 */
</span>    var chunkList, onError2, timerTimeout, done, request, response, urlParsed;
    // init onError2
    onError2 = function (error) {
        if (done) {
            return;
        }
        done = true;
        // cleanup timerTimeout
        clearTimeout(timerTimeout);
        // cleanup request and response
        [request, response].forEach(function (stream) {
            // try to end the stream
            try {
                stream.end();
            // else try to destroy the stream
            } catch (errorCaught) {
                try {
                    stream.destroy();
                } catch (ignore) {
                }
            }
        });
        // debug response
        console.error(new Date().toISOString() + ' http-response ' + JSON.stringify({
            method: options.method,
            url: options.url,
            statusCode: (response && response.statusCode) || 0
        }));
        onError(error, response);
    };
    // init timerTimeout
    timerTimeout = setTimeout(function () {
        onError2(new Error('http-request timeout'));
    }, options.timeout || 30000);
    urlParsed = require('url').parse(options.url);
    urlParsed.headers = options.headers;
    urlParsed.method = options.method;
    // debug request
    console.error();
    console.error(new Date().toISOString() + ' http-request ' + JSON.stringify({
        method: options.method,
        url: options.url
    }));
    request = require(
        urlParsed.protocol.slice(0, -1)
    ).request(urlParsed, function (_response) {
        response = _response;
        if (response.statusCode < 200 || response.statusCode > 299) {
            onError2(new Error(response.statusCode));
            return;
        }
        chunkList = [];
        response
            .on('data', function (chunk) {
                chunkList.push(chunk);
            })
            .on('end', function () {
                response.data = Buffer.concat(chunkList);
                onError2();
            })
            .on('error', onError2);
    }).on('error', onError2);
    request.end(options.data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.isNullOrUndefined"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>isNullOrUndefined (arg)](#apidoc.element.n_.context.utility2_moduleExports.isNullOrUndefined)
- description and source-code
```javascript
isNullOrUndefined = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will test if the arg is null or undefined
 */
</span>    return arg === null || arg === undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageMerge"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulCoverageMerge (coverage1, coverage2)](#apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageMerge)
- description and source-code
```javascript
istanbulCoverageMerge = function (coverage1, coverage2) {
<span class="apidocCodeCommentSpan">/*
 * this function will merge coverage2 into coverage1
 */
</span>    var dict1, dict2;
    coverage1 = coverage1 || {};
    coverage2 = coverage2 || {};
    Object.keys(coverage2).forEach(function (file) {
        if (!coverage2[file]) {
            return;
        }
        // if file is undefined in coverage1, then add it
        if (!coverage1[file]) {
            coverage1[file] = coverage2[file];
            return;
        }
        // merge file from coverage2 into coverage1
        ['b', 'f', 's'].forEach(function (key) {
            dict1 = coverage1[file][key];
            dict2 = coverage2[file][key];
            switch (key) {
            // increment coverage for branch lines
            case 'b':
                Object.keys(dict2).forEach(function (key) {
                    dict2[key].forEach(function (count, ii) {
                        dict1[key][ii] += count;
                    });
                });
                break;
            // increment coverage for function and statement lines
            case 'f':
            case 's':
                Object.keys(dict2).forEach(function (key) {
                    dict1[key] += dict2[key];
                });
                break;
            }
        });
    });
    return coverage1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageReportCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulCoverageReportCreate ()](#apidoc.element.n_.context.utility2_moduleExports.istanbulCoverageReportCreate)
- description and source-code
```javascript
istanbulCoverageReportCreate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. print coverage in text-format to stdout
 * 2. write coverage in html-format to filesystem
 * 3. return coverage in html-format as single document
 */
</span>    var options;
    /* istanbul ignore next */
    if (!local.global.__coverage__) {
        return '';
    }
    options = {};
    options.dir = process.cwd() + '/tmp/build/coverage.html';
    // merge previous coverage
    if (local.modeJs === 'node' && process.env.npm_config_mode_coverage_merge) {
        console.log('merging file://' + options.dir + '/coverage.json to coverage');
        try {
            local.coverageMerge(
                local.global.__coverage__,
                JSON.parse(
                    local._fs.readFileSync(options.dir + '/coverage.json', 'utf8')
                )
            );
        } catch (ignore) {
        }
        try {
            options.coverageCodeDict = JSON.parse(local._fs.readFileSync(
                options.dir + '/coverage.code-dict.json',
                'utf8'
            ));
            Object.keys(options.coverageCodeDict).forEach(function (key) {
                local.global.__coverageCodeDict__[key] =
                    local.global.__coverageCodeDict__[key] ||
                    options.coverageCodeDict[key];
            });
        } catch (ignore) {
        }
    }
    // init writer
    local.coverageReportHtml = '';
    local.coverageReportHtml += '<div class="coverageReportDiv">\n' +
        '<h1>coverage-report</h1>\n' +
        '<div ' +
        'style="background: #fff; border: 1px solid #000; margin 0; padding: 0;">\n';
    local.writerData = '';
    options.sourceStore = {};
    options.writer = local.writer;
    // 1. print coverage in text-format to stdout
    new local.TextReport(options).writeReport(local.collector);
    // 2. write coverage in html-format to filesystem
    new local.HtmlReport(options).writeReport(local.collector);
    local.writer.writeFile('', local.nop);
    // write coverage.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.json',
        JSON.stringify(local.global.__coverage__)
    );
    // write coverage.code-dict.json
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.code-dict.json',
        JSON.stringify(local.global.__coverageCodeDict__)
    );
    // write coverage.badge.svg
    options.pct = local.coverageReportSummary.root.metrics.lines.pct;
    local.fsWriteFileWithMkdirpSync2(
        local.path.dirname(options.dir) + '/coverage.badge.svg',
        local.templateCoverageBadgeSvg
            // edit coverage badge percent
            .replace((/100.0/g), options.pct)
            // edit coverage badge color
            .replace(
                (/0d0/g),
                ('0' + Math.round((100 - options.pct) * 2.21).toString(16)).slice(-2) +
                    ('0' + Math.round(options.pct * 2.21).toString(16)).slice(-2) + '00'
            )
    );
    console.log('created coverage file://' + options.dir + '/index.html');
    // 3. return coverage in html-format as a single document
    local.coverageReportHtml += '</div>\n</div>\n';
    // write coverage.rollup.html
    local.fsWriteFileWithMkdirpSync2(
        options.dir + '/coverage.rollup.html',
        local.coverageReportHtml
    );
    return local.coverageReportHtml;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentInPackage"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulInstrumentInPackage (code, file)](#apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentInPackage)
- description and source-code
```javascript
istanbulInstrumentInPackage = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will instrument the code
 * only if the macro /\* istanbul instrument in package $npm_package_nameAlias *\/
 * exists in the code
 */
</span>    return process.env.npm_config_mode_coverage &&
        code.indexOf('/* istanbul ignore all */\n') < 0 && (
            process.env.npm_config_mode_coverage === 'all' ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_package_nameAlias + ' */\n') >= 0 ||
            code.indexOf('/* istanbul instrument in package ' +
                    process.env.npm_config_mode_coverage + ' */\n') >= 0
        )
        ? local.instrumentSync(code, file)
        : code;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>istanbulInstrumentSync (code, file)](#apidoc.element.n_.context.utility2_moduleExports.istanbulInstrumentSync)
- description and source-code
```javascript
istanbulInstrumentSync = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. normalize the file
 * 2. save code to __coverageCodeDict__[file] for future html-report
 * 3. return instrumented code
 */
</span>    // 1. normalize the file
    file = local.path.resolve('/', file);
    // 2. save code to __coverageCodeDict__[file] for future html-report
    local.global.__coverageCodeDict__[file] = code;
    // 3. return instrumented code
    return new local.Instrumenter({
        embedSource: true,
        noAutoWrap: true
    }).instrumentSync(code, file).trimLeft();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jslintAndPrint"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jslintAndPrint (script, file)](#apidoc.element.n_.context.utility2_moduleExports.jslintAndPrint)
- description and source-code
```javascript
jslintAndPrint = function (script, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will jslint / csslint the script and print any errors to stderr
 */
</span>    var ignoreDict, lineno, scriptParsed;
    // cleanup errors
    local.errorCounter = 0;
    local.errorText = '';
    // do nothing for empty script
    if (!script.length) {
        return script;
    }
    // init ignoreDict
    ignoreDict = {};
    // init lineno
    lineno = 0;
    // parse script
    scriptParsed = script
        // indent text-block
        // /* jslint-indent-begin */ ... /* jslint-indent-end */
        .replace(
/* jslint-indent-begin 20 */
(function () {
    /*jslint maxlen: 256*/
    return (/^ *?\/\* jslint-indent-begin (\d+?) \*\/$[\S\s]+?^ *?\/\* jslint-indent-end \*\/$/gm);
}()),
/* jslint-indent-end */
            function (match0, match1) {
                return match0.replace(
                    (/(^ *\S)/gm),
                    new Array(Number(match1) + 1).join(' ') + '$1'
                );
            }
        )
        // ignore text-block
        // /* jslint-ignore-begin */ ... /* jslint-ignore-end */
        .replace(
/* jslint-ignore-begin */
(/^ *?\/\* jslint-ignore-begin \*\/$[\S\s]+?^ *?\/\* jslint-ignore-end \*\/$/gm),
/* jslint-ignore-end */
            function (match0) {
                return match0.replace((/.*/g), '');
            }
        )
        // ignore next-line
        // /* jslint-ignore-next-line */
        .replace(
/* jslint-ignore-next-line */
(/^ *?\/\* jslint-ignore-next-line \*\/\n.*/gm),
            function (match0) {
                return match0.replace((/.*/g), '');
            }
        );
    // csslint script
    if (file.slice(-4) === '.css') {
        scriptParsed = scriptParsed.replace(new RegExp([
            // handle flexbox
            ' display: flex;',
            ' flex: .+?;',
            ' flex-.+?: .+?;'
        ].join('|'), 'g'), function () {
            return ' background: url(' + Math.random() + ');';
        });
        local.CSSLint.errors = local.CSSLint.verify(scriptParsed).messages
            .filter(function (error) {
                return !ignoreDict[error.rule.id];
            });
        // if error occurred, then print colorized error messages
        if (!local.CSSLint.errors.length) {
            return script;
        }
        local.errorText = '\n\u001b[1m' + file + '\u001b[22m\n';
        local.CSSLint.errors
            .filter(function (error) {
                return error;
            })
            .forEach(function (error) {
                local.errorCounter += 1;
                lineno += 1;
                local.errorText +=
                    (' #' + String(lineno) + ' ').slice(-4) +
                    '\u001b[33m' + error.type + ' - ' + error.rule.id +
                    ' - ' + error.message + '\n    ' + error.rule.desc +
                    '\u001b[39m\n    ' + String(error.evidence).trim() +
                    '\u001b[90m \/\/ line ' + error.line +
                    ', col ' + error.col + '\u001b[39m\n';
            });
    // jslint es6-script
    } else if ((/^\/\*jslint\b[\s\w,:]*?\bes6: true\b/m)
            .test(scriptParsed.slice(0, 0x1000))) {
        // comment shebang
        scriptParsed = scriptParsed.replace((/^#!/), '//');
        local.jslintEs6.errors = local.jslintEs6(scriptParsed).warnings;
        if (!local.jslintEs6.errors.length) {
            return script;
        }
        // if error occurred, then print colorized error messages
        local.errorText = '\n\u001b[1m' + file + '\u001b[22m\n';
        local.jslintEs6.errors
            .filter(function (error) {
                return error;
            })
            .forEach(function (error) {
                local.errorCounter += 1;
                lineno += 1;
                local.errorText +=
                    (' #' + String(lineno) + ' ').slice(-4) +
                    '\u001b[33m' + error.message +
                    '\u001b[39m\n    ' + String(error.a).trim() +
                    '\u001b[90m \/\/ Line ' + (error.line + 1) +
                    ', Pos ' + (error.column + 1) + '\u001 ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jslintAndPrintConditional"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jslintAndPrintConditional (script, file, mode)](#apidoc.element.n_.context.utility2_moduleExports.jslintAndPrintConditional)
- description and source-code
```javascript
jslintAndPrintConditional = function (script, file, mode) {
<span class="apidocCodeCommentSpan">/*
 * this function will jslint / csslint the script and print any errors to stderr,
 * conditionally
 */
</span>    var extname;
    // cleanup errors
    local.jslint.errorCounter = 0;
    local.jslint.errorText = '';
    // optimization - ignore uglified/rollup files
    if ((/\bmin\b|\brollup\b/).test(file)) {
        return script;
    }
    extname = (/\.\w+$/).exec(file);
    extname = extname && extname[0];
    switch (extname) {
    case '.css':
        if (script.indexOf('/*csslint') >= 0 || mode === 'force') {
            local.jslintAndPrint(script, file);
        }
        break;
    case '.html':
        // csslint <style> tag
        script.replace(
            (/<style>([\S\s]+?)<\/style>/g),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                match1 = text.slice(0, ii).replace((/.+/g), '') + match1;
                local.jslintAndPrintConditional(match1, file + '.css', mode);
            }
        );
        // jslint <script> tag
        script.replace(
            (/<script>([\S\s]+?)<\/script>/g),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                match1 = text.slice(0, ii).replace((/.+/g), '') + match1;
                local.jslintAndPrintConditional(match1, file + '.js', mode);
            }
        );
        break;
    case '.js':
        if ((script.indexOf('/*jslint') >= 0 &&
                !local.global.__coverage__) || mode === 'force') {
            local.jslintAndPrint(script, file);
        }
        break;
    }
    return script;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jsonCopy"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jsonCopy (arg)](#apidoc.element.n_.context.utility2_moduleExports.jsonCopy)
- description and source-code
```javascript
jsonCopy = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a deep-copy of the JSON-arg
 */
</span>    return arg === undefined
        ? undefined
        : JSON.parse(JSON.stringify(arg));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jsonStringifyOrdered"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jsonStringifyOrdered (element, replacer, space)](#apidoc.element.n_.context.utility2_moduleExports.jsonStringifyOrdered)
- description and source-code
```javascript
jsonStringifyOrdered = function (element, replacer, space) {
<span class="apidocCodeCommentSpan">/*
 * this function will JSON.stringify the element,
 * with object-keys sorted and circular-references removed
 */
</span>    var circularList, stringify, tmp;
    stringify = function (element) {
    /*
     * this function will recursively JSON.stringify the element,
     * with object-keys sorted and circular-references removed
     */
        // if element is an object, then recurse its items with object-keys sorted
        if (element &&
                typeof element === 'object' &&
                typeof element.toJSON !== 'function') {
            // ignore circular-reference
            if (circularList.indexOf(element) >= 0) {
                return;
            }
            circularList.push(element);
            // if element is an array, then recurse its elements
            if (Array.isArray(element)) {
                return '[' + element.map(function (element) {
                    // recurse
                    tmp = stringify(element);
                    return typeof tmp === 'string'
                        ? tmp
                        : 'null';
                }).join(',') + ']';
            }
            return '{' + Object.keys(element)
                // sort object-keys
                .sort()
                .map(function (key) {
                    // recurse
                    tmp = stringify(element[key]);
                    if (typeof tmp === 'string') {
                        return JSON.stringify(key) + ':' + tmp;
                    }
                })
                .filter(function (element) {
                    return typeof element === 'string';
                })
                .join(',') + '}';
        }
        // else JSON.stringify as normal
        return JSON.stringify(element);
    };
    circularList = [];
    return JSON.stringify(element && typeof element === 'object'
        // recurse
        ? JSON.parse(stringify(element))
        : element, replacer, space);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmDecrypt"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtA256GcmDecrypt (token, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmDecrypt)
- description and source-code
```javascript
jwtA256GcmDecrypt = function (token, key) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7516
 * this function will use json-web-encryption to
 * aes-256-gcm-decrypt the token with the given base64url-encoded key
 */
</span>    return local.tryCatchOnError(function () {
        token = token
            .replace((/-/g), '+')
            .replace((/_/g), '/')
            .split('.');
        token = local.sjcl.decrypt(local.sjcl.codec.base64url.toBits(
            local.jwtAes256KeyInit(key)
        ), JSON.stringify({
            adata: token[4],
            ct: token[3],
            iv: token[2],
            ks: 256,
            mode: 'gcm'
        }));
        return local.jwtHs256Decode(token, key);
    }, local.nop) || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmEncrypt"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtA256GcmEncrypt (data, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtA256GcmEncrypt)
- description and source-code
```javascript
jwtA256GcmEncrypt = function (data, key) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7516
 * this function will use json-web-encryption to
 * aes-256-gcm-encrypt the data with the given base64url-encoded key
 */
</span>    var adata;
    adata = local.jwtAes256KeyCreate();
    data = local.jwtHs256Encode(data, key);
    data = JSON.parse(local.sjcl.encrypt(
        local.sjcl.codec.base64url.toBits(local.jwtAes256KeyInit(key)),
        data,
        { adata: local.sjcl.codec.base64url.toBits(adata), ks: 256, mode: 'gcm' }
    ));
    return local.jwtBase64UrlNormalize('eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4R0NNIn0..' +
        data.iv + '.' + data.ct + '.' + adata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtAes256KeyCreate ()](#apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyCreate)
- description and source-code
```javascript
jwtAes256KeyCreate = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random, aes-256-base64url-jwt-key
 */
</span>    return local.jwtBase64UrlNormalize(
        local.base64FromBuffer(local.bufferRandomBytes(32))
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtAes256KeyInit (key)](#apidoc.element.n_.context.utility2_moduleExports.jwtAes256KeyInit)
- description and source-code
```javascript
jwtAes256KeyInit = function (key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will init the aes-256-base64url-jwt-key
 */
</span>    // init npm_config_jwtAes256Key
    local.env.npm_config_jwtAes256Key = local.env.npm_config_jwtAes256Key ||
        'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA';
    return key || local.env.npm_config_jwtAes256Key;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtBase64UrlNormalize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtBase64UrlNormalize (text)](#apidoc.element.n_.context.utility2_moduleExports.jwtBase64UrlNormalize)
- description and source-code
```javascript
jwtBase64UrlNormalize = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will normlize the text to base64url format
 */
</span>    return text
        .replace((/\=/g), '')
        .replace((/\+/g), '-')
        .replace((/\//g), '_');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtHs256Decode"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtHs256Decode (token, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtHs256Decode)
- description and source-code
```javascript
jwtHs256Decode = function (token, key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will decode the json-web-token with the given base64-encode key
 */
</span>    var timeNow;
    timeNow = Date.now() / 1000;
    // try to decode the token
    return local.tryCatchOnError(function () {
        token = token.split('.');
        // validate header
        local.assert(token[0] === 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9', token);
        // validate signature
        local.assert(local.sjcl.codec.base64url.fromBits(
            new local.sjcl.misc.hmac(local.sjcl.codec.base64url.toBits(
                local.jwtAes256KeyInit(key)
            )).encrypt(token[0] + '.' + token[1])
        ) === token[2]);
        // return decoded data
        token = JSON.parse(local.base64ToString(token[1]));
        // https://tools.ietf.org/html/rfc7519#section-4.1
        // validate jwt-registered-headers
        local.assert(!token.exp || token.exp >= timeNow);
        local.assert(!token.nbf || token.nbf <= timeNow);
        return token;
    }, local.nop) || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtHs256Encode"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtHs256Encode (data, key)](#apidoc.element.n_.context.utility2_moduleExports.jwtHs256Encode)
- description and source-code
```javascript
jwtHs256Encode = function (data, key) {
<span class="apidocCodeCommentSpan">/*
 * https://jwt.io/
 * this function will encode the data into a json-web-token
 * with the given base64-encode key
 */
</span>    data = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.' +
        local.jwtBase64UrlNormalize(local.base64FromString(JSON.stringify(data)));
    return data + '.' + local.sjcl.codec.base64url.fromBits(
        new local.sjcl.misc.hmac(local.sjcl.codec.base64url.toBits(
            local.jwtAes256KeyInit(key)
        )).encrypt(data)
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.jwtNormalize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>jwtNormalize (data)](#apidoc.element.n_.context.utility2_moduleExports.jwtNormalize)
- description and source-code
```javascript
jwtNormalize = function (data) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7519#section-4.1
 * this function will normalize the jwt-data with registered-headers
 */
</span>    var timeNow;
    timeNow = Date.now() / 1000;
    return local.objectSetDefault(data, {
        exp: timeNow + 5 * 60,
        iat: timeNow,
        jti: Math.random().toString(16).slice(2),
        nbf: timeNow
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.listGetElementRandom"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>listGetElementRandom (list)](#apidoc.element.n_.context.utility2_moduleExports.listGetElementRandom)
- description and source-code
```javascript
listGetElementRandom = function (list) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a random element from the list
 */
</span>    return list[Math.floor(list.length * Math.random())];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.listShuffle"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>listShuffle (list)](#apidoc.element.n_.context.utility2_moduleExports.listShuffle)
- description and source-code
```javascript
listShuffle = function (list) {
<span class="apidocCodeCommentSpan">/*
 * https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle
 * this function will inplace shuffle the list, via fisher-yates algorithm
 */
</span>    var ii, random, swap;
    for (ii = list.length - 1; ii > 0; ii -= 1) {
        // coerce to finite integer
        random = (Math.random() * (ii + 1)) | 0;
        swap = list[ii];
        list[ii] = list[random];
        list[random] = swap;
    }
    return list;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareAssetsCached"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareAssetsCached (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareAssetsCached)
- description and source-code
```javascript
middlewareAssetsCached = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will serve cached-assets
 */
</span>    var options;
    options = {};
    local.onNext(options, function (error, data) {
        options.result = options.result || local.assetsDict[request.urlParsed.pathname];
        if (options.result === undefined) {
            nextMiddleware(error);
            return;
        }
        switch (options.modeNext) {
        case 1:
            // skip gzip
            if (response.headersSent ||
                    !(/\bgzip\b/).test(request.headers['accept-encoding'])) {
                options.modeNext += 1;
                options.onNext();
                return;
            }
            // gzip and cache result
            local.taskCreateCached({
                cacheDict: 'middlewareAssetsCachedGzip',
                key: request.urlParsed.pathname
            }, function (onError) {
                local.zlib.gzip(options.result, function (error, data) {
                    onError(error, !error && data.toString('base64'));
                });
            }, options.onNext);
            break;
        case 2:
            // set gzip header
            options.result = local.base64ToBuffer(data);
            response.setHeader('Content-Encoding', 'gzip');
            response.setHeader('Content-Length', options.result.length);
            options.onNext();
            break;
        case 3:
            local.middlewareCacheControlLastModified(request, response, options.onNext);
            break;
        case 4:
            response.end(options.result);
            break;
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareBodyRead"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareBodyRead (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareBodyRead)
- description and source-code
```javascript
middlewareBodyRead = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will
 * read and save the request-body to request.bodyRaw
 */
</span>    // jslint-hack
    local.nop(response);
    // if request is already read, then goto nextMiddleware
    if (!request.readable) {
        nextMiddleware();
        return;
    }
    local.streamReadAll(request, function (error, data) {
        request.bodyRaw = request.bodyRaw || data;
        nextMiddleware(error);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareCacheControlLastModified"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareCacheControlLastModified ( request, response, nextMiddleware )](#apidoc.element.n_.context.utility2_moduleExports.middlewareCacheControlLastModified)
- description and source-code
```javascript
middlewareCacheControlLastModified = function ( request, response, nextMiddleware ) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will update the Last-Modified header
 */
</span>    // do not cache if headers already sent or url has '?' search indicator
    if (!(response.headersSent || request.url.indexOf('?') >= 0)) {
        // init serverResponseHeaderLastModified
        local.serverResponseHeaderLastModified =
            local.serverResponseHeaderLastModified ||
            // resolve to 1000 ms
            new Date(new Date(Math.floor(Date.now() / 1000) * 1000).toGMTString());
        // respond with 304 If-Modified-Since serverResponseHeaderLastModified
        if (new Date(request.headers['if-modified-since']) >=
                local.serverResponseHeaderLastModified) {
            response.statusCode = 304;
            response.end();
            return;
        }
        response.setHeader('Cache-Control', 'no-cache');
        response.setHeader(
            'Last-Modified',
            local.serverResponseHeaderLastModified.toGMTString()
        );
    }
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareFileServer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareFileServer (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareFileServer)
- description and source-code
```javascript
middlewareFileServer = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will serve files
 */
</span>    if (request.method !== 'GET' || local.modeJs === 'browser') {
        nextMiddleware();
        return;
    }
    request.urlFile = (process.cwd() + request.urlParsed.pathname
        // security - disable parent directory lookup
        .replace((/.*\/\.\.\//g), '/'))
        // replace trailing '/' with '/index.html'
        .replace((/\/$/), '/index.html');
    // serve file from cache
    local.taskCreateCached({
        cacheDict: 'middlewareFileServer',
        key: request.urlFile
    // run background-task to re-cache file
    }, function (onError) {
        local.fs.readFile(request.urlFile, function (error, data) {
            onError(error, data && local.base64FromBuffer(data));
        });
    }, function (error, data) {
        // default to nextMiddleware
        if (error) {
            nextMiddleware();
            return;
        }
        // init response-header content-type
        request.urlParsed.contentType = (/\.[^\.]*$/).exec(request.urlParsed.pathname);
        request.urlParsed.contentType = local.contentTypeDict[
            request.urlParsed.contentType && request.urlParsed.contentType[0]
        ];
        local.serverRespondHeadSet(request, response, null, {
            'Content-Type': request.urlParsed.contentType
        });
        // serve file from cache
        response.end(local.base64ToBuffer(data));
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareForwardProxy"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareForwardProxy (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareForwardProxy)
- description and source-code
```javascript
middlewareForwardProxy = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will forward-proxy the request
 * to its destination-host
 */
</span>    var onError, options, timerTimeout;
    // handle preflight-cors
    if ((request.headers['access-control-request-headers'] || '')
            .indexOf('forward-proxy-url') >= 0) {
        // enable cors
        // http://en.wikipedia.org/wiki/Cross-origin_resource_sharing
        local.serverRespondHeadSet(request, response, null, {
            'Access-Control-Allow-Headers': 'forward-proxy-headers,forward-proxy-url',
            'Access-Control-Allow-Methods': 'DELETE,GET,HEAD,OPTIONS,PATCH,POST,PUT',
            'Access-Control-Allow-Origin': '*'
        });
        response.end();
        return;
    }
    if (!request.headers['forward-proxy-url']) {
        nextMiddleware();
        return;
    }
    // enable cors
    // http://en.wikipedia.org/wiki/Cross-origin_resource_sharing
    local.serverRespondHeadSet(request, response, null, {
        'Access-Control-Allow-Headers': 'forward-proxy-headers,forward-proxy-url',
        'Access-Control-Allow-Methods': 'DELETE,GET,HEAD,OPTIONS,PATCH,POST,PUT',
        'Access-Control-Allow-Origin': '*'
    });
    // init onError
    onError = function (error) {
        clearTimeout(timerTimeout);
        if (!error || options.done) {
            return;
        }
        options.done = true;
        // cleanup client
        local.streamListCleanup([options.clientRequest, options.clientResponse]);
        nextMiddleware(error);
    };
    // init options
    options = local.urlParse(request.headers['forward-proxy-url']);
    options.method = request.method;
    options.url = request.headers['forward-proxy-url'];
    // init timerTimeout
    timerTimeout = local.onTimeout(
        onError,
        local.timeoutDefault,
        'forward-proxy ' + options.method + ' ' + options.url
    );
    // parse headers
    options.headers = {};
    local.tryCatchOnError(function () {
        options.headers = JSON.parse(request.headers['forward-proxy-headers']);
    }, local.nop);
    // debug options
    local._debugForwardProxy = options;
    console.error(new Date().toISOString() + ' middlewareForwardProxy ' +
        JSON.stringify({
            method: options.method,
            url: options.url,
            headers: options.headers
        }));
    options.clientRequest = (options.protocol === 'https:'
        ? local.https
        : local.http).request(options, function (clientResponse) {
        options.clientResponse = clientResponse.on('error', onError);
        // pipe clientResponse to serverResponse
        options.clientResponse.pipe(response);
    }).on('error', onError);
    // init event-handling
    request.on('error', onError);
    response.on('finish', onError).on('error', onError);
    // pipe serverRequest to clientRequest
    request.pipe(options.clientRequest);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareGroupCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareGroupCreate (middlewareList)](#apidoc.element.n_.context.utility2_moduleExports.middlewareGroupCreate)
- description and source-code
```javascript
middlewareGroupCreate = function (middlewareList) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a middleware that will
 * sequentially run the sub-middlewares in middlewareList
 */
</span>    var self;
    self = function (request, response, nextMiddleware) {
        var options;
        options = {};
        local.onNext(options, function (error) {
            // recurse with next middleware in middlewareList
            if (options.modeNext < self.middlewareList.length) {
                // run the sub-middleware
                self.middlewareList[options.modeNext](
                    request,
                    response,
                    options.onNext
                );
                return;
            }
            // default to nextMiddleware
            nextMiddleware(error);
        });
        options.modeNext = -1;
        options.onNext();
    };
    self.middlewareList = middlewareList;
    return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.middlewareInit"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>middlewareInit (request, response, nextMiddleware)](#apidoc.element.n_.context.utility2_moduleExports.middlewareInit)
- description and source-code
```javascript
middlewareInit = function (request, response, nextMiddleware) {
<span class="apidocCodeCommentSpan">/*
 * this function will run the middleware that will init the request and response
 */
</span>    // debug server-request
    local._debugServerRequest = request;
    // debug server-response
    local._debugServerResponse = response;
    // init timerTimeout
    local.serverRespondTimeoutDefault(request, response, local.timeoutDefault);
    // init request.urlParsed
    request.urlParsed = local.urlParse(request.url);
    // init response-header content-type
    request.urlParsed.contentType = (/\.[^\.]*$/).exec(request.urlParsed.pathname);
    request.urlParsed.contentType = local.contentTypeDict[
        request.urlParsed.contentType && request.urlParsed.contentType[0]
    ];
    local.serverRespondHeadSet(request, response, null, {
        'Content-Type': request.urlParsed.contentType
    });
    // set main-page content-type to text/html
    if (request.urlParsed.pathname === '/') {
        local.serverRespondHeadSet(request, response, null, {
            'Content-Type': 'text/html; charset=UTF-8'
        });
    }
    // init response.end and response.write to accept Uint8Array instance
    ['end', 'write'].forEach(function (key) {
        response['_' + key] = response['_' + key] || response[key];
        response[key] = function () {
            var args;
            args = Array.from(arguments);
            args[0] = local.bufferToNodeBuffer(args[0]);
            response['_' + key].apply(response, args);
        };
    });
    // default to nextMiddleware
    nextMiddleware();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.moduleDirname"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>moduleDirname (module, modulePathList)](#apidoc.element.n_.context.utility2_moduleExports.moduleDirname)
- description and source-code
```javascript
moduleDirname = function (module, modulePathList) {
<span class="apidocCodeCommentSpan">/*
 * this function will search modulePathList for the module's __dirname
 */
</span>    var result, tmp;
    // search process.cwd()
    if (!module || module === '.' || module.indexOf('/') >= 0) {
        return require('path').resolve(process.cwd(), module || '');
    }
    // search builtin
    if (Object.keys(process.binding('natives')).indexOf(module) >= 0) {
        return module;
    }
    // search modulePathList
    [
        ['node_modules'],
        modulePathList,
        require('module').globalPaths
    ].some(function (modulePathList) {
        modulePathList.some(function (modulePath) {
            try {
                tmp = require('path').resolve(
                    process.cwd(),
                    modulePath + '/' + module
                );
                result = require('fs').statSync(tmp).isDirectory() && tmp;
                return result;
            } catch (ignore) {
            }
        });
        return result;
    });
    return result || '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.nop"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>nop ()](#apidoc.element.n_.context.utility2_moduleExports.nop)
- description and source-code
```javascript
nop = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.normalizeDict"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeDict (dict)](#apidoc.element.n_.context.utility2_moduleExports.normalizeDict)
- description and source-code
```javascript
normalizeDict = function (dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the dict
 */
</span>    return dict && typeof dict === 'object' && !Array.isArray(dict)
        ? dict
        : {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.normalizeList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeList (list)](#apidoc.element.n_.context.utility2_moduleExports.normalizeList)
- description and source-code
```javascript
normalizeList = function (list) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the list
 */
</span>    return Array.isArray(list)
        ? list
        : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.normalizeText"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>normalizeText (text)](#apidoc.element.n_.context.utility2_moduleExports.normalizeText)
- description and source-code
```javascript
normalizeText = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will normalize the text
 */
</span>    return typeof text === 'string'
        ? text
        : '';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectGetElementFirst"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectGetElementFirst (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectGetElementFirst)
- description and source-code
```javascript
objectGetElementFirst = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will get the first element of the arg
 */
</span>    var item;
    item = {};
    item.key = Object.keys(arg)[0];
    item.value = arg[item.key];
    return item;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectKeysTypeof"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectKeysTypeof (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectKeysTypeof)
- description and source-code
```javascript
objectKeysTypeof = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will return a list of the arg's keys, sorted by item-type
 */
</span>    return Object.keys(arg).map(function (key) {
        return typeof arg[key] + ' ' + key;
    }).sort().join('\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectLiteralize"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectLiteralize (arg)](#apidoc.element.n_.context.utility2_moduleExports.objectLiteralize)
- description and source-code
```javascript
objectLiteralize = function (arg) {
<span class="apidocCodeCommentSpan">/*
 * this function will traverse arg, and replace every encounter of the magical key '$[]'
 * with its object literal [key, value]
 */
</span>    local.objectTraverse(arg, function (element) {
        if (element && typeof element === 'object' && !Array.isArray(element)) {
            Object.keys(element).forEach(function (key) {
                if (key.indexOf('$[]') === 0) {
                    element[element[key][0]] = element[key][1];
                    delete element[key];
                }
            });
        }
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectSetDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectSetDefault (arg, defaults, depth)](#apidoc.element.n_.context.utility2_moduleExports.objectSetDefault)
- description and source-code
```javascript
objectSetDefault = function (arg, defaults, depth) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively set defaults for undefined-items in the arg
 */
</span>    arg = arg || {};
    defaults = defaults || {};
    Object.keys(defaults).forEach(function (key) {
        var arg2, defaults2;
        arg2 = arg[key];
        // handle misbehaving getter
        try {
            defaults2 = defaults[key];
        } catch (ignore) {
        }
        if (defaults2 === undefined) {
            return;
        }
        // init arg[key] to default value defaults[key]
        if (!arg2) {
            arg[key] = defaults2;
            return;
        }
        // if arg2 and defaults2 are both non-null and non-array objects,
        // then recurse with arg2 and defaults2
        if (depth > 1 &&
                // arg2 is a non-null and non-array object
                arg2 &&
                typeof arg2 === 'object' &&
                !Array.isArray(arg2) &&
                // defaults2 is a non-null and non-array object
                defaults2 &&
                typeof defaults2 === 'object' &&
                !Array.isArray(defaults2)) {
            // recurse
            local.objectSetDefault(arg2, defaults2, depth - 1);
        }
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectSetOverride"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectSetOverride (arg, overrides, depth, env)](#apidoc.element.n_.context.utility2_moduleExports.objectSetOverride)
- description and source-code
```javascript
objectSetOverride = function (arg, overrides, depth, env) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively set overrides for items in the arg
 */
</span>    arg = arg || {};
    env = env || (typeof process === 'object' && process.env) || {};
    overrides = overrides || {};
    Object.keys(overrides).forEach(function (key) {
        var arg2, overrides2;
        arg2 = arg[key];
        overrides2 = overrides[key];
        if (overrides2 === undefined) {
            return;
        }
        // if both arg2 and overrides2 are non-null and non-array objects,
        // then recurse with arg2 and overrides2
        if (depth > 1 &&
                // arg2 is a non-null and non-array object
                (arg2 &&
                typeof arg2 === 'object' &&
                !Array.isArray(arg2)) &&
                // overrides2 is a non-null and non-array object
                (overrides2 &&
                typeof overrides2 === 'object' &&
                !Array.isArray(overrides2))) {
            local.objectSetOverride(arg2, overrides2, depth - 1, env);
            return;
        }
        // else set arg[key] with overrides[key]
        arg[key] = arg === env
            // if arg is env, then overrides falsey value with empty string
            ? overrides2 || ''
            : overrides2;
    });
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.objectTraverse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>objectTraverse (arg, onSelf, circularList)](#apidoc.element.n_.context.utility2_moduleExports.objectTraverse)
- description and source-code
```javascript
objectTraverse = function (arg, onSelf, circularList) {
<span class="apidocCodeCommentSpan">/*
 * this function will recursively traverse the arg,
 * and run onSelf with the arg's properties
 */
</span>    onSelf(arg);
    circularList = circularList || [];
    if (arg &&
            typeof arg === 'object' &&
            circularList.indexOf(arg) < 0) {
        circularList.push(arg);
        Object.keys(arg).forEach(function (key) {
            // recurse with arg[key]
            local.objectTraverse(arg[key], onSelf, circularList);
        });
    }
    return arg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onErrorDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorDefault (error)](#apidoc.element.n_.context.utility2_moduleExports.onErrorDefault)
- description and source-code
```javascript
onErrorDefault = function (error) {
<span class="apidocCodeCommentSpan">/*
 * this function will if error exists, then print error.stack to stderr
 */
</span>    if (error && !local.global.__coverage__) {
        console.error(error.stack);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onErrorThrow"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorThrow (error)](#apidoc.element.n_.context.utility2_moduleExports.onErrorThrow)
- description and source-code
```javascript
onErrorThrow = function (error) {
<span class="apidocCodeCommentSpan">/*
 * this function will assert no error occurred
 */
</span>    if (error) {
        throw error;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onErrorWithStack"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onErrorWithStack (onError)](#apidoc.element.n_.context.utility2_moduleExports.onErrorWithStack)
- description and source-code
```javascript
onErrorWithStack = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a new callback that will call onError,
 * and append the current stack to any error
 */
</span>    var stack;
    stack = new Error().stack.replace((/(.*?)\n.*?$/m), '$1');
    return function (error, data, meta) {
        if (error &&
                error !== local.errorDefault &&
                String(error.stack).indexOf(stack.split('\n')[2]) < 0) {
            // append the current stack to error.stack
            error.stack += '\n' + stack;
        }
        onError(error, data, meta);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onFileModifiedRestart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onFileModifiedRestart (file)](#apidoc.element.n_.context.utility2_moduleExports.onFileModifiedRestart)
- description and source-code
```javascript
onFileModifiedRestart = function (file) {
<span class="apidocCodeCommentSpan">/*
 * this function will watch the file, and if modified, then restart the process
 */
</span>    if (local.env.npm_config_mode_auto_restart &&
            local.fs.existsSync(file) &&
            local.fs.statSync(file).isFile()) {
        local.fs.watchFile(file, {
            interval: 1000,
            persistent: false
        }, function (stat2, stat1) {
            if (stat2.mtime > stat1.mtime) {
                console.error('file modified - ' + file);
                local.exit(77);
            }
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onNext"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onNext (options, onError)](#apidoc.element.n_.context.utility2_moduleExports.onNext)
- description and source-code
```javascript
onNext = function (options, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will wrap onError inside the recursive function options.onNext,
 * and append the current stack to any error
 */
</span>    options.onNext = local.onErrorWithStack(function (error, data, meta) {
        try {
            options.modeNext = error && !options.modeErrorIgnore
                ? Infinity
                : options.modeNext + 1;
            onError(error, data, meta);
        } catch (errorCaught) {
            // throw errorCaught to break infinite recursion-loop
            if (options.errorCaught) {
                throw options.errorCaught;
            }
            options.errorCaught = errorCaught;
            options.onNext(errorCaught, data, meta);
        }
    });
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onParallel"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onParallel (onError, onEach, onRetry)](#apidoc.element.n_.context.utility2_moduleExports.onParallel)
- description and source-code
```javascript
onParallel = function (onError, onEach, onRetry) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a function that will
 * 1. run async tasks in parallel
 * 2. if counter === 0 or error occurred, then call onError with error
 */
</span>    var onParallel;
    onError = local.onErrorWithStack(onError);
    onEach = onEach || local.nop;
    onRetry = onRetry || local.nop;
    onParallel = function (error, data) {
        if (onRetry(error, data)) {
            return;
        }
        // decrement counter
        onParallel.counter -= 1;
        // validate counter
        console.assert(onParallel.counter >= 0 || error || onParallel.error);
        // ensure onError is run only once
        if (onParallel.counter < 0) {
            return;
        }
        // handle error
        if (error) {
            onParallel.error = error;
            // ensure counter <= 0
            onParallel.counter = -Math.abs(onParallel.counter);
        }
        // call onError when done
        if (onParallel.counter <= 0) {
            onError(error, data);
            return;
        }
        onEach();
    };
    // init counter
    onParallel.counter = 0;
    // return callback
    return onParallel;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onParallelList"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onParallelList (options, onEach, onError)](#apidoc.element.n_.context.utility2_moduleExports.onParallelList)
- description and source-code
```javascript
onParallelList = function (options, onEach, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. async-run onEach in parallel,
 *    with the given options.rateLimit and options.retryLimit
 * 2. call onError when done
 */
</span>    var ii, onEach2, onParallel;
    onEach2 = function () {
        while (ii + 1 < options.list.length && onParallel.counter < options.rateLimit) {
            ii += 1;
            onParallel.ii += 1;
            onParallel.remaining -= 1;
            onEach({
                element: options.list[ii],
                ii: ii,
                list: options.list,
                retry: 0
            }, onParallel);
        }
    };
    onParallel = local.onParallel(onError, onEach2, function (error, data) {
        if (error && data && data.retry < options.retryLimit) {
            local.onErrorDefault(error);
            data.retry += 1;
            setTimeout(function () {
                onParallel.counter -= 1;
                onEach(data, onParallel);
            }, 1000);
            return true;
        }
    });
    onParallel.counter += 1;
    ii = -1;
    onParallel.ii = -1;
    onParallel.remaining = options.list.length;
    options.rateLimit = Number(options.rateLimit) || 4;
    options.rateLimit = Math.max(options.rateLimit, 3);
    options.retryLimit = Number(options.retryLimit) || 2;
    onEach2();
    onParallel();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onReadyAfter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onReadyAfter (onError)](#apidoc.element.n_.context.utility2_moduleExports.onReadyAfter)
- description and source-code
```javascript
onReadyAfter = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will call onError when onReadyBefore.counter === 0
 */
</span>    local.onReadyBefore.counter += 1;
    local.taskCreate({ key: 'utility2.onReadyAfter' }, null, onError);
    local.onResetAfter(local.onReadyBefore);
    return onError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onReadyBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onReadyBefore (error, data)](#apidoc.element.n_.context.utility2_moduleExports.onReadyBefore)
- description and source-code
```javascript
onReadyBefore = function (error, data) {
    if (onRetry(error, data)) {
        return;
    }
    // decrement counter
    onParallel.counter -= 1;
    // validate counter
    console.assert(onParallel.counter >= 0 || error || onParallel.error);
    // ensure onError is run only once
    if (onParallel.counter < 0) {
        return;
    }
    // handle error
    if (error) {
        onParallel.error = error;
        // ensure counter <= 0
        onParallel.counter = -Math.abs(onParallel.counter);
    }
    // call onError when done
    if (onParallel.counter <= 0) {
        onError(error, data);
        return;
    }
    onEach();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onResetAfter"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onResetAfter (onError)](#apidoc.element.n_.context.utility2_moduleExports.onResetAfter)
- description and source-code
```javascript
onResetAfter = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will call onError when onResetBefore.counter === 0
 */
</span>    local.onResetBefore.counter += 1;
    // visual notification - onResetAfter
    local.ajaxProgressUpdate();
    local.taskCreate({ key: 'utility2.onResetAfter' }, null, onError);
    setTimeout(local.onResetBefore);
    return onError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onResetBefore"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onResetBefore (error, data)](#apidoc.element.n_.context.utility2_moduleExports.onResetBefore)
- description and source-code
```javascript
onResetBefore = function (error, data) {
    if (onRetry(error, data)) {
        return;
    }
    // decrement counter
    onParallel.counter -= 1;
    // validate counter
    console.assert(onParallel.counter >= 0 || error || onParallel.error);
    // ensure onError is run only once
    if (onParallel.counter < 0) {
        return;
    }
    // handle error
    if (error) {
        onParallel.error = error;
        // ensure counter <= 0
        onParallel.counter = -Math.abs(onParallel.counter);
    }
    // call onError when done
    if (onParallel.counter <= 0) {
        onError(error, data);
        return;
    }
    onEach();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.onTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>onTimeout (onError, timeout, message)](#apidoc.element.n_.context.utility2_moduleExports.onTimeout)
- description and source-code
```javascript
onTimeout = function (onError, timeout, message) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a timeout-error-handler,
 * that will append the current stack to any error encountered
 */
</span>    onError = local.onErrorWithStack(onError);
    // create timeout timer
    return setTimeout(function () {
        onError(new Error('onTimeout - timeout-error - ' +
            timeout + ' ms - ' + (typeof message === 'function'
            ? message()
            : message)));
    // coerce to finite integer
    }, timeout | 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.processSpawnWithTimeout"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>processSpawnWithTimeout ()](#apidoc.element.n_.context.utility2_moduleExports.processSpawnWithTimeout)
- description and source-code
```javascript
processSpawnWithTimeout = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will run like child_process.spawn,
 * but with auto-timeout after timeoutDefault milliseconds
 */
</span>    var childProcess;
    // spawn childProcess
    childProcess = local.child_process.spawn.apply(local.child_process, arguments)
        .on('exit', function () {
            // try to kill timerTimeout childProcess
            local.tryCatchOnError(function () {
                process.kill(childProcess.timerTimeout.pid);
            }, local.nop);
        });
    // init failsafe timerTimeout
    childProcess.timerTimeout = local.child_process.spawn('/bin/sh', ['-c', 'sleep ' +
        // coerce to finite integer
        (((0.001 * local.timeoutDefault) | 0) +
        // add 2 second delay to failsafe timerTimeout
        2) + '; kill -9 ' + childProcess.pid + ' 2>/dev/null'], { stdio: 'ignore' });
    return childProcess;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.profile"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>profile (fnc, onError)](#apidoc.element.n_.context.utility2_moduleExports.profile)
- description and source-code
```javascript
profile = function (fnc, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will profile the async fnc in milliseconds with the callback onError
 */
</span>    var timeStart;
    timeStart = Date.now();
    // run async fnc
    fnc(function (error) {
        // call onError with difference in milliseconds between Date.now() and timeStart
        onError(error, Date.now() - timeStart);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.profileSync"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>profileSync (fnc)](#apidoc.element.n_.context.utility2_moduleExports.profileSync)
- description and source-code
```javascript
profileSync = function (fnc) {
<span class="apidocCodeCommentSpan">/*
 * this function will profile the sync fnc in milliseconds
 */
</span>    var timeStart;
    timeStart = Date.now();
    // run sync fnc
    fnc();
    // return difference in milliseconds between Date.now() and timeStart
    return Date.now() - timeStart;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.replStart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>replStart ()](#apidoc.element.n_.context.utility2_moduleExports.replStart)
- description and source-code
```javascript
replStart = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will start the repl-debugger
 */
</span>    /*jslint evil: true*/
    var self;
    if (global.utility2_serverRepl1) {
        return;
    }
    // start replServer
    self = global.utility2_serverRepl1 = require('repl').start({ useGlobal: true });
    self.nop = function () {
    /*
     * this function will do nothing
     */
        return;
    };
    self.onError = function (error) {
    /*
     * this function will debug any repl-error
     */
        // debug error
        global.utility2_debugReplError = error;
        console.error(error.stack);
    };
    // save repl eval function
    self.evalDefault = self.eval;
    // hook custom repl eval function
    self.eval = function (script, context, file, onError) {
        var match, onError2;
        match = (/^(\S+)(.*?)\n/).exec(script);
        onError2 = function (error, data) {
            // debug error
            global.utility2_debugReplError = error || global.utility2_debugReplError;
            onError(error, data);
        };
        switch (match && match[1]) {
        // syntax sugar to run async shell command
        case '$':
            switch (match[2]) {
            // syntax sugar to run git diff
            case ' git diff':
                match[2] = ' git diff --color | cat';
                break;
            // syntax sugar to run git log
            case ' git log':
                match[2] = ' git log -n 4 | cat';
                break;
            }
            // run async shell command
            require('child_process').spawn(
                '/bin/sh',
                ['-c', match[2]],
                { stdio: ['ignore', 1, 2] }
            )
                // on shell exit, print return prompt
                .on('exit', function (exitCode) {
                    console.error('exit-code ' + exitCode);
                    self.evalDefault(
                        '\n',
                        context,
                        file,
                        onError2
                    );
                });
            script = '\n';
            break;
        // syntax sugar to grep current dir
        case 'grep':
            // run async shell command
            require('child_process').spawn(
                '/bin/sh',
                ['-c', 'find . -type f | grep -v ' +
/* jslint-ignore-begin */
'"\
/\\.\\|.*\\(\\b\\|_\\)\\(\\.\\d\\|\
archive\\|artifact\\|\
bower_component\\|build\\|\
coverage\\|\
doc\\|\
external\\|\
fixture\\|\
git_module\\|\
jquery\\|\
log\\|\
min\\|mock\\|\
node_module\\|\
rollup\\|\
swp\\|\
tmp\\|\
vendor\\)\\(\\b\\|[_s]\\)\
" ' +
/* jslint-ignore-end */
                    '| tr "\\n" "\\000" | xargs -0 grep -in "' +
                    match[2].trim() + '"'],
                { stdio: ['ignore', 1, 2] }
            )
                // on shell exit, print return prompt
                .on('exit', function (exitCode) {
                    console.error('exit-code ' + exitCode);
                    self.evalDefault(
                        '\n',
                        context,
                        file,
                        onError2
                    );
                });
            script = '\n';
            break;
        // syntax sugar to list object's keys, sorted by item-type
        case 'keys':
            script = 'console.error(Object.keys(' + match[2] +
                ').map(function (key) {' +
                'return typeof ' + match[2] + '[key] + " " + key + "\\n";' +
                '}).sort().join("") + Object.keys(' + match[2] + ').length)\n';
            break;
        // syntax sugar to print stringified arg
        case 'print':
            script = 'console.error(String(' + match[2] + '))\n';
            break;
        }
        // eval the script
        self.evalDefault(script, context, file, onError2);
    };
    self.socket = { end: self.nop, on: self.nop, write: self.nop };
    // init process.stdout
    process.stdout._writeDefault = process.stdout._writeDefault ||
        process.stdout._write;
    process.stdout._write = function (chunk, e ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.requireExampleJsFromReadme"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>requireExampleJsFromReadme ()](#apidoc.element.n_.context.utility2_moduleExports.requireExampleJsFromReadme)
- description and source-code
```javascript
requireExampleJsFromReadme = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will require and export example.js embedded in README.md
 */
</span>    var module, script, tmp;
    // start the repl-debugger
    local.replStart();
    // debug dir
    [__dirname, process.cwd()].forEach(function (dir) {
        local.fs.readdirSync(dir).forEach(function (file) {
            if ((/\brollup\b/).test(file)) {
                return;
            }
            file = dir + '/' + file;
            // if the file is modified, then restart the process
            local.onFileModifiedRestart(file);
            switch (local.path.extname(file)) {
            case '.css':
            case '.html':
            case '.js':
            case '.json':
                // jslint file
                local.jslintAndPrintConditional(
                    local.tryCatchReadFile(file, 'utf8'),
                    file
                );
                break;
            }
        });
    });
    if (local.global.utility2_rollup || local.env.npm_config_mode_start) {
        // init assets
        local.assetsDict['/'] = local.assetsDict['/index.html'] = local.templateRender(
            // uncomment utility2-comment
            local.assetsDict['/assets.index.template.html'].replace(
                (/<!-- utility2-comment\b([\S\s]+?)\butility2-comment -->/g),
                '$1'
            ),
            { env: local.env, isRollup: true }
        );
        local.assetsDict['/assets.example.js'] =
            local.assetsDict['/assets.example.template.js'];
        local.assetsDict['/assets.app.js'] =
            local.fs.readFileSync(__filename, 'utf8').replace((/^#!/), '//');
        // coverage-hack
        local.nop(local.env.npm_config_mode_start && (function () {
            local.assetsDict['/assets.app.js'] =
                local.assetsDict['/assets.utility2.rollup.begin.js'];
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.fs.readFileSync(__filename, 'utf8').replace((/^#!/), '//');
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.assetsDict['/assets.example.js'];
            local.assetsDict['/assets.app.js'] += '\n\n\n' +
                local.assetsDict['/assets.test.js'];
            local.global.local = local;
        }()));
        local[local.env.npm_package_nameAlias] = local;
        return local;
    }
    // init file $npm_package_main
    tmp = process.cwd() + '/' + local.env.npm_package_main;
    global.utility2_moduleExports = require(tmp);
    local.assetsDict['/assets.' + local.env.npm_package_nameAlias + '.js'] =
        local.istanbulInstrumentInPackage(
            local.fs.readFileSync(tmp, 'utf8').replace((/^#!/), '//'),
            tmp
        );
    global.utility2_moduleExports.global = global;
    // read script from README.md
    script = local.templateRenderJslintLite(
        local.assetsDict['/assets.example.template.js'],
        {}
    );
    // coverage-hack
    local.nop(local.env.npm_package_readmeParse && (function () {
        local.fs.readFileSync('README.md', 'utf8').replace(
            (/'''\w*?(\n[\W\s]*?example\.js[\n\"][\S\s]+?)\n'''/),
            function (match0, match1, ii, text) {
                // jslint-hack
                local.nop(match0);
                // preserve lineno
                script = text.slice(0, ii).replace((/.+/g), '') + match1;
            }
        );
    }()));
    script = script
        // alias require($npm_package_name) to utility2_moduleExports;
        .replace(
            "require('" + local.env.npm_package_name + "')",
            'global.utility2_moduleExports'
        )
        .replace(
            "require('" + local.env.npm_package_nameOriginal + "')",
            'global.utility2_moduleExports'
        );
    // init example.js
    tmp = process.cwd() + '/example.js';
    // jslint script
    local.jslintAndPrintConditional(script, tmp);
    // cover script
    script = local.istanbulInstrumentInPackage(script, tmp);
    // init module
    module = require.cache[tmp] = new local.Module(tmp);
    // load script into module
    mo ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.serverRespondDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondDefault (request, response, statusCode, error)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondDefault)
- description and source-code
```javascript
serverRespondDefault = function (request, response, statusCode, error) {
<span class="apidocCodeCommentSpan">/*
 * this function will respond with a default message,
 * or error.stack for the given statusCode
 */
</span>    // init statusCode and contentType
    local.serverRespondHeadSet(
        request,
        response,
        statusCode,
        { 'Content-Type': 'text/plain; charset=utf-8' }
    );
    if (error) {
        // debug statusCode / method / url
        local.errorMessagePrepend(
            error,
            response.statusCode + ' ' + request.method + ' ' + request.url + '\n'
        );
        // print error.stack to stderr
        local.onErrorDefault(error);
        // end response with error.stack
        response.end(error.stack);
        return;
    }
    // end response with default statusCode message
    response.end(
        statusCode + ' ' + local.http.STATUS_CODES[statusCode]
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.serverRespondEcho"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondEcho (request, response)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondEcho)
- description and source-code
```javascript
serverRespondEcho = function (request, response) {
<span class="apidocCodeCommentSpan">/*
 * this function will respond with debug info
 */
</span>    response.write(request.method + ' ' + request.url +
        ' HTTP/' + request.httpVersion + '\r\n' +
        Object.keys(request.headers).map(function (key) {
            return key + ': ' + request.headers[key] + '\r\n';
        }).join('') + '\r\n');
    request.pipe(response);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.serverRespondHeadSet"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondHeadSet (request, response, statusCode, headers)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondHeadSet)
- description and source-code
```javascript
serverRespondHeadSet = function (request, response, statusCode, headers) {
<span class="apidocCodeCommentSpan">/*
 * this function will set the response object's statusCode / headers
 */
</span>    // jslint-hack
    local.nop(request);
    if (response.headersSent) {
        return;
    }
    // init response.statusCode
    if (Number(statusCode)) {
        response.statusCode = Number(statusCode);
    }
    Object.keys(headers).forEach(function (key) {
        if (headers[key]) {
            response.setHeader(key, headers[key]);
        }
    });
    return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.serverRespondTimeoutDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>serverRespondTimeoutDefault (request, response, timeout)](#apidoc.element.n_.context.utility2_moduleExports.serverRespondTimeoutDefault)
- description and source-code
```javascript
serverRespondTimeoutDefault = function (request, response, timeout) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a timeout-error-handler for the server-request
 */
</span>    request.onTimeout = request.onTimeout || function (error) {
        local.serverRespondDefault(request, response, 500, error);
        setTimeout(function () {
            // cleanup request and response
            local.streamListCleanup([request, response]);
        }, 1000);
    };
    request.timerTimeout = local.onTimeout(
        request.onTimeout,
        timeout || local.timeoutDefault,
        'server ' + request.method + ' ' + request.url
    );
    response.on('finish', function () {
        // cleanup timerTimeout
        clearTimeout(request.timerTimeout);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.setTimeoutOnError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>setTimeoutOnError (onError, error, data)](#apidoc.element.n_.context.utility2_moduleExports.setTimeoutOnError)
- description and source-code
```javascript
setTimeoutOnError = function (onError, error, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will async-call onError
 */
</span>    if (typeof onError === 'function') {
        setTimeout(function () {
            onError(error, data);
        });
    }
    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashScryptCreate (password, options)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptCreate)
- description and source-code
```javascript
sjclHashScryptCreate = function (password, options) {
<span class="apidocCodeCommentSpan">/*
 * https://github.com/wg/scrypt
 * this function will create a scrypt-hash of the password
 * with the given options (default = $s0$10801)
 * e.g. $s0$e0801$epIxT/h6HbbwHaehFnh/bw==$7H0vsXlY8UxxyW/BWx/9GuY7jEvGjT71GFd6O4SZND0=
 */
</span>    // init options
    options = (options || '$s0$10801').split('$');
    // init salt
    if (!options[3]) {
        options[3] = local.sjcl.codec.base64.fromBits(
            local.sjcl.random.randomWords(4, 0)
        );
    }
    // init hash
    options[4] = local.sjcl.codec.base64.fromBits(
        local.sjcl.misc.scrypt(
            password || '',
            local.sjcl.codec.base64.toBits(options[3]),
            Math.pow(2, parseInt(options[2].slice(0, 1), 16)),
            parseInt(options[2].slice(1, 2), 16),
            parseInt(options[2].slice(3, 4), 16)
        )
    );
    return options.slice(0, 5).join('$');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptValidate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashScryptValidate (password, hash)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashScryptValidate)
- description and source-code
```javascript
sjclHashScryptValidate = function (password, hash) {
<span class="apidocCodeCommentSpan">/*
 * https://github.com/wg/scrypt
 * this function will validate the password against the scrypt-hash
 */
</span>    return local.sjclHashScryptCreate(password, hash) === hash;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.sjclHashSha256Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHashSha256Create (data)](#apidoc.element.n_.context.utility2_moduleExports.sjclHashSha256Create)
- description and source-code
```javascript
sjclHashSha256Create = function (data) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a base64-encoded sha-256 hash of the string data
 */
</span>    return local.sjcl.codec.base64.fromBits(local.sjcl.hash.sha256.hash(data));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.sjclHmacSha256Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>sjclHmacSha256Create (key, data)](#apidoc.element.n_.context.utility2_moduleExports.sjclHmacSha256Create)
- description and source-code
```javascript
sjclHmacSha256Create = function (key, data) {
<span class="apidocCodeCommentSpan">/*
 * this function will create a base64-encoded sha-256 hmac
 * from the base64-encoded key and string data
 */
</span>    return local.sjcl.codec.base64.fromBits(
        (new local.sjcl.misc.hmac(
            local.sjcl.codec.base64.toBits(key),
            local.sjcl.hash.sha256
        )).mac(local.sjcl.codec.utf8String.toBits(data))
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.streamListCleanup"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>streamListCleanup (streamList)](#apidoc.element.n_.context.utility2_moduleExports.streamListCleanup)
- description and source-code
```javascript
streamListCleanup = function (streamList) {
<span class="apidocCodeCommentSpan">/*
 * this function will end or destroy the streams in streamList
 */
</span>    streamList.forEach(function (stream) {
        // try to end the stream
        local.tryCatchOnError(function () {
            stream.end();
        }, function () {
            // if error, then try to destroy the stream
            local.tryCatchOnError(function () {
                stream.destroy();
            }, local.nop);
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.streamReadAll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>streamReadAll (stream, onError)](#apidoc.element.n_.context.utility2_moduleExports.streamReadAll)
- description and source-code
```javascript
streamReadAll = function (stream, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will concat data from the stream,
 * and pass it to onError when done reading
 */
</span>    var chunkList;
    chunkList = [];
    // read data from the stream
    stream
        // on data event, push the buffer chunk to chunkList
        .on('data', function (chunk) {
            chunkList.push(chunk);
        })
        // on end event, pass concatenated read buffer to onError
        .on('end', function () {
            onError(null, local.modeJs === 'browser'
                ? chunkList[0]
                : local.bufferConcat(chunkList));
        })
        // on error event, pass error to onError
        .on('error', onError);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.stringHtmlSafe"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>stringHtmlSafe (text)](#apidoc.element.n_.context.utility2_moduleExports.stringHtmlSafe)
- description and source-code
```javascript
stringHtmlSafe = function (text) {
<span class="apidocCodeCommentSpan">/*
 * this function will make the text html-safe
 */
</span>    // new RegExp('[' + '"&\'<>'.split('').sort().join('') + ']', 'g')
    return text.replace((/["&'<>]/g), function (match0) {
        return '&#x' + match0.charCodeAt(0).toString(16) + ';';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.taskCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>taskCreate (options, onTask, onError)](#apidoc.element.n_.context.utility2_moduleExports.taskCreate)
- description and source-code
```javascript
taskCreate = function (options, onTask, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will create the task onTask named options.key, if it does not exist,
 * and push onError to its onErrorList
 */
</span>    var task;
    // init task
    task = local.taskOnTaskDict[options.key] = local.taskOnTaskDict[options.key] ||
        { onErrorList: [] };
    // push callback onError to the task
    if (onError) {
        onError = local.onErrorWithStack(onError);
        task.onErrorList.push(onError);
    }
    // if task exists, then return it
    if (!onTask || task.onTask) {
        return task;
    }
    task.onDone = function () {
        // if already done, then do nothing
        if (task.done) {
            return;
        }
        task.done = true;
        // cleanup timerTimeout
        clearTimeout(task.timerTimeout);
        // cleanup task
        delete local.taskOnTaskDict[options.key];
        // preserve error.message and error.stack
        task.result = JSON.stringify(Array.from(arguments)
            .map(function (element) {
                if (element && element.stack) {
                    element = local.objectSetDefault(local.jsonCopy(element), {
                        message: element.message,
                        name: element.name,
                        stack: element.stack
                    });
                }
                return element;
            }));
        // pass result to callbacks in onErrorList
        task.onErrorList.forEach(function (onError) {
            onError.apply(null, JSON.parse(task.result));
        });
    };
    // init timerTimeout
    task.timerTimeout = local.onTimeout(
        task.onDone,
        options.timeout || local.timeoutDefault,
        'taskCreate ' + options.key
    );
    task.onTask = onTask;
    // run onTask
    task.onTask(task.onDone);
    return task;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.taskCreateCached"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>taskCreateCached (options, onTask, onError)](#apidoc.element.n_.context.utility2_moduleExports.taskCreateCached)
- description and source-code
```javascript
taskCreateCached = function (options, onTask, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. if cache-hit, then call onError with cacheValue
 * 2. run onTask in background
 * 3. save onTask's result to cache
 * 4. if cache-miss, then call onError with onTask's result
 */
</span>    local.onNext(options, function (error, data) {
        switch (options.modeNext) {
        //  1. if cache-hit, then call onError with cacheValue
        case 1:
            // read cacheValue from memory-cache
            local.cacheDict[options.cacheDict] = local.cacheDict[options.cacheDict] ||
                {};
            options.cacheValue = local.cacheDict[options.cacheDict][options.key];
            if (options.cacheValue) {
                // call onError with cacheValue
                options.modeCacheHit = true;
                onError(null, JSON.parse(options.cacheValue));
                if (!options.modeCacheUpdate) {
                    break;
                }
            }
            // run background-task with lower priority for cache-hit
            setTimeout(options.onNext, options.modeCacheHit && options.cacheTtl);
            break;
        // 2. run onTask in background
        case 2:
            local.taskCreate(options, onTask, options.onNext);
            break;
        default:
            // 3. save onTask's result to cache
            // JSON.stringify data to prevent side-effects on cache
            options.cacheValue = JSON.stringify(data);
            if (!error && options.cacheValue) {
                local.cacheDict[options.cacheDict][options.key] = options.cacheValue;
            }
            // 4. if cache-miss, then call onError with onTask's result
            if (!options.modeCacheHit) {
                onError(error, options.cacheValue && JSON.parse(options.cacheValue));
            }
            (options.onCacheWrite || local.nop)();
            break;
        }
    });
    options.modeNext = 0;
    options.onNext();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.templateRender"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>templateRender (template, dict)](#apidoc.element.n_.context.utility2_moduleExports.templateRender)
- description and source-code
```javascript
templateRender = function (template, dict) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the template with the given dict
 */
</span>    var argList, getValue, match, renderPartial, rgx, value;
    dict = dict || {};
    getValue = function (key) {
        argList = key.split(' ');
        value = dict;
        // iteratively lookup nested values in the dict
        argList[0].split('.').forEach(function (key) {
            value = value && value[key];
        });
        return value;
    };
    renderPartial = function (match0, helper, key, partial) {
        switch (helper) {
        case 'each':
            value = getValue(key);
            return Array.isArray(value)
                ? value.map(function (dict) {
                    // recurse with partial
                    return local.templateRender(partial, dict);
                }).join('')
                : '';
        case 'if':
            partial = partial.split('{{#unless ' + key + '}}');
            partial = getValue(key)
                ? partial[0]
                // handle 'unless' case
                : partial.slice(1).join('{{#unless ' + key + '}}');
            // recurse with partial
            return local.templateRender(partial, dict);
        case 'unless':
            return getValue(key)
                ? ''
                // recurse with partial
                : local.templateRender(partial, dict);
        default:
            // recurse with partial
            return match0[0] + local.templateRender(match0.slice(1), dict);
        }
    };
    // render partials
    rgx = (/\{\{#(\w+) ([^}]+?)\}\}/g);
    template = template || '';
    for (match = rgx.exec(template); match; match = rgx.exec(template)) {
        rgx.lastIndex += 1 - match[0].length;
        template = template.replace(
            new RegExp('\\{\\{#(' + match[1] + ') (' + match[2] +
                ')\\}\\}([\\S\\s]*?)\\{\\{/' + match[1] + ' ' + match[2] +
                '\\}\\}'),
            renderPartial
        );
    }
    // search for keys in the template
    return template.replace((/\{\{[^}]+?\}\}/g), function (match0) {
        getValue(match0.slice(2, -2));
        if (value === undefined) {
            return match0;
        }
        argList.slice(1).forEach(function (arg) {
            switch (arg) {
            case 'alphanumeric':
                value = value.replace((/\W/g), '_');
                break;
            case 'decodeURIComponent':
                value = decodeURIComponent(value);
                break;
            case 'encodeURIComponent':
                value = encodeURIComponent(value);
                break;
            case 'htmlSafe':
                value = value.replace((/["&'<>]/g), function (match0) {
                    return '&#x' + match0.charCodeAt(0).toString(16) + ';';
                });
                break;
            case 'jsonStringify':
                value = JSON.stringify(value);
                break;
            case 'jsonStringify4':
                value = JSON.stringify(value, null, 4);
                break;
            case 'markdownCodeSafe':
                value = value.replace((/'/g), '\'');
                break;
            default:
                value = value[arg]();
                break;
            }
        });
        return String(value);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.templateRenderJslintLite"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>templateRenderJslintLite (template, options)](#apidoc.element.n_.context.utility2_moduleExports.templateRenderJslintLite)
- description and source-code
```javascript
templateRenderJslintLite = function (template, options) {
<span class="apidocCodeCommentSpan">/*
 * this function will render the jslint-lite template with the given options.packageJson
 */
</span>    options.packageJson = options.packageJson ||
        JSON.parse(local.fs.readFileSync('package.json', 'utf8'));
    local.objectSetDefault(options.packageJson, {
        nameAlias: options.packageJson.name.replace((/\W/g), '_'),
        repository: { url: 'https://github.com/kaizhu256/node-' +
            options.packageJson.name + '.git' }
    }, 2);
    options.githubRepo = options.packageJson.repository.url.split('/').slice(-2);
    options.githubRepo[1] = options.githubRepo[1].replace((/\.git$/), '');
    template = template.replace(
        (/https:\/\/kaizhu256\.github\.io\/node-jslint-lite/g),
        'https://' +  options.githubRepo[0] + '.github.io/' +  options.githubRepo[1]
    );
    template = template.replace(
        (/kaizhu256\/node-jslint-lite/g),
        options.githubRepo.join('/')
    );
    template = template.replace(
        (/kaizhu256_2Fnode-jslint-lite/g),
        options.githubRepo.join('_2F')
    );
    template = template.replace(
        (/node-jslint-lite/g),
        options.githubRepo[1]
    );
    template = template.replace((/^#!/), '//');
    template = template.replace((/jslint-lite/g), options.packageJson.name);
    template = template.replace(
        '/* istanbul instrument in package jslint */',
        '/* istanbul instrument in package ' + options.packageJson.nameAlias + ' */'
    );
    template = template.replace(
        (/\b(assets\.|lib\.|local\.|utility2_)jslint\b/g),
        '$1' + options.packageJson.nameAlias
    );
    template = template.replace(
        (/\bh1-jslint\b/g),
        'h1-' + options.packageJson.nameAlias.replace((/_/g), '-')
    );
    template = template.replace(
        'assets.{{env.npm_package_nameAlias}}',
        'assets.' + options.packageJson.nameAlias
    );
    return template;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.testMock"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testMock (mockList, onTestCase, onError)](#apidoc.element.n_.context.utility2_moduleExports.testMock)
- description and source-code
```javascript
testMock = function (mockList, onTestCase, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will mock the objects in mockList while running the onTestCase
 */
</span>    var onError2;
    onError2 = function (error) {
        // restore mock[0] from mock[2]
        mockList.reverse().forEach(function (mock) {
            local.objectSetOverride(mock[0], mock[2]);
        });
        onError(error);
    };
    // try to call onError with mock-objects
    local.tryCatchOnError(function () {
        // mock-objects
        mockList.forEach(function (mock) {
            mock[2] = {};
            // backup mock[0] into mock[2]
            Object.keys(mock[1]).forEach(function (key) {
                mock[2][key] = mock[0][key];
            });
            // override mock[0] with mock[1]
            local.objectSetOverride(mock[0], mock[1]);
        });
        // run onTestCase
        onTestCase(onError2);
    }, onError2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.testReportCreate"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testReportCreate (testReport)](#apidoc.element.n_.context.utility2_moduleExports.testReportCreate)
- description and source-code
```javascript
testReportCreate = function (testReport) {
<span class="apidocCodeCommentSpan">/*
 * this function will create test-report artifacts
 */
</span>    // print test-report summary
    console.error('\n' + new Array(56).join('-') + '\n' + testReport.testPlatformList
        .filter(function (testPlatform) {
            // if testPlatform has no tests, then filter it out
            return testPlatform.testCaseList.length;
        })
        .map(function (testPlatform) {
            return '| test-report - ' + testPlatform.name + '\n|' +
                ('        ' + testPlatform.timeElapsed + ' ms     ')
                .slice(-16) +
                ('        ' + testPlatform.testsFailed + ' failed ')
                .slice(-16) +
                ('        ' + testPlatform.testsPassed + ' passed ')
                .slice(-16) + '     |\n' + new Array(56).join('-');
        })
        .join('\n') + '\n');
    // create test-report.html
    local.fs.writeFileSync(
        local.env.npm_config_dir_build + '/test-report.html',
        local.testReportMerge(testReport, {})
    );
    // create build.badge.svg
    local.fs.writeFileSync(local.env.npm_config_dir_build +
        '/build.badge.svg', local.assetsDict['/assets.buildBadge.template.svg']
        // edit branch name
        .replace((/0000-00-00 00:00:00/g),
            new Date().toISOString().slice(0, 19).replace('T', ' '))
        // edit branch name
        .replace((/- master -/g), '| ' + local.env.CI_BRANCH + ' |')
        // edit commit id
        .replace(
            (/aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa/g),
            local.env.CI_COMMIT_ID
        ));
    // create test-report.badge.svg
    local.fs.writeFileSync(
        local.env.npm_config_dir_build + '/test-report.badge.svg',
        local.assetsDict['/assets.testReportBadge.template.svg']
            // edit number of tests failed
            .replace((/999/g), testReport.testsFailed)
            // edit badge color
            .replace(
                (/d00/g),
                // coverage-hack - cover both fail and pass cases
                '0d00'.slice(!!testReport.testsFailed).slice(0, 3)
            )
    );
    console.error('created test-report file://' + local.env.npm_config_dir_build +
        '/test-report.html\n');
    // if any test failed, then exit with non-zero exit-code
    console.error('\n' + local.env.MODE_BUILD +
        ' - ' + testReport.testsFailed + ' failed tests\n');
    // exit with number of tests failed
    local.exit(testReport.testsFailed);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.testReportMerge"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testReportMerge (testReport1, testReport2)](#apidoc.element.n_.context.utility2_moduleExports.testReportMerge)
- description and source-code
```javascript
testReportMerge = function (testReport1, testReport2) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. merge testReport2 into testReport1
 * 2. return testReport1 in html-format
 */
</span>    var errorStackList, testCaseNumber, testReport;
    // 1. merge testReport2 into testReport1
    [testReport1, testReport2].forEach(function (testReport, ii) {
        ii += 1;
        local.objectSetDefault(testReport, {
            date: new Date().toISOString(),
            errorStackList: [],
            testPlatformList: [],
            timeElapsed: 0
        }, 8);
        // security - handle malformed testReport
        local.assert(
            testReport && typeof testReport === 'object',
            ii + ' invalid testReport ' + typeof testReport
        );
        // validate timeElapsed
        local.assert(
            typeof testReport.timeElapsed === 'number',
            ii + ' invalid testReport.timeElapsed ' + typeof testReport.timeElapsed
        );
        // security - handle malformed testReport.testPlatformList
        testReport.testPlatformList.forEach(function (testPlatform) {
            local.objectSetDefault(testPlatform, {
                name: 'undefined',
                testCaseList: [],
                timeElapsed: 0
            }, 8);
            local.assert(
                typeof testPlatform.name === 'string',
                ii + ' invalid testPlatform.name ' + typeof testPlatform.name
            );
            // insert $MODE_BUILD into testPlatform.name
            if (local.env.MODE_BUILD) {
                testPlatform.name = testPlatform.name.replace(
                    (/^(browser|node)\b/),
                    local.env.MODE_BUILD + ' - $1'
                );
            }
            // validate timeElapsed
            local.assert(
                typeof testPlatform.timeElapsed === 'number',
                ii + ' invalid testPlatform.timeElapsed ' +
                    typeof testPlatform.timeElapsed
            );
            // security - handle malformed testPlatform.testCaseList
            testPlatform.testCaseList.forEach(function (testCase) {
                local.objectSetDefault(testCase, {
                    errorStack: '',
                    name: 'undefined',
                    timeElapsed: 0
                }, 8);
                local.assert(
                    typeof testCase.errorStack === 'string',
                    ii + ' invalid testCase.errorStack ' + typeof testCase.errorStack
                );
                local.assert(
                    typeof testCase.name === 'string',
                    ii + ' invalid testCase.name ' + typeof testCase.name
                );
                // validate timeElapsed
                local.assert(
                    typeof testCase.timeElapsed === 'number',
                    ii + ' invalid testCase.timeElapsed ' + typeof testCase.timeElapsed
                );
            });
        });
    });
    // merge testReport2.testPlatformList into testReport1.testPlatformList
    testReport2.testPlatformList.forEach(function (testPlatform2) {
        // add testPlatform2 to testReport1.testPlatformList
        testReport1.testPlatformList.push(testPlatform2);
    });
    // update testReport1.timeElapsed
    testReport1.timeElapsed += testReport2.timeElapsed;
    testReport = testReport1;
    testReport.testsFailed = 0;
    testReport.testsPassed = 0;
    testReport.testsPending = 0;
    testReport.testPlatformList.forEach(function (testPlatform) {
        testPlatform.testsFailed = 0;
        testPlatform.testsPassed = 0;
        testPlatform.testsPending = 0;
        testPlatform.testCaseList.forEach(function (testCase) {
            switch (testCase.status) {
            // update failed tests
            case 'failed':
                testPlatform.testsFailed += 1;
                testReport.testsFailed += 1;
                break;
            // update passed tests
            case 'passed':
                testPlatform.testsPassed += 1;
                testReport.testsPassed += 1;
                break;
            // update pending tests ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.testRunDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunDefault (options)](#apidoc.element.n_.context.utility2_moduleExports.testRunDefault)
- description and source-code
```javascript
testRunDefault = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will run all tests in testPlatform.testCaseList
 */
</span>    var exit, testPlatform, testReport, testReportDiv1, timerInterval;
    // init modeTest
    local.modeTest = local.modeTest || local.env.npm_config_mode_test;
    if (!(local.modeTest || options.modeTest)) {
        return;
    }
    if (!options.testRunBeforeDone) {
        options.testRunBeforeTimer = options.testRunBeforeTimer ||
            setTimeout(function () {
                local._testRunBefore();
                local.onReadyAfter(function () {
                    options.testRunBeforeDone = true;
                    local.testRunDefault(options);
                });
            });
        return;
    }
    // reset _testRunBefore
    options.testRunBeforeDone = options.testRunBeforeTimer = null;
    // visual notification - testRun
    local.ajaxProgressUpdate();
    switch (local.modeJs) {
    case 'node':
        // mock proces.exit
        exit = process.exit;
        process.exit = local.nop;
        break;
    }
    // init modeTestCase
    local.modeTestCase = local.modeTestCase || local.env.npm_config_mode_test_case;
    // init testReport
    testReport = local.testReport;
    // init testReport timer
    local.timeElapsedStart(testReport);
    // init testPlatform
    testPlatform = local.testReport.testPlatformList[0];
    // init testPlatform timer
    local.timeElapsedStart(testPlatform);
    // reset testPlatform.testCaseList
    testPlatform.testCaseList.length = 0;
    // add tests into testPlatform.testCaseList
    Object.keys(options).forEach(function (key) {
        // add testCase options[key] to testPlatform.testCaseList
        if ((local.modeTestCase && local.modeTestCase.split(',').indexOf(key) >= 0) ||
                (!local.modeTestCase && key.indexOf('testCase_') === 0)) {
            testPlatform.testCaseList.push({
                name: key,
                status: 'pending',
                onTestCase: options[key]
            });
        }
    });
    // visual notification - update test-progress until done
    // init testReportDiv1 element
    if (local.modeJs === 'browser') {
        testReportDiv1 = document.querySelector('#testReportDiv1');
    }
    testReportDiv1 = testReportDiv1 || { style: {} };
    testReportDiv1.style.display = 'block';
    testReportDiv1.innerHTML = local.testReportMerge(testReport, {});
    // update test-report status every 1000 ms until done
    timerInterval = setInterval(function () {
        // update testReportDiv1 in browser
        testReportDiv1.innerHTML = local.testReportMerge(testReport, {});
        if (testReport.testsPending === 0) {
            // cleanup timerInterval
            clearInterval(timerInterval);
        }
    }, 1000);
    // shallow-copy testPlatform.testCaseList to prevent side-effects
    // from in-place sort from testReportMerge
    local.onParallelList({
        list: testPlatform.testCaseList.slice()
    }, function (testCase, onParallel) {
        var onError, timerTimeout;
        onError = function (error) {
            // cleanup timerTimeout
            clearTimeout(timerTimeout);
            // if testCase already done, then fail testCase with error for ending again
            if (testCase.done) {
                error = error || new Error('callback in testCase ' +
                    testCase.name + ' called multiple times');
            }
            // if error occurred, then fail testCase
            if (error) {
                testCase.status = 'failed';
                console.error('\ntestCase ' + testCase.name + ' failed\n' +
                    error.message + '\n' + error.stack);
                testCase.errorStack = testCase.errorStack ||
                    error.message + '\n' + error.stack;
                // validate errorStack is non-empty
                local.assert(
                    testCase.errorStack,
                    'invalid errorStack ' + testCase.errorStack
                );
            }
            // if already done, then do nothing
            if (testCase.done) { ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.testRunServer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>testRunServer (options)](#apidoc.element.n_.context.utility2_moduleExports.testRunServer)
- description and source-code
```javascript
testRunServer = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will
 * 1. create server from local._middleware
 * 2. start server on local.env.PORT
 * 3. run tests
 */
</span>    if (local.global.utility2_serverHttp1) {
        return;
    }
    local.onReadyBefore.counter += 1;
    local._middleware = local._middleware || local.middlewareGroupCreate([
        local.middlewareInit,
        local.middlewareForwardProxy,
        local.middlewareAssetsCached,
        local._middlewareJsonpStateInit
    ]);
    // 1. create server from local._middleware
    local.serverLocalRequestHandler = function (request, response) {
        local._middleware(request, response, function (error) {
            local._middlewareError(error, request, response);
        });
    };
    local.global.utility2_serverHttp1 = local.http.createServer(
        local.serverLocalRequestHandler
    );
    // 2. start server on local.env.PORT
    console.error('server listening on http-port ' + local.env.PORT);
    local.onReadyBefore.counter += 1;
    local.global.utility2_serverHttp1.listen(local.env.PORT, local.onReadyBefore);
    // 3. run tests
    local.testRunDefault(options);
    local.onReadyBefore();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.timeElapsedPoll"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeElapsedPoll (options)](#apidoc.element.n_.context.utility2_moduleExports.timeElapsedPoll)
- description and source-code
```javascript
timeElapsedPoll = function (options) {
<span class="apidocCodeCommentSpan">/*
 * this function will poll options.timeElapsed
 */
</span>    options = local.timeElapsedStart(options);
    options.timeElapsed = Date.now() - options.timeStart;
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.timeElapsedStart"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>timeElapsedStart (options, timeStart)](#apidoc.element.n_.context.utility2_moduleExports.timeElapsedStart)
- description and source-code
```javascript
timeElapsedStart = function (options, timeStart) {
<span class="apidocCodeCommentSpan">/*
 * this function will start options.timeElapsed
 */
</span>    options = options || {};
    options.timeStart = timeStart || options.timeStart || Date.now();
    return options;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.tryCatchOnError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>tryCatchOnError (fnc, onError)](#apidoc.element.n_.context.utility2_moduleExports.tryCatchOnError)
- description and source-code
```javascript
tryCatchOnError = function (fnc, onError) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to run the fnc in a try-catch block,
 * else call onError with the errorCaught
 */
</span>    // validate onError
    local.assert(typeof onError === 'function', typeof onError);
    try {
        // reset errorCaught
        local._debugTryCatchErrorCaught = null;
        return fnc();
    } catch (errorCaught) {
        // debug errorCaught
        local._debugTryCatchErrorCaught = errorCaught;
        return onError(errorCaught);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.tryCatchReadFile"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>tryCatchReadFile (file, options)](#apidoc.element.n_.context.utility2_moduleExports.tryCatchReadFile)
- description and source-code
```javascript
tryCatchReadFile = function (file, options) {
<span class="apidocCodeCommentSpan">/*
 * this function will try to read the file or return an empty string
 */
</span>    var data;
    data = '';
    try {
        data = local.fs.readFileSync(file, options);
    } catch (ignore) {
    }
    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.uglify"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>uglify (code, file)](#apidoc.element.n_.context.utility2_moduleExports.uglify)
- description and source-code
```javascript
uglify = function (code, file) {
<span class="apidocCodeCommentSpan">/*
 * this function will uglify the js-code
 */
</span>    var ast;
    // uglify css
    if ((file || '').slice(-4) === '.css') {
        return code
            // remove comment /**/
            .replace((/\/\*[\S\s]*?\*\//g), '')
            // remove comment //
            .replace((/\/\/.*/g), '')
            // remove whitespace
            .replace((/\t/g), ' ')
            .replace((/ {2,}/g), ' ')
            .replace((/ *?([\n,:;{}]) */g), '$1')
            .replace((/\n\n+/g), '\n')
            .trim();
    }
    // parse code and get the initial AST
    ast = local.parse(code
        .trim()
        // comment shebang
        .replace((/^#!/), '//'));
    // get a new AST with mangled names
    ast = local.ast_mangle(ast);
    // get an AST with compression optimizations
    ast = local.ast_squeeze(ast);
    // compressed code here
    return local.split_lines(local.gen_code(ast, { ascii_only: true }), 79);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.urlParse"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>urlParse (url)](#apidoc.element.n_.context.utility2_moduleExports.urlParse)
- description and source-code
```javascript
urlParse = function (url) {
<span class="apidocCodeCommentSpan">/*
 * https://developer.mozilla.org/en-US/docs/Web/API/URL
 * this function will parse the url according to the above spec, plus a query param
 */
</span>    var urlParsed;
    urlParsed = {};
    // try to parse the url
    local.tryCatchOnError(function () {
        // resolve host-less url
        switch (local.modeJs) {
        case 'browser':
            local.serverLocalHost = local.serverLocalHost ||
                location.protocol + '//' + location.host;
            // resolve absolute path
            if (url[0] === '/') {
                url = local.serverLocalHost + url;
            // resolve relative path
            } else if (!(/^\w+?:\/\//).test(url)) {
                url = local.serverLocalHost +
                    location.pathname.replace((/\/[^\/]*?$/), '') + '/' + url;
            }
            urlParsed = new local.global.URL(url);
            urlParsed.path = '/' + urlParsed.href
                .split('/')
                .slice(3)
                .join('/')
                .split('#')[0];
            break;
        case 'node':
            local.env.PORT = local.env.PORT || '8081';
            local.serverLocalHost = local.serverLocalHost ||
                ('http://127.0.0.1:' + local.env.PORT);
            // resolve absolute path
            if (url[0] === '/') {
                url = local.serverLocalHost + url;
            // resolve relative path
            } else if (!(/^\w+?:\/\//).test(url)) {
                url = local.serverLocalHost + '/' + url;
            }
            urlParsed = local.url.parse(url);
            break;
        }
        // init query
        urlParsed.query = {};
        urlParsed.search.slice(1).replace((/[^&]+/g), function (item) {
            item = item.split('=');
            item[0] = decodeURIComponent(item[0]);
            item[1] = decodeURIComponent(item.slice(1).join('='));
            // parse repeating query-param as an array
            if (urlParsed.query[item[0]]) {
                if (!Array.isArray(urlParsed.query[item[0]])) {
                    urlParsed.query[item[0]] = [urlParsed.query[item[0]]];
                }
                urlParsed.query[item[0]].push(item[1]);
            } else {
                urlParsed.query[item[0]] = item[1];
            }
        });
    }, local.nop);
    // https://developer.mozilla.org/en/docs/Web/API/URL#Properties
    return {
        hash: urlParsed.hash || '',
        host: urlParsed.host || '',
        hostname: urlParsed.hostname || '',
        href: urlParsed.href || '',
        path: urlParsed.path || '',
        pathname: urlParsed.pathname || '',
        port: urlParsed.port || '',
        protocol: urlParsed.protocol || '',
        query: urlParsed.query || {},
        search: urlParsed.search || ''
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.uuid4Create"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.</span>uuid4Create ()](#apidoc.element.n_.context.utility2_moduleExports.uuid4Create)
- description and source-code
```javascript
uuid4Create = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will create a random uuid,
 * with format 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'
 */
</span>    // code derived from http://jsperf.com/uuid4
    var id, ii;
    id = '';
    for (ii = 0; ii < 32; ii += 1) {
        switch (ii) {
        case 8:
        case 20:
            id += '-';
            // coerce to finite integer
            id += (Math.random() * 16 | 0).toString(16);
            break;
        case 12:
            id += '-';
            id += '4';
            break;
        case 16:
            id += '-';
            id += (Math.random() * 4 | 8).toString(16);
            break;
        default:
            // coerce to finite integer
            id += (Math.random() * 16 | 0).toString(16);
        }
    }
    return id;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2_moduleExports.FormData.prototype"></a>[module n_.context.utility2_moduleExports.FormData.prototype](#apidoc.module.n_.context.utility2_moduleExports.FormData.prototype)

#### <a name="apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.append"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.FormData.prototype.</span>append (name, value, filename)](#apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.append)
- description and source-code
```javascript
append = function (name, value, filename) {
<span class="apidocCodeCommentSpan">/*
 * https://xhr.spec.whatwg.org/#dom-formdata-append
 * The append(name, value, filename) method, when invoked, must run these steps:
 * 1. If the filename argument is given, set value to a new File object
 *    whose contents are value and name is filename.
 * 2. Append a new entry whose name is name, and value is value,
 *    to context object's list of entries.
 */
</span>    if (filename) {
        // bug-workaround - chromium cannot assign name to Blob instance
        local.tryCatchOnError(function () {
            value.name = filename;
        }, local.nop);
    }
    this.entryList.push({ name: name, value: value });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.read"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_moduleExports.FormData.prototype.</span>read (onError)](#apidoc.element.n_.context.utility2_moduleExports.FormData.prototype.read)
- description and source-code
```javascript
read = function (onError) {
<span class="apidocCodeCommentSpan">/*
 * https://tools.ietf.org/html/rfc7578
 * this function will read from formData as a buffer, e.g.
 * --Boundary\r\n
 * Content-Disposition: form-data; name="key"\r\n
 * \r\n
 * value\r\n
 * --Boundary\r\n
 * Content-Disposition: form-data; name="input1"; filename="file1.png"\r\n
 * Content-Type: image/jpeg\r\n
 * \r\n
 * <data1>\r\n
 * --Boundary\r\n
 * Content-Disposition: form-data; name="input2"; filename="file2.png"\r\n
 * Content-Type: image/jpeg\r\n
 * \r\n
 * <data2>\r\n
 * --Boundary--\r\n
 */
</span>    var boundary, result;
    // handle null-case
    if (this.entryList.length === 0) {
        onError(null, local.bufferCreate());
        return;
    }
    // init boundary
    boundary = '--' + Date.now().toString(16) + Math.random().toString(16);
    // init result
    result = [];
    local.onParallelList({
        list: this.entryList
    }, function (options, onParallel) {
        var value;
        value = options.element.value;
        if (!(value instanceof local.Blob)) {
            result[options.ii] = [boundary +
                '\r\nContent-Disposition: form-data; name="' + options.element.name +
                '"\r\n\r\n', value, '\r\n'];
            onParallel.counter += 1;
            onParallel();
            return;
        }
        // read from blob in parallel
        onParallel.counter += 1;
        local.blobRead(value, 'binary', function (error, data) {
            result[options.ii] = !error && [boundary +
                '\r\nContent-Disposition: form-data; name="' + options.element.name +
                '"' +
                // read param filename
                (value && value.name
                    ? '; filename="' + value.name + '"'
                    : '') +
                '\r\n' +
                // read param Content-Type
                (value && value.type
                    ? 'Content-Type: ' + value.type + '\r\n'
                    : '') +
                '\r\n', data, '\r\n'];
            onParallel(error);
        });
    }, function (error) {
        // add closing boundary
        result.push([boundary + '--\r\n']);
        // concatenate result
        onError(
            error,
            // flatten result
            !error && local.bufferConcat(Array.prototype.concat.apply([], result))
        );
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.context.utility2_serverRepl1"></a>[module n_.context.utility2_serverRepl1](#apidoc.module.n_.context.utility2_serverRepl1)

#### <a name="apidoc.element.n_.context.utility2_serverRepl1._ttyWrite"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>_ttyWrite (d, key)](#apidoc.element.n_.context.utility2_serverRepl1._ttyWrite)
- description and source-code
```javascript
(d, key) => {
  key = key || {};
  if (!self.editorMode || !self.terminal) {
    ttyWrite(d, key);
    return;
  }

  // editor mode
  if (key.ctrl && !key.shift) {
    switch (key.name) {
      case 'd': // End editor mode
        self.turnOffEditorMode();
        sawCtrlD = true;
        ttyWrite(d, { name: 'return' });
        break;
      case 'n': // Override next history item
      case 'p': // Override previous history item
        break;
      default:
        ttyWrite(d, key);
    }
  } else {
    switch (key.name) {
      case 'up':   // Override previous history item
      case 'down': // Override next history item
        break;
      case 'tab':
        // prevent double tab behavior
        self._previousKey = null;
        ttyWrite(d, key);
        break;
      default:
        ttyWrite(d, key);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.completer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>completer (text, cb)](#apidoc.element.n_.context.utility2_serverRepl1.completer)
- description and source-code
```javascript
function completer(text, cb) {
  complete.call(self, text, self.editorMode
    ? self.completeOnEditorMode(cb) : cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.eval"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>eval (script, context, file, onError)](#apidoc.element.n_.context.utility2_serverRepl1.eval)
- description and source-code
```javascript
eval = function (script, context, file, onError) {
    var match, onError2;
    match = (/^(\S+)(.*?)\n/).exec(script);
    onError2 = function (error, data) {
        // debug error
        global.utility2_debugReplError = error || global.utility2_debugReplError;
        onError(error, data);
    };
    switch (match && match[1]) {
    // syntax sugar to run async shell command
    case '$':
        switch (match[2]) {
        // syntax sugar to run git diff
        case ' git diff':
            match[2] = ' git diff --color | cat';
            break;
        // syntax sugar to run git log
        case ' git log':
            match[2] = ' git log -n 4 | cat';
            break;
        }
        // run async shell command
        require('child_process').spawn(
            '/bin/sh',
            ['-c', match[2]],
            { stdio: ['ignore', 1, 2] }
        )
            // on shell exit, print return prompt
            .on('exit', function (exitCode) {
                console.error('exit-code ' + exitCode);
                self.evalDefault(
                    '\n',
                    context,
                    file,
                    onError2
                );
            });
        script = '\n';
        break;
    // syntax sugar to grep current dir
    case 'grep':
        // run async shell command
        require('child_process').spawn(
            '/bin/sh',
            ['-c', 'find . -type f | grep -v ' +
<span class="apidocCodeCommentSpan">/* jslint-ignore-begin */
</span>'"\
/\\.\\|.*\\(\\b\\|_\\)\\(\\.\\d\\|\
archive\\|artifact\\|\
bower_component\\|build\\|\
coverage\\|\
doc\\|\
external\\|\
fixture\\|\
git_module\\|\
jquery\\|\
log\\|\
min\\|mock\\|\
node_module\\|\
rollup\\|\
swp\\|\
tmp\\|\
vendor\\)\\(\\b\\|[_s]\\)\
" ' +
/* jslint-ignore-end */
                '| tr "\\n" "\\000" | xargs -0 grep -in "' +
                match[2].trim() + '"'],
            { stdio: ['ignore', 1, 2] }
        )
            // on shell exit, print return prompt
            .on('exit', function (exitCode) {
                console.error('exit-code ' + exitCode);
                self.evalDefault(
                    '\n',
                    context,
                    file,
                    onError2
                );
            });
        script = '\n';
        break;
    // syntax sugar to list object's keys, sorted by item-type
    case 'keys':
        script = 'console.error(Object.keys(' + match[2] +
            ').map(function (key) {' +
            'return typeof ' + match[2] + '[key] + " " + key + "\\n";' +
            '}).sort().join("") + Object.keys(' + match[2] + ').length)\n';
        break;
    // syntax sugar to print stringified arg
    case 'print':
        script = 'console.error(String(' + match[2] + '))\n';
        break;
    }
    // eval the script
    self.evalDefault(script, context, file, onError2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.evalDefault"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>evalDefault ()](#apidoc.element.n_.context.utility2_serverRepl1.evalDefault)
- description and source-code
```javascript
function runBound() {
  return bound(this, self, cb, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.nop"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>nop ()](#apidoc.element.n_.context.utility2_serverRepl1.nop)
- description and source-code
```javascript
nop = function () {
<span class="apidocCodeCommentSpan">/*
 * this function will do nothing
 */
</span>    return;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.onError"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>onError (error)](#apidoc.element.n_.context.utility2_serverRepl1.onError)
- description and source-code
```javascript
onError = function (error) {
<span class="apidocCodeCommentSpan">/*
 * this function will debug any repl-error
 */
</span>    // debug error
    global.utility2_debugReplError = error;
    console.error(error.stack);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.context.utility2_serverRepl1.writer"></a>[function <span class="apidocSignatureSpan">n_.context.utility2_serverRepl1.</span>writer (obj, showHidden, depth)](#apidoc.element.n_.context.utility2_serverRepl1.writer)
- description and source-code
```javascript
writer = function (obj, showHidden, depth) {
  return util.inspect(obj, showHidden, depth, true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.inputStream"></a>[module n_.inputStream](#apidoc.module.n_.inputStream)

#### <a name="apidoc.element.n_.inputStream.read"></a>[function <span class="apidocSignatureSpan">n_.inputStream.</span>read (n)](#apidoc.element.n_.inputStream.read)
- description and source-code
```javascript
read = function (n) {
  debug('read', n);
  n = parseInt(n, 10);
  var state = this._readableState;
  var nOrig = n;

  if (n !== 0)
    state.emittedReadable = false;

  // if we're doing read(0) to trigger a readable event, but we
  // already have a bunch of data in the buffer, then just trigger
  // the 'readable' event and move on.
  if (n === 0 &&
      state.needReadable &&
      (state.length >= state.highWaterMark || state.ended)) {
    debug('read: emitReadable', state.length, state.ended);
    if (state.length === 0 && state.ended)
      endReadable(this);
    else
      emitReadable(this);
    return null;
  }

  n = howMuchToRead(n, state);

  // if we've ended, and we're now clear, then finish it up.
  if (n === 0 && state.ended) {
    if (state.length === 0)
      endReadable(this);
    return null;
  }

  // All the actual chunk generation logic needs to be
  // *below* the call to _read.  The reason is that in certain
  // synthetic stream cases, such as passthrough streams, _read
  // may be a completely synchronous operation which may change
  // the state of the read buffer, providing enough data when
  // before there was *not* enough.
  //
  // So, the steps are:
  // 1. Figure out what the state of things will be after we do
  // a read from the buffer.
  //
  // 2. If that resulting state will trigger a _read, then call _read.
  // Note that this may be asynchronous, or synchronous.  Yes, it is
  // deeply ugly to write APIs this way, but that still doesn't mean
  // that the Readable class should behave improperly, as streams are
  // designed to be sync/async agnostic.
  // Take note if the _read call is sync or async (ie, if the read call
  // has returned yet), so that we know whether or not it's safe to emit
  // 'readable' etc.
  //
  // 3. Actually pull the requested chunks out of the buffer and return.

  // if we need a readable event, then we need to do some reading.
  var doRead = state.needReadable;
  debug('need readable', doRead);

  // if we currently have less than the highWaterMark, then also read some
  if (state.length === 0 || state.length - n < state.highWaterMark) {
    doRead = true;
    debug('length less than watermark', doRead);
  }

  // however, if we've ended, then there's no point, and if we're already
  // reading, then it's unnecessary.
  if (state.ended || state.reading) {
    doRead = false;
    debug('reading or ended', doRead);
  } else if (doRead) {
    debug('do read');
    state.reading = true;
    state.sync = true;
    // if the length is currently zero, then we *need* a readable event.
    if (state.length === 0)
      state.needReadable = true;
    // call internal read method
    this._read(state.highWaterMark);
    state.sync = false;
    // If _read pushed data synchronously, then 'reading' will be false,
    // and we need to re-evaluate how much data we can return to the user.
    if (!state.reading)
      n = howMuchToRead(nOrig, state);
  }

  var ret;
  if (n > 0)
    ret = fromList(n, state);
  else
    ret = null;

  if (ret === null) {
    state.needReadable = true;
    n = 0;
  } else {
    state.length -= n;
  }

  if (state.length === 0) {
    // If we have nothing in the buffer, then we want to know
    // as soon as we *do* get something into the buffer.
    if (!state.ended)
      state.needReadable = true;

    // If we tried to read() past the EOF, then emit end on the next tick.
    if (nOrig !== n && state.ended)
      endReadable(this);
  }

  if (ret !== null)
    this.emit('data', ret);

  return ret;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.inputStream._events"></a>[module n_.inputStream._events](#apidoc.module.n_.inputStream._events)

#### <a name="apidoc.element.n_.inputStream._events._socketEnd"></a>[function <span class="apidocSignatureSpan">n_.inputStream._events.</span>_socketEnd ()](#apidoc.element.n_.inputStream._events._socketEnd)
- description and source-code
```javascript
function onSocketEnd() {
  // XXX Should not have to do as much crap in this function.
  // ended should already be true, since this is called *after*
  // the EOF errno and onread has eof'ed
  debug('onSocketEnd', this._readableState);
  this._readableState.ended = true;
  if (this._readableState.endEmitted) {
    this.readable = false;
    maybeDestroy(this);
  } else {
    this.once('end', function() {
      this.readable = false;
      maybeDestroy(this);
    });
    this.read(0);
  }

  if (!this.allowHalfOpen) {
    this.write = writeAfterFIN;
    this.destroySoon();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.inputStream._events.data"></a>[function <span class="apidocSignatureSpan">n_.inputStream._events.</span>data (b)](#apidoc.element.n_.inputStream._events.data)
- description and source-code
```javascript
function onData(b) {
  if (stream.listenerCount('keypress') > 0) {
    var r = stream[KEYPRESS_DECODER].write(b);
    if (r) {
      clearTimeout(timeoutId);

      if (iface) {
        iface._sawKeyPress = r.length === 1;
      }

      for (var i = 0; i < r.length; i++) {
        if (r[i] === '\t' && typeof r[i + 1] === 'string' && iface) {
          iface.isCompletionEnabled = false;
        }

        try {
          stream[ESCAPE_DECODER].next(r[i]);
          // Escape letter at the tail position
          if (r[i] === '\x1b' && i + 1 === r.length) {
            timeoutId = setTimeout(escapeCodeTimeout, ESCAPE_CODE_TIMEOUT);
          }
        } catch (err) {
          // if the generator throws (it could happen in the 'keypress'
          // event), we need to restart it.
          stream[ESCAPE_DECODER] = emitKeys(stream);
          stream[ESCAPE_DECODER].next();
          throw err;
        } finally {
          if (iface) {
            iface.isCompletionEnabled = true;
          }
        }
      }
    }
  } else {
    // Nobody's watching anyway
    stream.removeListener('data', onData);
    stream.on('newListener', onNewListener);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.inputStream._events.finish"></a>[function <span class="apidocSignatureSpan">n_.inputStream._events.</span>finish ()](#apidoc.element.n_.inputStream._events.finish)
- description and source-code
```javascript
function onSocketFinish() {
  // If still connecting - defer handling 'finish' until 'connect' will happen
  if (this.connecting) {
    debug('osF: not yet connected');
    return this.once('connect', onSocketFinish);
  }

  debug('onSocketFinish');
  if (!this.readable || this._readableState.ended) {
    debug('oSF: ended, destroy', this._readableState);
    return this.destroy();
  }

  debug('oSF: not ended, call shutdown()');

  // otherwise, just shutdown, or destroy() if not possible
  if (!this._handle || !this._handle.shutdown)
    return this.destroy();

  var req = new ShutdownWrap();
  req.oncomplete = afterShutdown;
  req.handle = this._handle;
  var err = this._handle.shutdown(req);

  if (err)
    return this._destroy(errnoException(err, 'shutdown'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.inputStream._events.pause"></a>[function <span class="apidocSignatureSpan">n_.inputStream._events.</span>pause ()](#apidoc.element.n_.inputStream._events.pause)
- description and source-code
```javascript
() => {
  if (!stdin._handle)
    return;
  stdin._readableState.reading = false;
  stdin._handle.reading = false;
  stdin._handle.readStop();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.inputStream._handle"></a>[module n_.inputStream._handle](#apidoc.module.n_.inputStream._handle)

#### <a name="apidoc.element.n_.inputStream._handle.onread"></a>[function <span class="apidocSignatureSpan">n_.inputStream._handle.</span>onread (nread, buffer)](#apidoc.element.n_.inputStream._handle.onread)
- description and source-code
```javascript
function onread(nread, buffer) {
  var handle = this;
  var self = handle.owner;
  assert(handle === self._handle, 'handle != self._handle');

  self._unrefTimer();

  debug('onread', nread);

  if (nread > 0) {
    debug('got data');

    // read success.
    // In theory (and in practice) calling readStop right now
    // will prevent this from being called again until _read() gets
    // called again.

    // Optimization: emit the original buffer with end points
    var ret = self.push(buffer);

    if (handle.reading && !ret) {
      handle.reading = false;
      debug('readStop');
      var err = handle.readStop();
      if (err)
        self._destroy(errnoException(err, 'read'));
    }
    return;
  }

  // if we didn't get any bytes, that doesn't necessarily mean EOF.
  // wait for the next one.
  if (nread === 0) {
    debug('not any data, keep waiting');
    return;
  }

  // Error, possibly EOF.
  if (nread !== uv.UV_EOF) {
    return self._destroy(errnoException(nread, 'read'));
  }

  debug('EOF');

  // push a null to signal the end of data.
  // Do it before 'maybeDestroy' for correct order of events:
  // 'end' -> 'close'
  self.push(null);

  if (self._readableState.length === 0) {
    self.readable = false;
    maybeDestroy(self);
  }

  // internal end event so that we know that the actual socket
  // is no longer readable, and we can start the shutdown
  // procedure. No need to wait for all the data to be consumed.
  self.emit('_socketEnd');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.inputStream._writableState"></a>[module n_.inputStream._writableState](#apidoc.module.n_.inputStream._writableState)

#### <a name="apidoc.element.n_.inputStream._writableState.onwrite"></a>[function <span class="apidocSignatureSpan">n_.inputStream._writableState.</span>onwrite (er)](#apidoc.element.n_.inputStream._writableState.onwrite)
- description and source-code
```javascript
onwrite = function (er) {
  onwrite(stream, er);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.outputStream"></a>[module n_.outputStream](#apidoc.module.n_.outputStream)

#### <a name="apidoc.element.n_.outputStream._write"></a>[function <span class="apidocSignatureSpan">n_.outputStream.</span>_write (chunk, encoding, callback)](#apidoc.element.n_.outputStream._write)
- description and source-code
```javascript
_write = function (chunk, encoding, callback) {
    process.stdout._writeDefault(chunk, encoding, callback);
    // coverage-hack
    self.nop(self.socket.readable && (function () {
        self.socket.write(chunk, encoding);
    }()));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.outputStream._writeDefault"></a>[function <span class="apidocSignatureSpan">n_.outputStream.</span>_writeDefault (data, encoding, cb)](#apidoc.element.n_.outputStream._writeDefault)
- description and source-code
```javascript
_writeDefault = function (data, encoding, cb) {
  this._writeGeneric(false, data, encoding, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.outputStream.destroy"></a>[function <span class="apidocSignatureSpan">n_.outputStream.</span>destroy (er)](#apidoc.element.n_.outputStream.destroy)
- description and source-code
```javascript
destroy = function (er) {
  er = er || new Error('process.stdout cannot be closed.');
  stdout.emit('error', er);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.outputStream.destroySoon"></a>[function <span class="apidocSignatureSpan">n_.outputStream.</span>destroySoon (er)](#apidoc.element.n_.outputStream.destroySoon)
- description and source-code
```javascript
destroySoon = function (er) {
  er = er || new Error('process.stdout cannot be closed.');
  stdout.emit('error', er);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.outputStream._events"></a>[module n_.outputStream._events](#apidoc.module.n_.outputStream._events)

#### <a name="apidoc.element.n_.outputStream._events._socketEnd"></a>[function <span class="apidocSignatureSpan">n_.outputStream._events.</span>_socketEnd ()](#apidoc.element.n_.outputStream._events._socketEnd)
- description and source-code
```javascript
function onSocketEnd() {
  // XXX Should not have to do as much crap in this function.
  // ended should already be true, since this is called *after*
  // the EOF errno and onread has eof'ed
  debug('onSocketEnd', this._readableState);
  this._readableState.ended = true;
  if (this._readableState.endEmitted) {
    this.readable = false;
    maybeDestroy(this);
  } else {
    this.once('end', function() {
      this.readable = false;
      maybeDestroy(this);
    });
    this.read(0);
  }

  if (!this.allowHalfOpen) {
    this.write = writeAfterFIN;
    this.destroySoon();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.outputStream._events.end"></a>[function <span class="apidocSignatureSpan">n_.outputStream._events.</span>end ()](#apidoc.element.n_.outputStream._events.end)
- description and source-code
```javascript
function g() {
  target.removeListener(type, g);
  if (!fired) {
    fired = true;
    listener.apply(target, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.n_.outputStream._events.finish"></a>[function <span class="apidocSignatureSpan">n_.outputStream._events.</span>finish ()](#apidoc.element.n_.outputStream._events.finish)
- description and source-code
```javascript
function onSocketFinish() {
  // If still connecting - defer handling 'finish' until 'connect' will happen
  if (this.connecting) {
    debug('osF: not yet connected');
    return this.once('connect', onSocketFinish);
  }

  debug('onSocketFinish');
  if (!this.readable || this._readableState.ended) {
    debug('oSF: ended, destroy', this._readableState);
    return this.destroy();
  }

  debug('oSF: not ended, call shutdown()');

  // otherwise, just shutdown, or destroy() if not possible
  if (!this._handle || !this._handle.shutdown)
    return this.destroy();

  var req = new ShutdownWrap();
  req.oncomplete = afterShutdown;
  req.handle = this._handle;
  var err = this._handle.shutdown(req);

  if (err)
    return this._destroy(errnoException(err, 'shutdown'));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.outputStream._handle"></a>[module n_.outputStream._handle](#apidoc.module.n_.outputStream._handle)

#### <a name="apidoc.element.n_.outputStream._handle.onread"></a>[function <span class="apidocSignatureSpan">n_.outputStream._handle.</span>onread (nread, buffer)](#apidoc.element.n_.outputStream._handle.onread)
- description and source-code
```javascript
function onread(nread, buffer) {
  var handle = this;
  var self = handle.owner;
  assert(handle === self._handle, 'handle != self._handle');

  self._unrefTimer();

  debug('onread', nread);

  if (nread > 0) {
    debug('got data');

    // read success.
    // In theory (and in practice) calling readStop right now
    // will prevent this from being called again until _read() gets
    // called again.

    // Optimization: emit the original buffer with end points
    var ret = self.push(buffer);

    if (handle.reading && !ret) {
      handle.reading = false;
      debug('readStop');
      var err = handle.readStop();
      if (err)
        self._destroy(errnoException(err, 'read'));
    }
    return;
  }

  // if we didn't get any bytes, that doesn't necessarily mean EOF.
  // wait for the next one.
  if (nread === 0) {
    debug('not any data, keep waiting');
    return;
  }

  // Error, possibly EOF.
  if (nread !== uv.UV_EOF) {
    return self._destroy(errnoException(nread, 'read'));
  }

  debug('EOF');

  // push a null to signal the end of data.
  // Do it before 'maybeDestroy' for correct order of events:
  // 'end' -> 'close'
  self.push(null);

  if (self._readableState.length === 0) {
    self.readable = false;
    maybeDestroy(self);
  }

  // internal end event so that we know that the actual socket
  // is no longer readable, and we can start the shutdown
  // procedure. No need to wait for all the data to be consumed.
  self.emit('_socketEnd');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.n_.outputStream._writableState"></a>[module n_.outputStream._writableState](#apidoc.module.n_.outputStream._writableState)

#### <a name="apidoc.element.n_.outputStream._writableState.onwrite"></a>[function <span class="apidocSignatureSpan">n_.outputStream._writableState.</span>onwrite (er)](#apidoc.element.n_.outputStream._writableState.onwrite)
- description and source-code
```javascript
onwrite = function (er) {
  onwrite(stream, er);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
