# Keccak.js

### Minor modified version which only loads client side sha3 as server side C++ causes issues with Meteor 1.3+

### Notes below taken from the original keccakjs library ->

It uses `browserify-sha3` to do the mapping for you.

Example usage:

```js
const keccak = require('keccakjs-browseronly')

var hash = new keccak() // uses 512 bits by default
hash.update('hello')
hash.update(new Buffer('42004200', 'hex'))
hash.digest() // binary output
hash.digest('hex') // hex output
```

**NOTE: This library supports the Keccak padding only - and not the final SHA3 padding.**
