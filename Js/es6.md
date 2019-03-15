### Promise

```javascript
var promise = new Promise(function (resolve, reject) {
    //do something
    resolve("value");	
});

promise.then("do something");

// chaining
new Promise(function(resolve, reject) {
    resolve(1);
}).then(function(val){    
    return new Promise(function(resolve, reject){
        resolve(val+1); // 2
    })
}).then(function(val){
    console.log(val) // 2;
})
```

Promise` chaining시에는 return value가 다음으로 넘어간다. 이 때 `Promise`를 return 하면 `resolve` 값이 넘어간다.

### Spread

```javascript
... [1,2,3] // -> 1, 2, 3
```

