```js
// es5
var arr = ['val1', 'val2', 'val3'];
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]);
  console.log(i);
  console.log(arr);
}

//es6
arr.map((val, index, array) => {
  console.log(val);
  console.log(index);
  console.log(array);
})
arr.forEach((val, index, array) => {
  console.log(val);
  console.log(index);
  console.log(array);
})

for (let i = 0; i < allImgs.length; i++)
```
