# Solved-Tasks-CodeWars
JavaScript
```
[4ky]
```

[Twice linear](https://www.codewars.com/kata/twice-linear/train/javascript)
```
function dblLinear(n) {
  // a place to store the sequence
  const sequence = [1]; // start the sequence with 1
  const seen = {};
  // a place to keep track of the length, set to 0
  let length = 0;
  // a place to keep track of current x index, set to 0
  let xIndex = 0;

  // while length is less than n
  while(length < n) {
    const x = sequence[xIndex];
    // calculate y given the current x
    const y = 2 * x + 1;
    // insert y into the sequence in sorted order
    if (!seen[y]) {
      for (var i = sequence.length - 1; i >= 0; i--) {
        if (sequence[i] < y) {
          break;
        }
      }
      sequence.splice(i + 1, 0, y);
      seen[y] = true;
    }
    // calcuate z given the current x
    const z = 3 * x + 1;
    // insert z into the sequence in sorted order
    sequence.push(z);
    seen[z] = true;
    // increase length
    length++;
    // increase x index
    xIndex++;
  }
  // return sequence at n
  return sequence[n];
}
```


```
[6ky]
```


[Tortoise racing](https://www.codewars.com/kata/55e2adece53b4cdcb900006c/train/javascript)
```
function race(v1, v2, g) {
if(v1 >= v2)
  return null
  let time = g / (v2 - v1)
  let h = Math.trunc(time)
  let m = Math.trunc((time * 60) % 60)
  let s = Math.trunc((time * 3600) % 60)
    return [h, m, s]
}
```

[Backspaces in string](https://www.codewars.com/kata/5727bb0fe81185ae62000ae3/train/javascript)
```
function cleanString(s) {
  let arr = []
  for (let el of s) {
    if (el === "#") {
      arr.pop()
    } else {
      arr.push(el)
    }
  }
  return arr.join("")
}
```

[Unique In Order](https://www.codewars.com/kata/54e6533c92449cc251001667/train/javascript)
```
let uniqueInOrder=function(iterable){
  let newStr = []
  for(let i = 0;i < iterable.length;i++){
     if(iterable[i]!==iterable[i+1]){
      newStr.push(iterable[i])
    }
  }
  return newStr
}
```

[Array.diff](https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript)
```
function arrayDiff(a, b) {
   if (a.length === 0) {
    return [];
   } else {
     let diff = [];
     a.forEach(function(item) {
       if (!b.includes(item)){
        diff.push(item);
       }
     });
     return diff;
   }
}
```

[Are they the "same"?](https://www.codewars.com/kata/550498447451fbbd7600041c/train/javascript)
```
function comp(array1, array2){
  if (!array1 || !array2) {
    return false;
  } else {
    array1 = array1.map(a => { return a*a }).sort((a,b) => { return b-a }); 
    array2 = array2.sort((a,b) => { return b-a });
    for (let i = 0; i < array1.length; i++) {
      if (array2[i] !== array1[i]) {
         return false;
      }
    }
    return true;
  }
}
```

[Valid Braces](https://www.codewars.com/kata/5277c8a221e209d3f6000b56/train/javascript)
```
function validBraces(braces) {
  while (/\(\)|\[\]|\{\}/g.test(braces)) {
    braces = braces.replace(/\(\)|\[\]|\{\}/g, "");
  }
  return !braces.length;
}
```


```
[7ky]
```

[Series of integers from m to n](https://www.codewars.com/kata/5841f680c5c9b092950001ae/train/javascript)
```
function generateIntegers(m, n) {
  let newArr = []
  for(let i = m; i <= n;i++){
    newArr.push(i)
  }
  return newArr
}
```


[The Skiponacci Sequence](https://www.codewars.com/kata/580777ee2e14accd9f000165/train/javascript)
```
function skiponacci(n) {
  if(n === 1)return '1'
let fib = [1,1];
  for(let i  = 2;i < n;i++){
    fib.push(fib[i - 1]+ fib[i-2])
  }
 return  fib.map((el,i) => i % 2 !== 0?'skip':el).join(' ')                 
}
```


[Show multiples of 2 numbers within a range](https://www.codewars.com/kata/583989556754d6f4c700018e/train/javascript)
```
function multiples(s1,s2,s3){
   let arr = [];
  for (let i = 1; i < s3; i++){
    if(i % s1 == 0 && i % s2 == 0)
     arr.push(i);
  }  
  return arr;  
}
```


[254 shades of grey](https://www.codewars.com/kata/54d22119beeaaaf663000024/train/javascript)
```
const numberToHexadecimal = number => number.toString(16).padStart(2, '0')
const shadesOfGrey = n => {
  if (n < 0) return []
const max = Math.min(n, 254)
return Array.from({ length: max }, (_, index) => {
    const hexadecimal = numberToHexadecimal(index + 1)
    return `#${hexadecimal}${hexadecimal}${hexadecimal}`
  })
}
```


[80's Kids #2: Help ALF Find His Spaceship](https://www.codewars.com/kata/5660aa3d5e011dfd6e000063/train/javascript)
```
const findSpaceship = (map = '') => {
  if (!map.includes('X')) return 'Spaceship lost forever.'

  const spaces = map
    .trim()
    .split(/\n/)
    .reverse()

  const y = spaces.findIndex(space => space.includes('X'))
  const x = spaces[y].indexOf('X')

  return [x, y]
}
```


[Binary Addition](https://www.codewars.com/kata/551f37452ff852b7bd000139/train/javascript)
```
function addBinary(a,b) {
 return (a + b).toString(2)
}

const addBinary = (a, b) => (a + b).toString(2);

```


[Minimum to multiple](https://www.codewars.com/kata/5e030f77cec18900322c535d/train/javascript)
```
function minimum(a, x) {
  return Math.min(a % x, x - a % x)
}
```


[The highest profit wins!](https://www.codewars.com/kata/559590633066759614000063/train/javascript)
```
function minMax(arr){
  return [Math.min(...arr),Math.max(...arr)]
}
```


[Formatting decimal places #1](https://www.codewars.com/kata/5641c3f809bf31f008000042/train/javascript)
```
function twoDecimalPlaces(number) {
 return Math.trunc(number * 100) / 100
}
```


[Array Mash](https://www.codewars.com/kata/582642b1083e12521f0000da/train/javascript)
```
function arrayMash (array1, array2) {
let newArr = []
for(let i = 0;i < array1.length;i++){
  newArr.push(array1[i],array2[i])
}
  return newArr
}
```


[Find the next perfect square!](https://www.codewars.com/kata/56269eb78ad2e4ced1000013/train/javascript)
```
function findNextSquare(sq) {
  return Math.sqrt(sq)%1? -1 : Math.pow(Math.sqrt(sq)+1,2);
}
```


[You're a square!](https://www.codewars.com/kata/54c27a33fb7da0db0100040e/train/javascript)
```
let isSquare = function(n){
   return Math.sqrt(n) % 1 === 0 ? true : false;
}

let isSquare = function(n){
   return Math.sqrt(n) % 1 === 0 
}
```


[Absent vowel](https://www.codewars.com/kata/56414fdc6488ee99db00002c/train/javascript)
```
function absentVowel(x){
    const vowels = ["a", "e", "i", "o", "u"];
    for (let i = 0; i < vowels.length; i++) {
      if (!x.includes(vowels[i])) {
        return i;
      }
    }
  }
  ```


[Dominant array elements](https://www.codewars.com/kata/5a04133e32b8b998dc000089/train/javascript)
```
function solve(arr){
  let array = [arr[arr.length - 1]];
  for (let i = arr.length - 2; i >= 0; i--){
    if (arr[i] > array[0]) array.unshift(arr[i]);
  }
  return array;
}
```


[Squares sequence](https://www.codewars.com/kata/5546180ca783b6d2d5000062/train/javascript)
```
function squares(x, n) {
let arr = []
for(let i = 0; i < n;i++){
  arr.push(x)
  x = x * x
}
return arr
}
```

[Square Every Digit](https://www.codewars.com/kata/546e2562b03326a88e000020/solutions/javascript)
```
function squareDigits(num) {
let a = (num + '').split('');
  let res1 = [];
  for(let i = 0; i < a.length; i++){    
    res1.push(a[i] ** 2);   
  }
  return +res1.join('');
}
```

[Credit Card Mask](https://www.codewars.com/kata/5412509bd436bd33920011bc/train/javascript)
```
function maskify(cc) {
let maskCard = '';
for (let i = 0; i <= cc.length-1; i++) {
  if (i <= cc.length-5) {
    maskCard = maskCard + '#';
  } else {
    maskCard = maskCard + cc[i];
  }
}
  return maskCard;
}
```

["Very Even" Numbers.](https://www.codewars.com/kata/58c9322bedb4235468000019/train/javascript)
```
function isVeryEvenNumber(n) {
  return !n-- || n % 9 % 2 === 1;
}
```

[Double Sort](https://www.codewars.com/kata/57cc79ec484cf991c900018d/train/javascript)
```
function dbSort(a){
  const strings = a.filter( x => typeof x === "string" ).sort((a, b) => { 
    if (a > b) {
      return 1;
    } else if (b > a) {
      return -1;
    } else {
      return 0;
    }
  });  
  
  const numbers = a.filter( x => typeof x === "number").sort((a, b) => a-b);
  
  return [...numbers, ...strings];
}
```

[ATM](https://www.codewars.com/kata/5635e7cb49adc7b54500001c/train/javascript)
```
function solve(n) {
   if (n % 10 !== 0 ) return -1;
  let count = 0;
  let money = [500, 200, 100, 50, 20, 10];
  for (let bill of money) {
    while (n >= bill) {
      n = n - bill; 
      count++; 
    }
  }
 return count;
} 
```


```
[8ky]
```

[Training JS #4: Basic data types--Array](https://www.codewars.com/kata/571effabb625ed9b0600107a/train/javascript)
```
function getLength(arr){
  //return length of arr
  return arr.length
}
function getFirst(arr){
  //return the first element of arr
  return arr[0]
}
function getLast(arr){
  //return the last element of arr
  return arr[arr.length-1]
}
function pushElement(arr){
  let  el = 1 ;
  //push el to arr
  arr.push(el)
  return arr
}
function popElement(arr){
  //pop an element from arr
  arr.pop()
  return arr
}
```


[Filling an array (part 1)](https://www.codewars.com/kata/571d42206414b103dc0006a1/train/javascript)
```
function arr (N){
 let newArr = []
 for(let i = 0; i < N;i++){
   newArr.push(i)
 }
  return newArr
}
```

[Filling an array (part 1)](https://www.codewars.com/kata/571d42206414b103dc0006a1/train/javascript)
```
function arr (N){
 let newArr = []
 for(let i = 0; i < N;i++){
   newArr.push(i)
 }
  return newArr
} 
```


[Parse float](https://www.codewars.com/kata/57a386117cb1f31890000039/train/javascript)
```
function parseF(s) {
  if(s == parseFloat(s)){
    return Number.parseFloat(s)
    }else{
      return null
    }                    
  }

2 Variant

function parseF(s){
  return isNaN(parseFloat(s)) ? null : parseFloat(s);
}

3 Variant

let parseF = s => isNaN(parseFloat(s)) ? null : parseFloat(s)
```

[Convert number to reversed array of digits](https://www.codewars.com/kata/5583090cbe83f4fd8c000051/train/javascript)
```
function digitize(n){
 return  (n + '').split('').reverse().map(el => +el) 
}
```

[My head is at the wrong end!](https://www.codewars.com/kata/56f699cd9400f5b7d8000b55/train/javascript)
``
function fixTheMeerkat(arr) {
 return arr.reverse()
}
```

[A bugs trilogy: Episode 1 - "Let Math.Random(); decide your future"](https://www.codewars.com/kata/562e98755e9214cd2500003d/train/javascript)
```
function yourFutureCareer(){
let career = Math.random()
if (career <= 0.32) return 'FrontEnd Developer'
if (career <= 0.65) return 'BackEnd Developer'
return 'Full-Stack Developer'
    }
```


[Is it a number?](https://www.codewars.com/kata/57126304cdbf63c6770012bd/train/javascript)
```
function isDigit(s) {
 return s==parseFloat(s);
}
```


[Is this my tail?](https://www.codewars.com/kata/56f695399400f5d9ef000af5/train/javascript)
```
function correctTail(bod, tail) {
  return bod[bod.length-1] === tail
}
```

[Pre-FizzBuzz Workout #1](https://www.codewars.com/kata/569e09850a8e371ab200000b/train/javascript)
```
function preFizz(n) {
  let arr = []
  for(let i = 1;i <= n;i++){
   if(n > 0){
     arr.push(i)
    }
  }
  return arr
}
```


[Array Mash](https://www.codewars.com/kata/582642b1083e12521f0000da/solutions/javascript)
```
function arrayMash (array1, array2) {
let newArr = []
for(let i = 0;i < array1.length;i++){
  newArr.push(array1[i],array2[i])
}
  return newArr
}
```

[Find Maximum and Minimum Values of a List](https://www.codewars.com/kata/577a98a6ae28071780000989/solutions/javascript)
```
let min = function(list){
    return Math.min(...list);
}

let max = function(list){
    return Math.max(...list);
}
```

[Coefficients of the Quadratic Equation](https://www.codewars.com/kata/5d59576768ba810001f1f8d6/train/javascript)
```
function quadratic(x1, x2){
return[1, -x1-x2, x1*x2]
}
```

[Find Maximum and Minimum Values of a List](https://www.codewars.com/kata/577a98a6ae28071780000989/train/javascript)
```
let min = function(list){
    return Math.min(...list);
}
let max = function(list){
    return Math.max(...list);
}
```

[Filter out the geese](https://www.codewars.com/kata/57ee4a67108d3fd9eb0000e7/train/javascript)
```
function gooseFilter (birds){
  let geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  return birds.filter(bird => !geese.includes(bird));
}
```

[Expressions Matter](https://www.codewars.com/kata/5ae62fcf252e66d44d00008e/train/javascript)
```
function expressionMatter(a, b, c){
  return Math.max(a * (b + c), a * b * c, (a + b) * c, a + b + c)
}
```

[Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence](https://www.codewars.com/kata/57fb09ef2b5314a8a90001ed/train/javascript)
```
function replace(s){
  const array = s.split("");
  for (let i = 0; i < array.length; i++){
    if ((/[aeiou]/i).test(array[i])){
      array[i] = "!";
    }
  }
  return array.join("");
}
```

[Exclamation marks series #2: Remove all exclamation marks from the end of sentence](https://www.codewars.com/kata/57faece99610ced690000165/train/javascript)
```
function remove(s){
  return s.replace(/!*$/g, '')
}
```

[Exclamation marks series #1: Remove a exclamation mark from the end of string](https://www.codewars.com/kata/57fae964d80daa229d000126/train/javascript)
```
function remove(s){
  return s.slice(0, s[s.length-1] === "!" ? s.length-1 : s.length);
}
```

[Double Char](https://www.codewars.com/kata/56b1f01c247c01db92000076/train/javascript)
```
function doubleChar(str) {
 return str.split("").map( n => n + n ).join("");
}
```

[Do I get a bonus?](https://www.codewars.com/kata/56f6ad906b88de513f000d96/train/javascript)
```
function bonusTime(salary, bonus) {
return bonus===true?"£"+ salary*10:"£"+ salary
}
```

[Count by X](https://www.codewars.com/kata/5513795bd3fafb56c200049e/train/javascript)
```
function countBy(x, n) {
  let z = [];
  while (z.length < n) {
    for (let i = x; i <= (x * n); ++i) {
      i % x === 0 && z.push(i);
    }
  }
  return z;
}
```

[All Star Code Challenge #22](https://www.codewars.com/kata/5865cff66b5699883f0001aa/train/javascript)
```
function toTime(s) {
 return `${Math.floor(s / 3600)} hour(s) and ${Math.floor(s % 3600 / 60)} minute(s)`       
  }
  ```

[Price of Mangoes](https://www.codewars.com/kata/57a77726bb9944d000000b06/train/javascript)
```
function mango(quantity, price){
let a = Math.floor(quantity / 3)
return (quantity - a) * price
}
```

[Correct the mistakes of the character recognition software](https://www.codewars.com/kata/577bd026df78c19bca0002c0/train/javascript)
```
function correct(string){
	const correction = {
    "5": "S",
    "0": "O",
    "1": "I"
  }
  return string.split("").map(x => x = correction[x] !== undefined ? correction[x] : x).join(""); 
}
```

[Convert a String to a Number!](https://www.codewars.com/kata/544675c6f971f7399a000e79/train/javascript)
```
let stringToNumber = function(str){ 
  return Number(str);
}
```

[Convert a Number to a String!](https://www.codewars.com/kata/5265326f5fda8eb1160004c8/train/javascript)
```
function numberToString(num) {
 return String(num);
}
```

[Check the exam](https://www.codewars.com/kata/5a3dd29055519e23ec000074/train/javascript)
```
function checkExam(array1, array2) {
 let sum = 0;
 for (let i = 0; i < array1.length; i++) {
   if (array2[i] !== "") {
     sum = sum += array1[i] === array2[i] ? 4 : -1;
   }
 }
 return sum > 0 ? sum : 0;
}
```

[Century From Year](https://www.codewars.com/kata/5a3fe3dde1ce0e8ed6000097/train/javascript)
```
function century(year) {
 return Math.floor(year/100) + (year % 100 === 0 ? 0 : 1);
}
```

[Cat years, Dog years](https://www.codewars.com/kata/5a6663e9fd56cb5ab800008b/train/javascript)
```
let humanYearsCatYearsDogYears = function(humanYears) {
  const catYears = humanYears === 1 ? 15 :
                   humanYears === 2 ? 15 + 9 :
                   15 + 9 + ((humanYears - 2) * 4);
  
  const dogYears = humanYears === 1 ? 15 :
                   humanYears === 2 ? 15 + 9 :
                   15 + 9 + ((humanYears - 2) * 5);
  
  return [humanYears,catYears,dogYears];
}
```

[Bin to Decimal](https://www.codewars.com/kata/57a5c31ce298a7e6b7000334/train/javascript)
```
function binToDec(bin){
  return parseInt(bin, 2);
}
```

[Training JS #34: methods of Math---pow() sqrt() and cbrt()](https://www.codewars.com/kata/5733f948d780e27df6000e33/train/javascript)
```
function cutCube(volume,n){
return Math.cbrt(volume / n) % 1 === 0 && Math.cbrt(n) % 1 === 0 ? true : false; 
  }
  
  function cutCube(volume,n){
 return Math.cbrt(volume) % 1 == 0 && Math.cbrt(volume / n) % 1 == 0;
}
  ```
  
[N-th Power](https://www.codewars.com/kata/57d814e4950d8489720008db/train/javascript)
```
function index(array, n){
   if (array[n] == undefined) { 
    return -1;
  }  else {
    return Math.pow(array[n], n);
  }
}

function index(array, n){
  return array[n] ** n || -1;
}

function index( array, n ) {
    return (array.length) > n ? Math.pow(array[n], n) : -1;
}
```


[Multiply](https://www.codewars.com/kata/50654ddff44f800200000004/train/javascript)
```
function multiply(a, b){
 return a * b
}
```

[101 Dalmatians - squash the bugs, not the dogs!](https://www.codewars.com/kata/56f6919a6b88de18ff000b36/train/javascript)
```
function howManyDalmatians(number){
  
  let dogs = ["Hardly any", "More than a handful!", "Woah that's a lot of dogs!", "101 DALMATIANS!!!"]
  
 return  number <= 10?dogs[0]:number <= 50?dogs[1]:number === 101? dogs[3] : dogs[2]
  
  }
  ```

[Sum The Strings](https://www.codewars.com/kata/5966e33c4e686b508700002d/train/javascript)
```
function sumStr(a,b) {
  return String(+a + +b);
}
```

[Sum without highest and lowest number](https://www.codewars.com/kata/576b93db1129fcf2200001e6/train/javascript)
```
function sumArray(array) {
  const sortedArr = array && array.sort((a, b) => a-b);
  return !sortedArr || sortedArr.length < 3 ? 0 : sortedArr.slice(1, sortedArr.length-1).reduce((a,b) => a + b, 0);
}
```

[Sum Mixed Array](https://www.codewars.com/kata/57eaeb9578748ff92a000009/train/javascript)
```
function sumMix(x){
  return x.map(val => parseInt(val)).reduce((acc, cur) => acc + cur);
}
```

[Squash the bugs](https://www.codewars.com/kata/56f173a35b91399a05000cb7/train/javascript)
```
function findLongest(str) {
  const spl = str.split(" ");
  let longest = 0
  for (let i = 0; i < spl.length; i++) {
    if (spl[i].length > longest) (
      longest = spl[i].length
    )
  }
  return longest
}
```

[Square(n) Sum](https://www.codewars.com/kata/515e271a311df0350d00000f/train/javascript)
```
function squareSum(numbers){
  return numbers.map(n => Math.pow(n, 2)).reduce((a, b) => a + b, 0);
}
```

[SpeedCode #2 - Array Madness](https://www.codewars.com/kata/56ff6a70e1a63ccdfa0001b1/train/javascript)
```
function arrayMadness(a, b) {
  let square = a.reduce((a, b) => a + b**2, 0)
  let cube = b.reduce((a, b) => a + b**3, 0)
  return square > cube
}
```

[Reversing Words in a String](https://www.codewars.com/kata/57a55c8b72292d057b000594/train/javascript)
```javasc
function reverse(string){
  return string.split(" ").reverse().join(" ");
}
```

[Reversed Words](https://www.codewars.com/kata/51c8991dee245d7ddf00000e/train/javascript)
```javascript
function reverseWords(str){
  return str.split(" ").reverse().join(" ");
}
```

[Classic Hello World](https://www.codewars.com/kata/57036f007fd72e3b77000023/train/javascript)
```javascript
class Solution{
  static main() {
    console.log("Hello World!");
  }  
}
```

[Watermelon](https://www.codewars.com/kata/55192f4ecd82ff826900089e/train/javascript)
```javascript
function divide(weight){
  return weight <= 2 ? false : weight % 2 === 0;
}
```

[Triple Trouble](https://www.codewars.com/kata/5704aea738428f4d30000914/train/javascript)
```javascript
function tripleTrouble(one, two, three){
  let string = ""
   for(let i = 0; i < one.length; i++){
    string += one[i]+two[i]+three[i];
  }
   return string 
 }
 ```


[Twice as old](https://www.codewars.com/kata/5b853229cfde412a470000d0/train/javascript)
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs(dadYearsOld - sonYearsOld * 2)
}
```

[Total amount of points](https://www.codewars.com/kata/5bb904724c47249b10000131/train/javascript)
```javascript
function points(games) {
  return games.map(x => {
    const [a, b] = x.split(":");
    if (a > b) {
      return 3;
    } else if (a < b) {
      return 0;
    } else {
      return 1;
    }
  }).reduce((a,b) => a + b, 0);
}
```

[You only need one - Beginner](https://www.codewars.com/kata/57cc975ed542d3148f00015b/train/javascript)
```javascript
function check(a,x){
    return a.includes(x);
};
```

[Find variable which breaks strict comparison!](https://www.codewars.com/kata/560f8d41cf6e1fe5c900002e/train/javascript)
```javascript
function findStrangeValue() {
  return NaN;
}
```

[Remove First and Last Character](https://www.codewars.com/kata/56bc28ad5bdaeb48760009b0/train/javascript)
```javascript
function removeChar(str){
return str.slice(1, -1)
 }
 ```

[Remove String Spaces](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/javascript)
```
function noSpace(x){
 return   x.split(' ').join('');
}
```

[Count the Monkeys!](https://www.codewars.com/kata/56f69d9f9400f508fb000ba7/train/javascript)
```
function monkeyCount(n) {
let monkey = [];
  for(let i = 1; i <= n;i++){
    monkey.push(i);
  }
return monkey
}
```

[What is between?](https://www.codewars.com/kata/55ecd718f46fba02e5000029/train/javascript)
```
function between(a, b) {
  const between = [];
  for (let i = a; i <= b; i++) {
    between.push(i);
  }
  return between;
}
```

[Well of Ideas - Easy Version](https://www.codewars.com/kata/57f222ce69e09c3630000212/train/javascript)
```
function well(x){
  const good = x.filter( x => x === "good").length;
  if (good === 0) { 
    return "Fail!" 
  } else { 
    return good <= 2 ? 'Publish!' : 'I smell a series!'
  };
}
```

[Training JS #7: if..else and ternary operator](https://www.codewars.com/kata/57202aefe8d6c514300001fd/train/javascript)
```
function saleHotdogs(n){
  if(n<5){return n*  100}
  if(n>=5&&n<10){return n * 95}
  if(n>=10){return n * 90}
}
```

[The Wide-Mouthed frog!](https://www.codewars.com/kata/57ec8bd8f670e9a47a000f89/train/javascript)
```
function mouthSize(animal) {
  return /alligator/gi.test(animal) ? "small" : "wide";
}
```

[The Feast of Many Beasts](https://www.codewars.com/kata/5aa736a455f906981800360d/train/javascript)
```
function feast(beast, dish) {
if(beast[0] === dish[0] && beast[beast.length -1] === dish[dish.length -1])
return true;
else return false;
}
```

[The falling speed of petals](https://www.codewars.com/kata/5a0be7ea8ba914fc9c00006b/train/javascript)
```
function sakuraFall(v) {
  return v <= 0 ? 0 : (80 * 5) / v;
}
```

[Surface Area and Volume of a Box](https://www.codewars.com/kata/565f5825379664a26b00007c/train/javascript)
```
function getSize(width, height, depth) {
 const volume = width * height * depth;
 const area = 2 * (width * height + height * depth + width * depth);
 return [area, volume]
}
```

[Even or Odd](https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/javascript)
```
function even_or_odd(number) {
 return number % 2 === 0?'Even':'Odd'
 }
 ```

[Sum of positive](https://www.codewars.com/kata/5715eaedb436cf5606000381/train/javascript)
```
function positiveSum(arr) {
  let total = 0;    
  for (i = 0; i < arr.length; i++) {    // setup loop to go through array of given length
    if (arr[i] > 0) {                   // if arr[i] is greater than zero
      total += arr[i];                  // add arr[i] to total
    }
  }
  return total;                         // return total
}
```

[Sum Mixed Array](https://www.codewars.com/kata/57eaeb9578748ff92a000009/train/javascript)
```
function sumMix(x){
  return x.map(val => parseInt(val)).reduce((acc, cur) => acc + cur);
}
```

[Sum without highest and lowest number](https://www.codewars.com/kata/576b93db1129fcf2200001e6/train/javascript)
```
function sumArray(array) {
  const sortedArr = array && array.sort((a, b) => a-b);
  return !sortedArr || sortedArr.length < 3 ? 0 : sortedArr.slice(1, sortedArr.length-1).reduce((a,b) => a + b, 0);
}
```

[noobCode 01: SUPERSIZE ME.... or rather, this integer!](https://www.codewars.com/kata/5709bdd2f088096786000008/train/javascript)
```
function superSize(num){
  return +String(num).split("").sort((a, b) => b - a).join("");
}
```

[Surface Area and Volume of a Box](https://www.codewars.com/kata/565f5825379664a26b00007c/train/javascript)
```
function getSize(width, height, depth) {
 const volume = width * height * depth;
 const area = 2 * (width * height + height * depth + width * depth);
 return [area, volume]
}
```

[The falling speed of petals](https://www.codewars.com/kata/5a0be7ea8ba914fc9c00006b/train/javascript)
```
function sakuraFall(v) {
  return v <= 0 ? 0 : (80 * 5) / v;
}
```

[The Feast of Many Beasts](https://www.codewars.com/kata/5aa736a455f906981800360d/train/javascript)
```
function feast(beast, dish) {
return splice(beast) === splice(dish);
  function splice(word) {
    return word[0] + word[word.length - 1];
  }
  }
  ```

[The Wide-Mouthed frog!](https://www.codewars.com/kata/57ec8bd8f670e9a47a000f89/train/javascript)
```
function mouthSize(animal) {
  return /alligator/gi.test(animal) ? "small" : "wide";
}
```

[Remove String Spaces](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/javascript)
```
function noSpace(x){
 return   x.split(' ').join('');
}
```

[isReallyNaN](https://www.codewars.com/kata/56c24c58e0c0f741d4001aef/train/javascript)
```
const isReallyNaN = (val) => {
  return Number.isNaN(val)?true:false;
};

const isReallyNaN = Number.isNaN
```

[Filter the number](https://www.codewars.com/kata/55b051fac50a3292a9000025/train/javascript)
```
let FilterString = function(value) {
  let str = value.split("");
  let arr = [];
  for(let i = 0; i < str.length; i++){
    if(isNaN(str[i]) == false){arr.push(str[i]);}
  }
  return +arr.join('');
}


let FilterString = function(value) {
  let str = '';
  for (i = 0; i < value.length; i++){
    if (!isNaN(value[i])){
      str += value[i]; 
    }
  }
  return +str;
}

```

[Is integer safe to use?](https://www.codewars.com/kata/55a4f9afeffe4231090000d6/train/javascript)
```
function SafeInteger(n) {
  return Number.isSafeInteger(n)
}

function SafeInteger(n) {
  return !!(Number.isSafeInteger(n));
}
```

[5 without numbers !!](https://www.codewars.com/kata/59441520102eaa25260000bf/train/javascript)
```
function unusualFive() {
  return "fiver".length;
}
```

[A Needle in the Haystack](https://www.codewars.com/kata/56676e8fabd2d1ff3000000c/train/javascript)
```
function findNeedle(haystack) {
    let index = haystack.indexOf('needle');
    return "found the needle at position " + index;
  }
  ```

[A wolf in sheep's clothing](https://www.codewars.com/kata/5c8bfa44b9d1192e1ebd3d15/train/javascript)
```
function warnTheSheep(queue) {
  const sheep = queue.length - (queue.indexOf('wolf') + 1);
  const first = queue[queue.length - 1];
  return first === 'wolf' ? `Pls go away and stop eating my sheep` : `Oi! Sheep number ${sheep}! You are about to be eaten by a wolf!`
}
```

[Abbreviate a Two Word Name](https://www.codewars.com/kata/57eadb7ecd143f4c9c0000a3/train/javascript)
```
function abbrevName(name){
    return name.split(" ").map(n => n[0].toUpperCase()).join(".");
}
```

[Alan Partridge II - Apple Turnover](https://www.codewars.com/kata/580a094553bd9ec5d800007d/train/javascript)
```
function apple(x){
  return Math.pow(x, 2) > 1000 ? 'It\'s hotter than the sun!!' : 'Help yourself to a honeycomb Yorkie for the glovebox.';
}
```

[Is it a palindrome?](https://www.codewars.com/kata/57a1fd2ce298a731b20006a4/train/javascript)
```
function isPalindrome(x) {
  let str = ''
  x = x.toLowerCase()
 for(let i = 0;i < x.length;i++){
   str = x[i] + str
 }
  return str === x
}
```

[BASIC: Making Six Toast.](https://www.codewars.com/kata/5834fec22fb0ba7d080000e8/train/javascript)
```
function sixToast(num) {
  return Math.abs(num - 6)
}

function sixToast(num) {
  
  return num >= 6 ? num - 6 : num;
}

function sixToast(num) {
  if (num < 6){
  return 6 - num
  } else 
  return num -6; 
}
```

[Closest elevator](https://www.codewars.com/kata/5c374b346a5d0f77af500a5a/train/javascript)
```
function elevator(left, right, call){
let a = Math.abs(call - left)
let b = Math.abs(call - right)
if(b <= a){return 'right'
     }else{return 'left'}
  }
  
  function elevator(left, right, call) {
  return Math.abs(call - left) < Math.abs(call - right) ? 'left' : 'right';
}
```  

[Area of a Square](https://www.codewars.com/kata/5748838ce2fab90b86001b1a/train/javascript)
```
function squareArea(A){
 return +(Math.pow(((A*2)/Math.PI),2)).toFixed(2);
}
```

[Alan Partridge II - Apple Turnover](https://www.codewars.com/kata/580a094553bd9ec5d800007d/train/javascript)
```
function apple(x){
if(x**2>1000){return'It\'s hotter than the sun!!';
  }else{return 'Help yourself to a honeycomb Yorkie for the glovebox.';
       }
}
```

[Beginner - Reduce but Grow](https://www.codewars.com/kata/57f780909f7e8e3183000078/train/javascript)
```
function grow(x){
  return x.reduce((a, b) => a * b);
}

``` Ruby```

def grow(x)
  x.map.reduce(:*)
end
```

[Array plus array](https://www.codewars.com/kata/5a2be17aee1aaefe2a000151/train/javascript)
```
function arrayPlusArray(arr1, arr2) {
  return [...arr1, ...arr2].reduce((sum, val) => sum + val); //something went wrong
}
```

[Beginner Series #1 School Paperwork](https://www.codewars.com/kata/55f9b48403f6b87a7c0000bd/train/javascript)
```
function paperwork(n, m) {
  return n + m <= 0 ? 0 : n * m;
}
```

[Beginner Series #2 Clock](https://www.codewars.com/kata/55f9bca8ecaa9eac7100004a/train/javascript)
```
function past(h, m, s){
  return ((h*3600 + m * 60 + s) *1000);
}
```

[Beginner Series #4 Cockroach](https://www.codewars.com/kata/55fab1ffda3e2e44f00000c6/train/javascript)
```
function cockroachSpeed(s) {
  return Math.floor(s / 0.036);
}
```

























