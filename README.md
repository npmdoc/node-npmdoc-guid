# api documentation for  [guid (v0.0.12)](https://github.com/dandean/guid)  [![npm package](https://img.shields.io/npm/v/npmdoc-guid.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-guid) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-guid.svg)](https://travis-ci.org/npmdoc/node-npmdoc-guid)
#### A Guid generator and validator.

[![NPM](https://nodei.co/npm/guid.png?downloads=true)](https://www.npmjs.com/package/guid)

[![apidoc](https://npmdoc.github.io/node-npmdoc-guid/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-guid_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-guid/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-guid/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-guid/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Dean",
        "email": "@dandean",
        "url": "http://dandean.com"
    },
    "bugs": {
        "url": "https://github.com/dandean/guid/issues"
    },
    "contributors": [
        {
            "name": "Tommy Messbauer"
        }
    ],
    "dependencies": {},
    "deprecated": "Please use node-uuid instead. It is much better.",
    "description": "A Guid generator and validator.",
    "devDependencies": {
        "mocha": "~1.14.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9137c52b185f7de12490b9bebcc1660b9025fe0c",
        "tarball": "https://registry.npmjs.org/guid/-/guid-0.0.12.tgz"
    },
    "ender": "./ender.js",
    "homepage": "https://github.com/dandean/guid",
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/dandean/guid/raw/master/LICENSE"
        }
    ],
    "main": "./guid",
    "maintainers": [
        {
            "name": "dandean",
            "email": "me@dandean.com"
        }
    ],
    "name": "guid",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/dandean/guid.git"
    },
    "scripts": {
        "test": "mocha -R spec -u tdd tests/*.js"
    },
    "testling": {
        "browsers": {
            "ie": [
                6,
                7,
                8,
                9,
                10
            ],
            "ff": [
                24,
                25,
                "nightly"
            ],
            "chrome": [
                28,
                29,
                30,
                31,
                "canary"
            ],
            "safari": [
                "5.0.5",
                5.1
            ],
            "android-browser": [
                4.2
            ],
            "opera": [
                17,
                "next"
            ],
            "iphone": [
                6
            ],
            "ipad": [
                6
            ]
        },
        "harness": "mocha-tdd",
        "files": "tests/*.js"
    },
    "version": "0.0.12"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module guid](#apidoc.module.guid)
1.  [function <span class="apidocSignatureSpan">guid.</span>create ()](#apidoc.element.guid.create)
1.  [function <span class="apidocSignatureSpan">guid.</span>isGuid (value)](#apidoc.element.guid.isGuid)
1.  [function <span class="apidocSignatureSpan">guid.</span>raw ()](#apidoc.element.guid.raw)
1.  string <span class="apidocSignatureSpan">guid.</span>EMPTY



# <a name="apidoc.module.guid"></a>[module guid](#apidoc.module.guid)

#### <a name="apidoc.element.guid.create"></a>[function <span class="apidocSignatureSpan">guid.</span>create ()](#apidoc.element.guid.create)
- description and source-code
```javascript
create = function () {
  return new Guid([gen(2), gen(1), gen(1), gen(1), gen(3)].join("-"));
}
```
- example usage
```shell
...
In its simplest form, Guid lets you generate raw GUID formatted strings:

Guid.raw();
// -> '6fdf6ffc-ed77-94fa-407e-a7b86ed9e59d'

Let's generate a new Guid instance.

var guid = Guid.create();

We've now got an object which we can work with programmatically. Lets check the
validity of our Guid using the built-in validator:

Guid.isGuid(guid);
// -> true
...
```

#### <a name="apidoc.element.guid.isGuid"></a>[function <span class="apidocSignatureSpan">guid.</span>isGuid (value)](#apidoc.element.guid.isGuid)
- description and source-code
```javascript
isGuid = function (value) {
  return value && (value instanceof Guid || validator.test(value.toString()));
}
```
- example usage
```shell
...
Let's generate a new Guid instance.

    var guid = Guid.create();

We've now got an object which we can work with programmatically. Lets check the
validity of our Guid using the built-in validator:

    Guid.isGuid(guid);
    // -> true

    Guid.value;
    // -> '6fdf6ffc-ed77-94fa-407e-a7b86ed9e59d'

A handy bit of functionality is that its 'toString' method returns the string
value, so you can do handy things like this:
...
```

#### <a name="apidoc.element.guid.raw"></a>[function <span class="apidocSignatureSpan">guid.</span>raw ()](#apidoc.element.guid.raw)
- description and source-code
```javascript
raw = function () {
  return [gen(2), gen(1), gen(1), gen(1), gen(3)].join("-");
}
```
- example usage
```shell
...

# Guid lets you generate and validate unique identifiers.

[![browser support](https://ci.testling.com/tommydudebreaux/guid.png)](https://ci.testling.com/tommydudebreaux/guid)

In its simplest form, Guid lets you generate raw GUID formatted strings:

    Guid.raw();
    // -> '6fdf6ffc-ed77-94fa-407e-a7b86ed9e59d'

Let's generate a new Guid instance.

    var guid = Guid.create();

We've now got an object which we can work with programmatically. Lets check the
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
