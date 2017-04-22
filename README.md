# npmdoc-next

#### api documentation for  next (v2.1.1)  [![npm package](https://img.shields.io/npm/v/npmdoc-next.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-next) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-next.svg)](https://travis-ci.org/npmdoc/node-npmdoc-next)

#### Minimalistic framework for server-rendered React applications

[![NPM](https://nodei.co/npm/next.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/next)

- [https://npmdoc.github.io/node-npmdoc-next/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-next/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-next/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-next/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-next/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-next/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "next",
    "version": "2.1.1",
    "description": "Minimalistic framework for server-rendered React applications",
    "main": "./dist/server/next.js",
    "license": "MIT",
    "repository": "zeit/next.js",
    "publishConfig": {
        "tag": "beta"
    },
    "files": [
        "dist",
        "babel.js",
        "link.js",
        "css.js",
        "head.js",
        "document.js",
        "prefetch.js",
        "router.js",
        "error.js"
    ],
    "bin": {
        "next": "./dist/bin/next"
    },
    "scripts": {
        "build": "fly",
        "release": "fly release",
        "pretestonly": "fly pretest",
        "testonly": "cross-env NODE_PATH=test/lib jest \\.test.js",
        "posttestonly": "fly posttest",
        "pretest": "npm run lint",
        "test": "npm run testonly -- --coverage --forceExit --runInBand --verbose --bail",
        "coveralls": "nyc --instrument=false --source-map=false report --temp-directory=./coverage --reporter=text-lcov | coveralls",
        "lint": "standard 'bin/*' 'client/**/*.js' 'examples/**/*.js' 'lib/**/*.js' 'pages/**/*.js' 'server/**/*.js' 'test/**/*.js'",
        "prepublish": "npm run release",
        "precommit": "lint-staged"
    },
    "standard": {
        "parser": "babel-eslint",
        "ignore": [
            "**/node_modules/**"
        ]
    },
    "lint-staged": {
        "*.js": "standard",
        "bin/*": "standard"
    },
    "dependencies": {
        "ansi-html": "0.0.7",
        "babel-core": "6.24.0",
        "babel-generator": "6.24.0",
        "babel-loader": "6.4.1",
        "babel-plugin-module-resolver": "2.6.2",
        "babel-plugin-react-require": "3.0.0",
        "babel-plugin-transform-class-properties": "6.22.0",
        "babel-plugin-transform-es2015-modules-commonjs": "6.24.0",
        "babel-plugin-transform-object-rest-spread": "6.22.0",
        "babel-plugin-transform-react-jsx-source": "6.22.0",
        "babel-plugin-transform-react-remove-prop-types": "0.3.3",
        "babel-plugin-transform-runtime": "6.22.0",
        "babel-preset-latest": "6.24.0",
        "babel-preset-react": "6.23.0",
        "babel-runtime": "6.23.0",
        "case-sensitive-paths-webpack-plugin": "2.0.0",
        "cross-spawn": "5.1.0",
        "del": "2.2.2",
        "friendly-errors-webpack-plugin": "1.5.0",
        "glob": "^7.1.1",
        "glob-promise": "3.1.0",
        "htmlescape": "1.1.1",
        "http-status": "1.0.1",
        "is-windows-bash": "1.0.3",
        "json-loader": "0.5.4",
        "loader-utils": "1.1.0",
        "md5-file": "3.1.1",
        "minimist": "1.2.0",
        "mitt": "1.1.0",
        "mkdirp-then": "1.2.0",
        "mv": "2.1.1",
        "mz": "2.6.0",
        "path-match": "1.2.4",
        "pkg-up": "1.0.0",
        "react-hot-loader": "3.0.0-beta.6",
        "send": "0.15.1",
        "source-map-support": "0.4.14",
        "strip-ansi": "3.0.1",
        "styled-jsx": "0.5.7",
        "touch": "1.0.0",
        "unfetch": "2.1.2",
        "url": "0.11.0",
        "uuid": "3.0.1",
        "webpack": "2.3.3",
        "webpack-dev-middleware": "1.10.1",
        "webpack-hot-middleware": "2.18.0",
        "write-file-webpack-plugin": "4.0.0"
    },
    "devDependencies": {
        "babel-eslint": "7.2.0",
        "babel-jest": "18.0.0",
        "babel-plugin-istanbul": "4.1.1",
        "babel-plugin-transform-remove-strict-mode": "0.0.2",
        "babel-preset-es2015": "6.24.0",
        "benchmark": "2.1.4",
        "cheerio": "0.22.0",
        "chromedriver": "2.29.0",
        "coveralls": "2.13.0",
        "cross-env": "4.0.0",
        "fly": "2.0.5",
        "fly-babel": "2.1.1",
        "fly-clear": "1.0.1",
        "fly-esnext": "2.0.1",
        "fly-watch": "1.1.1",
        "husky": "0.13.3",
        "jest-cli": "19.0.1",
        "lint-staged": "^3.4.0",
        "node-fetch": "1.6.3",
        "node-notifier": "5.1.2",
        "nyc": "10.2.0",
        "react": "15.4.2",
        "react-dom": "15.4.2",
        "standard": "9.0.2",
        "wd": "1.2.0"
    },
    "peerDependencies": {
        "react": "^15.4.2",
        "react-dom": "^15.4.2"
    },
    "jest": {
        "testEnvironment": "node",
        "roots": [
            "test/"
        ]
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
