### join

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var energy = fruits.join(",");  // "Banana,Orange,Apple,Mango"
```

### splice

> 기존 배열을 변경

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
//index, number_of_removed
fruits.splice(0,1); // ["Banana"] , fruits -> ["Orange", "Apple", "Mango"]
```

### slice

> 기존 배열을 변경하지 않음

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
//index, number_of_removed
fruits.slice(0,1); // ["Banana"]
fruits.slice(2); // ["Apple", "Mango"]
```

### reduce

```javascript
var default_val = 0;
[1, 2, 3].reduce(function(acc, val) {
    return acc * 3 + val
}, default_val)

// 1 * 3 * 3 + 2 * 3 + 3
```

