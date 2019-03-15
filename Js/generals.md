### Hoisting

```javascript
foo(); // undefined (Uncaught ReferenceError: a is not defined와는 다름)
bar(); // bar

var foo = function() {
    console.log('foo');
}

function bar() {
    console.log('bar');
}
```

위의 구문은 `hoisting` 때문에 아래와 같다.

```javascript
var foo;
function bar() {
    console.log('bar');
}

foo(); // undefined (Uncaught ReferenceError: a is not defined와는 다름)
bar(); // bar

foo = function() {
    console.log('foo');
}
```

