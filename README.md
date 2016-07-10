# poppins

A JavaScript dependency injection framework

## How?

### Create a dependency container

```javascript
const Poppins = require('poppins')
const inject = Poppins()
```

### Register a factory function

Here, our factory is named `kite` and requires `paper` and `string` as dependencies

```javascript
inject('kite', ({paper, string}) => {
  if (paper && string) {
    return 'a kite!'
  } else {
    return 'no kite :('
  }
})
```

### Get your stuff, with dependencies injected

```javascript
inject(function ({kite}) {
  // do stuff with the kite
})
```
