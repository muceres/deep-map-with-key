# deep-map-with-key

> Creates a new functor with the results of calling a provided function on every element in the calling functor and its key

[![tested with jest](https://img.shields.io/badge/tested_with-jest-99424f.svg)](https://github.com/facebook/jest)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier/)

## Install

```
$ npm install deep-map-with-key
```

## Usage

```js
const { deepMapWithKey } = require("deep-map-with-key");

const double = (number) => number * 2;

const cart = {
  rice: 2,
    fruits: {
      apple: 4,
      orange: 8
    }
  }
};

deepMapWithKey(double, cart); //=> { rice: 4, fruits: { apple: 8, orange: 16 } }
```

## API

### deepMapWithKey ⇒ `Object` \| `Array`

Creates a new functor with the results of calling a provided function on every element in the calling functor and its key

**Returns**: <code>Object</code> \| <code>Array</code> - Returns a new value after applying rules  
**Sig**: ((String, \*) -> \*) -> Object \| Array -> Object | Array

| Param   | Type                                      | Description                                                    |
| ------- | ----------------------------------------- | -------------------------------------------------------------- |
| fn      | <code>function</code>                     | The function to be called on every element of the input `list` |
| functor | <code>Object</code> \| <code>Array</code> | The functor to iterate over                                    |

**Example**

```js
const cart = { rice: 2, fruits: { apple: 4, orange: 8 } } };
const double = (number) => number * 2;
deepMapWithKey(double, cart); //=> { rice: 4, fruits: { apple: 8, orange: 16 } }
```

## License

MIT © [muceres](https://forgetheweb.eu)
