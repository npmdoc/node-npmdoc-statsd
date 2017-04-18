# npmdoc-statsd

#### api documentation for  [statsd (v0.8.0)](https://github.com/etsy/statsd)  [![npm package](https://img.shields.io/npm/v/npmdoc-statsd.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-statsd) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-statsd.svg)](https://travis-ci.org/npmdoc/node-npmdoc-statsd)

#### Network daemon for the collection and aggregation of realtime application metrics

[![NPM](https://nodei.co/npm/statsd.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/statsd)

- [https://npmdoc.github.io/node-npmdoc-statsd/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-statsd/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-statsd/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-statsd/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-statsd/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-statsd/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Etsy",
        "url": "https://codeascraft.com"
    },
    "bin": {
        "statsd": "./bin/statsd"
    },
    "bugs": {
        "url": "https://github.com/etsy/statsd/issues"
    },
    "dependencies": {
        "generic-pool": "2.2.0",
        "hashring": "3.2.0",
        "modern-syslog": "1.1.2",
        "winser": "=0.1.6"
    },
    "description": "Network daemon for the collection and aggregation of realtime application metrics",
    "devDependencies": {
        "nodeunit": "0.9.x",
        "temp": "0.4.x",
        "underscore": "1.4.x"
    },
    "directories": {},
    "dist": {
        "shasum": "92041479e174a214df7147f2fab1348af0839052",
        "tarball": "https://registry.npmjs.org/statsd/-/statsd-0.8.0.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "5d729d95847db0189e2c5571014b54c63d661f31",
    "homepage": "https://github.com/etsy/statsd",
    "keywords": [
        "statsd",
        "etsy",
        "metric",
        "aggregation",
        "realtime"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "kastner"
        },
        {
            "name": "mrtazz"
        },
        {
            "name": "draco2003"
        },
        {
            "name": "pkhzzrd"
        }
    ],
    "name": "statsd",
    "optionalDependencies": {
        "hashring": "3.2.0",
        "modern-syslog": "1.1.2",
        "winser": "=0.1.6"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/etsy/statsd.git"
    },
    "scripts": {
        "install-windows-service": "winser -i",
        "start": "node stats.js config.js",
        "test": "./run_tests.sh",
        "uninstall-windows-service": "winser -r"
    },
    "version": "0.8.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
