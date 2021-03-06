# egg-cluster

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![Known Vulnerabilities][snyk-image]][snyk-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/egg-cluster.svg?style=flat-square
[npm-url]: https://npmjs.org/package/egg-cluster
[travis-image]: https://img.shields.io/travis/eggjs/egg-cluster.svg?style=flat-square
[travis-url]: https://travis-ci.org/eggjs/egg-cluster
[codecov-image]: https://codecov.io/github/eggjs/egg-cluster/coverage.svg?branch=master
[codecov-url]: https://codecov.io/github/eggjs/egg-cluster?branch=master
[david-image]: https://img.shields.io/david/eggjs/egg-cluster.svg?style=flat-square
[david-url]: https://david-dm.org/eggjs/egg-cluster
[snyk-image]: https://snyk.io/test/npm/egg-cluster/badge.svg?style=flat-square
[snyk-url]: https://snyk.io/test/npm/egg-cluster
[download-image]: https://img.shields.io/npm/dm/egg-cluster.svg?style=flat-square
[download-url]: https://npmjs.org/package/egg-cluster

Cluster Manager for Egg

---

## Install

```bash
$ npm i egg-cluster
```

## Usage

```js
const startCluster = require('egg-cluster').startCluster;
startCluster({
  baseDir: '/path/to/app',
  customEgg: '/path/to/framework',
});
```

You can specify a callback that will be invoked when application has started. However, master process will exit when catch an error.

```js
startCluster(options, () => {
  console.log('started');
});
```

## Options

| Param     | Type      | Description              |
| --------- | --------- | ------------------------ |
| baseDir   | `String`  | directory of application |
| customEgg | `String`  | directory of framework   |
| plugins   | `Object`  | plugins for unittest     |
| workers   | `Number`  | numbers of app workers   |
| port      | `Number`  | port                     |
| https     | `Boolean` | start a https server     |
| key       | `String`  | ssl key                  |
| cert      | `String`  | ssl cert                 |

## License

[MIT](LICENSE)

