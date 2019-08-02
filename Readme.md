# string-spirits
![package version](https://img.shields.io/badge/dynamic/json.svg?color=d7d7d7&label=string-spirits&query=%24.version&url=https%3A%2F%2Funpkg.io%2Fstring-spirits%2Fpackage.json&prefix=v)
![stability](https://img.shields.io/badge/stability-release-66f29a.svg)
[![build status](https://travis-ci.org/partheseas/string-spirits.svg?branch=master)](https://travis-ci.org/partheseas/string-spirits)

A nice lightweight wildcard implementation written in TypeScript. I know there are already
a lot of these, but I had a use case that required to test a string against many wildcards
and determine which matched most specifically. I couldn't find one that did that, so
I just made my own. (If you would like that same functionality, look at the `bestMatch`
documentation.

## Installation
```Shell
yarn add string-spirits
```
You should use Yarn and [pnp](https://yarnpkg.com/en/docs/pnp).

## Usage
- [Documentation](https://string-spirits.now.sh)

Example:
```JavaScript
import Spirit from 'string-spirits';

const format = new Spirit( 'The weather is * today!' );
const greeting = 'The weather is great today!';

console.log( format.match( greeting )
  ? greeting
  : 'I have no idea what the weather is like because I am just a computer!' );
```

