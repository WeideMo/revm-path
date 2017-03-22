# revm-path

> Create a revved file path appending md5 hash string.


## Install

```
$ npm install --save revm-path
```


## Usage

```js
var revPath = require('revm-path');
var hash = 'bb9d8fe615'

var path = revPath('src/unicorn.png', hash);
//=> 'src/unicorn.png?bb9d8fe615'

revPath('src/unicorn.png', Date.now());
//=> 'src/unicorn.png?1432309925925'

// you can also revert an already hashed path
revPath.revert(path, hash);
//=> 'src/unicorn.png'
```


