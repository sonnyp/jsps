psjs
====

Pure JavaScript binding to [ps](https://en.wikipedia.org/wiki/Ps_%28Unix%29).

[![build status](https://img.shields.io/travis/sonnyp/psjs/master.svg?style=flat-square)](https://travis-ci.org/sonnyp/psjs/branches)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](http://standardjs.com/)

```
npm install psjs
```

# Usage

```javascript
var ps = require('psjs')

var options = {
  pid: process.pid, // if undefined, process.pid is used
  keywords: ['%cpu', '%mem'] // man ps for the list of keywords
}

ps.lookup(options, function(err, result) {
  console.log(err || result)
})
```

```json
{"%cpu": "44.7", "%mem": "0.4"}
```

# Test

```
npm install -g standard
npm test
```
