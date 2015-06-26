level-mobile
===========

**Note. This is a work in progress. Use at own risk**

<img alt="LevelDB Logo" height="100" src="http://leveldb.org/img/logo.svg">

**Fast & simple storage - a Node.js-style LevelDB wrapper**

[![NPM](https://nodei.co/npm/level-mobile.png)](https://nodei.co/npm/level-mobile/)

[![Build Status](https://secure.travis-ci.org/Level/level-mobile.png)](http://travis-ci.org/Level/level-mobile)

This is a convenience package that bundles the current release of **[LevelUP](https://github.com/level/levelup)** and **[LevelDOWN-Mobile](https://github.com/level/leveldown-mobile)** and exposes LevelUP on its export.

Use this package to avoid having to explicitly install LevelDOWN-Mobile when you want to use LevelDOWN-Mobile with LevelUP.

```js
var level = require('level-mobile)

// 1) Create our database, supply location and options.
//    This will create or open the underlying LevelDB store.
var db = level('./mydb')

// 2) put a key & value
db.put('name', 'Level', function (err) {
  if (err) return console.log('Ooops!', err) // some kind of I/O error

  // 3) fetch by key
  db.get('name', function (err, value) {
    if (err) return console.log('Ooops!', err) // likely the key was not found

    // ta da!
    console.log('name=' + value)
  })
})
```

See **[LevelUP](https://github.com/level/levelup)** and **[LevelDOWN-Mobile](https://github.com/level/leveldown-mobile)** for more details.

<a name="contributing"></a>
Contributing
------------

**level-mobile** is an **OPEN Open Source Project**. This means that:

> Individuals making significant and valuable contributions are given commit-access to the project to contribute as they see fit. This project is more like an open wiki than a standard guarded open source project.

See the [contribution guide](https://github.com/Level/community/blob/master/CONTRIBUTING.md) for more details.

<a name="licence"></a>
Licence &amp; Copyright
-------------------

Copyright (c) 2012-2015 **level-mobile** [contributors](https://github.com/level/community#contributors).

**level-mobile** is licensed under the MIT license. All rights not explicitly granted in the MIT license are reserved. See the included LICENSE.md file for more details.
