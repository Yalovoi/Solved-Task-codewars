# Solwed-Task
```
[8ky]
```
[Multiply](https://www.codewars.com/kata/50654ddff44f800200000004/train/javascript)
```javascript
function multiply(a, b){
 return a * b
}
```

[101 Dalmatians - squash the bugs, not the dogs!](https://www.codewars.com/kata/56f6919a6b88de18ff000b36/train/javascript)
```javascript
function howManyDalmatians(number){
  
  var dogs = ["Hardly any", "More than a handful!", "Woah that's a lot of dogs!", "101 DALMATIANS!!!"]
  
 return  number <= 10?dogs[0]:number <= 50?dogs[1]:number === 101? dogs[3] : dogs[2]
  
  }
  ```

[Sum The Strings](https://www.codewars.com/kata/5966e33c4e686b508700002d/train/javascript)
```javascript
function sumStr(a,b) {
  return String(+a + +b);
}
```

[Sum without highest and lowest number](https://www.codewars.com/kata/576b93db1129fcf2200001e6/train/javascript)
```javascript
function sumArray(array) {
  const sortedArr = array && array.sort((a, b) => a-b);
  return !sortedArr || sortedArr.length < 3 ? 0 : sortedArr.slice(1, sortedArr.length-1).reduce((a,b) => a + b, 0);
}
```

[Sum Mixed Array](https://www.codewars.com/kata/57eaeb9578748ff92a000009/train/javascript)
```javascript
function sumMix(x){
  return x.map(val => parseInt(val)).reduce((acc, cur) => acc + cur);
}
```








