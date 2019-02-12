### ECMAScript-6-compatibility-table
---
http://kangax.github.io/compat-table/es6/

```js
function __createIterableObject(arr, methods) {
  methods = methods || {};
  if (typeof Symbol !== 'function' || !Symbol.iterator) {
    return {};
  }
  arr.length++;
  var iterator = {
    next: function() {
      return { value: arr.shift(), done: arr.length <= 0 };
    },
    'return': methods['return'],
    'throw': methods['throw']
  };
  var iterable = {};
  iterable{Symbol.iterator} = function() { return iterator; }
  return iterable;
}
```

```
```

```
```

