# Solved-Task
```
[4ky]
```
[Twice linear](https://www.codewars.com/kata/twice-linear/train/javascript)
```javascript
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
["Very Even" Numbers.](https://www.codewars.com/kata/58c9322bedb4235468000019/train/javascript)
```javascript
function isVeryEvenNumber(n) {
  return !n-- || n % 9 % 2 === 1;
}
```

[Double Sort](https://www.codewars.com/kata/57cc79ec484cf991c900018d/train/javascript)
```javascript
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

[Squash the bugs](https://www.codewars.com/kata/56f173a35b91399a05000cb7/train/javascript)
```javascript
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
```javascript
function squareSum(numbers){
  return numbers.map(n => Math.pow(n, 2)).reduce((a, b) => a + b, 0);
}
```

[SpeedCode #2 - Array Madness](https://www.codewars.com/kata/56ff6a70e1a63ccdfa0001b1/train/javascript)
```javascript
function arrayMadness(a, b) {
  let square = a.reduce((a, b) => a + b**2, 0)
  let cube = b.reduce((a, b) => a + b**3, 0)
  return square > cube
}
```

[Reversing Words in a String](https://www.codewars.com/kata/57a55c8b72292d057b000594/train/javascript)
```javascript
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

[Welcome!](https://www.codewars.com/kata/577ff15ad648a14b780000e7/train/javascript)
```javascript
function greet(language) {
  var r = [
'Vitejte',
'Velkomst',
'Welkom',
'Tere tulemast',
'Tervetuloa',
'Welgekomen',
'Bienvenue',
'Willkommen',
'Failte',
'Benvenuto',
'Gaidits',
'Laukiamas',
'Witamy',
'Bienvenido',
'Valkommen',
'Croeso'];
  switch (language){
      case "czech":
          return r[0]
      case "danish":
          return r[1]
      case "dutch":
          return r[2]
      case "estonian":
          return r[3]
      case "finnish":
          return r[4]
      case "flemish":
          return r[5]
      case "french":
          return r[6]
      case "german":
          return r[7]
      case "irish":
          return r[8]
      case "italian":
          return r[9]
      case "latvian":
          return r[10]
      case "lithuanian":
          return r[11]
      case "polish":
          return r[12]
      case "spanish":
          return r[13]
      case "swedish":
          return r[14]
      case "welsh":
          return r[15]
      default:
          return 'Welcome'
  
  }
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











