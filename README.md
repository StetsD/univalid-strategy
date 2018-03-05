# univalid-strategy

Abstract class of strategy for [univalid](https://github.com/StetsD/univalid) module.


## Install

```sh
npm i univalid-strategy
```


## Usage

```js
const UnivalidStrategy = require('univalid-strategy');
class UnivalidStrategyDefault extends UnivalidStrategy {
    //...
}
```


## API

Methods are necessary for define and extend.

### applyFilter(filter, val)

Tests the pattern matching of symbols (by event)

**filter** - Type `string`

In current moment available patterns:
* oL - only latin symbols
* oC - only cyrillic symbols
* oN - only numbers
* oP - only numbers and latin symbols

**val** - Type `string`


### check()

### getValidationHandlers()

### set()

### get()

## OPTIONS

### validHandlers

```js
constructor(){
    this.validHandlers = {
        'required': (val) => {
            let data = val ? ('' + val).trim() : '';
            return !!data;
        }
    }
}
```
## License

ISC©
