# Array

```js
function duplicate(arr) {
  return arr.concat(arr);
}

duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]

const duplicate = (arr) => [...arr, ...arr];

duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]
```

Array.slice()
Array.from()
Array.length

```js
{
  function duplicate(array) {
    // 如何copy一个array: Array.from(array) 也行
    var result = array.slice();
    const length = array.length;

    //  array.forEach(function(item) {
    //    array.push(item)
    //  })

    // 如果用array.length在判断条件中，会死循环，因为每次都会增加一个item
    for (var i = 0; i < length; i++) {
      result.push(array[i]);
      //      if(array.length > 6) {
      //        debug
      //      }
    }

    return result;
  }
  var old_array = [1, 2, 3, 4, 5];
  console.log(duplicate(old_array));
  console.log(old_array);
}
```
