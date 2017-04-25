# npmtest-bodybuilder

#### basic test coverage for  [bodybuilder (v2.1.0)](https://github.com/danpaz/bodybuilder#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-bodybuilder.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-bodybuilder) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-bodybuilder.svg)](https://travis-ci.org/npmtest/node-npmtest-bodybuilder)

#### An elasticsearch query body builder.

[![NPM](https://nodei.co/npm/bodybuilder.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/bodybuilder)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-bodybuilder/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-bodybuilder/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-bodybuilder/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-bodybuilder/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-bodybuilder/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-bodybuilder/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-bodybuilder/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-bodybuilder/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-bodybuilder/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-bodybuilder/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-bodybuilder/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-bodybuilder/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-bodybuilder/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-bodybuilder/build/test-report.html](https://npmtest.github.io/node-npmtest-bodybuilder/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-bodybuilder/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-bodybuilder/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-bodybuilder/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-bodybuilder/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-bodybuilder/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Paz-Soldan"
    },
    "bugs": {
        "url": "https://github.com/danpaz/bodybuilder/issues"
    },
    "contributors": [
        {
            "name": "Nicolás Fantone"
        },
        {
            "name": "Nauval Atmaja"
        },
        {
            "name": "Ferron Hanse"
        },
        {
            "name": "Dave Cranwell"
        },
        {
            "name": "Anton Samper Rivaya"
        }
    ],
    "dependencies": {
        "lodash": "4.9.0"
    },
    "description": "An elasticsearch query body builder.",
    "devDependencies": {
        "babel-cli": "6.5.1",
        "babel-core": "6.5.1",
        "babel-plugin-lodash": "2.0.1",
        "babel-preset-es2015": "6.5.0",
        "babel-register": "6.18.0",
        "babel-tape-runner": "2.0.1",
        "documentation": "4.0.0-beta10",
        "eslint": "1.10.2",
        "tap-spec": "4.1.1",
        "tape": "4.6.2",
        "tape-watch": "2.2.4",
        "webpack": "1.12.13"
    },
    "directories": {},
    "dist": {
        "shasum": "45bd98566d13848ba6f50a1eeeb1c10273b216a8",
        "tarball": "https://registry.npmjs.org/bodybuilder/-/bodybuilder-2.1.0.tgz"
    },
    "files": [
        "browser/",
        "lib/",
        "src/",
        "repl.js"
    ],
    "gitHead": "0bf3cc4f3bdb6f8f301c87c9978eb8ef5d9592c0",
    "homepage": "https://github.com/danpaz/bodybuilder#readme",
    "keywords": [
        "elasticsearch",
        "bodybuilder",
        "querying",
        "queries",
        "query",
        "elastic",
        "search",
        "dsl"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "danpaz"
        }
    ],
    "name": "bodybuilder",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/danpaz/bodybuilder.git"
    },
    "scripts": {
        "build": "npm run build:babel && npm run build:umd && npm run build:docs",
        "build:babel": "babel src --out-dir lib",
        "build:docs": "documentation build src/index.js -o docs -f html --name bodybuilder",
        "build:umd": "webpack lib browser/bodybuilder.min.js",
        "check": "npm run lint && npm test",
        "git-commit": "git add docs browser && git commit -m \"Commit built files\"",
        "git-push": "git push origin master && git push origin v$npm_package_version",
        "lint": "eslint src test",
        "postversion": "npm run git-push",
        "preversion": "npm run check && npm run build && npm run git-commit",
        "style": "npm run lint",
        "test": "babel-tape-runner test/* | tap-spec",
        "watch:test": "tape-watch test/* -r babel-register -p tap-spec"
    },
    "version": "2.1.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
