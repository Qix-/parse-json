# parse-json [![Build Status](https://travis-ci.org/sindresorhus/parse-json.svg?branch=master)](https://travis-ci.org/sindresorhus/parse-json)

> Parse JSON with more helpful errors


## Install

```
$ npm install --save parse-json
```


## Usage

```js
var parseJson = require('parse-json');
var json = '{\n\t"foo": true,\n}';

JSON.parse(json);
/*
undefined:3
}
^
SyntaxError: Unexpected token }
*/

parseJson(json);
/*
SyntaxError: Trailing comma in object at 3:1
}
^
*/
```

## API

### parseJson(input, [reviver])

#### input

Type: `string`

#### reviver

Type: `function`

Prescribes how the value originally produced by parsing is transformed, before being returned. See [`JSON.parse` docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse#Using_the_reviver_parameter
) for more.


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
