# find-external-interface

> Find the name of a network interface bound to an external (non-localhost) IP address 

## Usage

This module exports a single function, [findExternalInterface](#findExternalInterface).

### findExternalInterface

Find the name of a network interface bound to an external (non-localhost) IP
address or `null` if none found.  This function returns the name of the first
interface which satisfies the criteria.

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)?** Options
    -   `options.IPv6` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** If true, find IPv6 interface (optional, default `false`)

**Examples**

```javascript
const {findExternalInterface} = require('find-external-interface');
const name = findExternalInterface(); // 'eth0'
const info = require('os').networkInterfaces(name); // ip address, etc.
```

Returns **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** Interface name

## Installation

```bash
$ npm install find-external-interface
```

## Requirements

- Node.js v4.0.0 or greater

## License

© 2017 [Christopher Hiller](https://github.com/boneskull).  Licensed MIT.