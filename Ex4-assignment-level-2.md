## writeCode

```js
let words = [
  "mystery",
  "brother",
  "aviator",
  "crocodile",
  "pearl",
  "orchard",
  "crackpot",
  "rhythm"
];
// - Write a function findLongestWord that takes an array of words and returns the longest word from the array. (Use above array "words" to test it). If there are 2 with the same length, it should return the first occurrence.

function findLongestWord(array) {
  let l = 0;
  let longestWord = "";
  for (word of array) {
    if (word.length > l) {
      l = word.length;
      longestWord = word;
    } 
  }
  return longestWord;
}

// - Convert the above array "words" into an array of length of word instead of word.

words.map(x => x.length);

// - Create a new array that only contains word with atleast one vowel.

let newArr = [];
let vowels = ["a", "e", "i", "o", "u"];


function checkVowel(word) {
  for (letter of word.toLowerCase()) {

    if (newArr.includes(word)) {
      continue;
    }
else {
    if (vowels.includes(letter)) {
      newArr.push(word);
    }
}
  }
  return newArr;
}

words.forEach(checkVowel);


// - Find the index of the word "rhythm"

words.indexOf("rhythm");

// - Create a new array that contians words not starting with vowel.

function checkStartLetter(word) {
  if (vowels.includes(word.toLowerCase().charAt(0))) {
    return false;
  }
  else return true;
}

word.filter(checkStartLetter);

// - Create a new array that contianse words not ending with vowel

function checkEndLetter(word) {
  if (vowels.includes(word.toLowerCase().charAt(word.length - 1))) {
    return false;
  }
  else return true;
}

words.filter(checkEndLetter);



let numbers = [6, 12, 1, 18, 13, 16, 2, 1, 8, 10];

// - Create a sumArray function that takes an array of number as a parameter, and calculate the sum of all its numbers

function sumArray(array) {
  let sum = 0;
  array.forEach(x => sum += x);
  return sum;
}

// - Make a new array that contains number multiplied by 3 like [6, 18, 27 ...]

numbers.map(x => x * 3);

// - Create a new array that contains only even numbers

numbers.filter(x => {x % 2 == 0})

// - Create  a new array that contains only odd numbers.

numbers.filter(x => {x % 2 != 0})

// - Create a new array that should have true for even number and false for odd numbers.

numbers.map(x => { 
  if (x % 2 == 0) {return true}
  else return false
})

// - Sort the above number in assending order.

numbers.sort((a, b) => {a - b});

// - Does sort mutate the original array?

Yes

// - Find the sum of the numbers in the array.

sumArray(numbers);

//- Write a function averageNumbers that receives an array of numbers and calculate the average of the numbers

function averageNumbers(array) {
 return sumArray(array) / array.length;
}

let strings = [
  "seat",
  "correspond",
  "linen",
  "motif",
  "hole",
  "smell",
  "smart",
  "chaos",
  "fuel",
  "palace"
];
// - Write a function averageWordLength that receives an array of words and calculates the average length of the words.

function averageWordLength(array) {
  let sum = 0;
  for (word of array) {
    sum += (word.length);
  }
  return sum / array.length;
}
```

## String Methods-writeCode

- Write a JavaScript function to check whether input value is a string or not.

```js
/* Requirements
  @name isString
  @parameter (any value) val
  @return Boolean
*/

function isString(value) {
  if (typeof value === "string")
  {return true;}
  else return false;
}

// Test
console.log(isString("tony stark")); // true;
console.log(isString([1, 2, 4, 0])); // false;
```

- Write a JavaScript function to check whether a string is blank or not.

```js
/* Requirements
  @name isBlank
  @parameter (any value) val
  @return Boolean
*/

function isBlank(val) {
  if (String(val).trim() === "") {return true}
  else return false
}

// Test
console.log(isBlank("")); // true;
console.log(isBlank("abc")); // false;
```

- Write a JavaScript function to split a string and convert it into an array of words.

```js
/* Requirements
  @name stringToArray
  @parameter (string) text
  @return Array
*/
function stringToArray(text) {
  text.split(" ");
}

// Test
console.log(stringToArray("Hello World")); // ["Robin", "Singh"];
console.log(stringToArray("Lady Bird")); // ["Lady", "Bird"];
```

- Write a JavaScript function to return specified number of characters from a string.

```js
/* Requirements
  @name truncate
  @parameter (string, number) text, len
  @return String
*/
function truncate(text, len) {
  text.substring(0, len);
}

// Test
console.log(truncate("Robin Singh", 4)); //"Robi";
```

- Write a JavaScript function to convert a `string` in abbreviated form.

```js
/* Requirements
  @name abbrevName
  @parameter (string) fullName
  @return String
*/
function abbrevName(fullName) {
  fullName.split();
  
}


INCOMPLETE

// Test
console.log(abbrevName("Robin Singh")); //"Robin S."
```

- Write a JavaScript function to hide email addresses to protect from unauthorized user.

```js
/* Requirements
  @name protect
  @parameter (string) email
  @return String
*/


function protect(email) {
  let atIndex = email.indexOf("@");
  let id = email.substring(0, email.lastIndexOf("@"))
  let l = Math.floor(id.length / 2)
  let mask = email.substring(l, email.lastIndexOf("@"));
  let remain = email.substring(0, l);
  return remain.padEnd(id.length, "*") + email.substring(email.lastIndexOf("@"));
}

// Test
console.log(protect("robin_singh@example.com")); // "robin...@example.com"
```

- Write a JavaScript function to parameterize a string.

```js
/* Requirements
  @name parameterize
  @parameter (string) str
  @return String
*/

function parameterize(str) {
  let s = str.toLowerCase();
  let arr = s.split(" ");
  return arr.join("-");
}

// Test
console.log(parameterize("Robin Singh from USA.")); // "robin-singh-from-usa"
```

- Write a JavaScript function to capitalize the first letter of a `string`.

```js
/* Requirements
@name capitalizeFirst
@parameter (string, number) text, len
@return String
*/
function capitalizeFirst(str) {
  let firstChar = str.charAt(0);
  let lowerFirst = firstChar.toLowerCase();
  let final = lowerFirst + str.substring(1);
  return final;
}

// Test
console.log(capitalizeFirst("js string exercises")); // "Js string exercises"
```

- Write a JavaScript function to capitalize the first letter of each word in a string.

```js
/* Requirements
  @name capitalizeWords
  @parameter (string) text
  @return String
*/

function capitalizeWords(text) {
  let arr = text.split(" ");
  let newArr = arr.map(x => {
    let f = String(x).charAt(0).toUpperCase();
    let word = f + x.substring(1);
    return word;
  })
  return newArr.join(" ");
}

console.log(capitalizeWords("js string exercises")); // "Js String Exercises"
```

- Write a function that takes a string which has lower and upper case letters as a parameter and converts upper case letters to lower case, and lower case letters to upper case.

```js
/* Requirements
  @name swapcase
  @parameter (string) text
  @return String
*/

function swapcase(text) {

  let lowerArr = ["abcdefghijklmnopqrstuvwxyz"]
    let upperArr = ["ABCDEFGHIJKLMNOPQRSTUVWXYZ"]
    

  for (letter of text) {
    let final = [];
    if (lowerArr.indexOf(letter) >= 0) {
      final.push(letter.toUpperCase())
    }
    else if (upperArr.indexOf(letter) >= 0)
      final.push(letter.toLowerCase())
  }
  return final.join("");

}

// Tets
console.log(swapcase("AaBbc")); // "aAbBC"
```

- Write a function to convert a string into camel case.

Example:

```js
/* Requirements
  @name camelize
  @parameter (string) text
  @return String
*/

function camelize(text) {

  let WordsArr = text.split(" ");
  let ans = [];
  for (word of wordsArr) {
    let letterArr = word.split("")
    let cap = letterArr[0].toUpperCase()
    letterArr.shift();
    letterArr.unshift(cap);
    let wordDone = letterArr.join("");
    ans.push(wordDone);
  }
  return ans.join("")
 
}


// Test
console.log(camelize("JavaScript Exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScript exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScriptExercises")); // "JavaScriptExercises"
```

- Write a function to uncamelize a string. Example:

```js
/* Requirements
  @name uncamelize
  @parameter (string, string) text, joinStr
  @return String
*/

function uncamelize(text, joiner) {
let caps = [];
let arr = text.split("");
for (let char of arr) {
  if(char === char.toUpperCase()) {
    caps.push(arr.indexOf(char))
  }
}
for (let cap of caps) {
  arr[cap] = arr[cap].toLowerCase();
  arr.splice(cap, 0, joiner);
}
return arr.join("");
 
}

// Tets
console.log(uncamelize("helloWorld", "_")); // "hello_world"
```

- Write a function to concatenates a given string n times (default is 1).

```js
/* Requirements
  @name repeat
  @parameter (string, number) text, times
  @return String
*/
function repeat(text, times = 1) {
  let ans = text;
  for (let i = 0; i < times; i++) {
    ans += text;
  }
  return ans;
}

// Test
console.log(repeat("Ha!", 3)); // "Ha!Ha!Ha!"
```

- Write a function to insert a string within a string at a particular position (default is 1).

```js
/* Requirements
  @name repeat
  @parameter (string, number) text, position
  @return String
*/
function repeat(text, add, position) {
  let arr = text.split("");
  arr.splice(position, 0, add);
  return arr.join("")
}

// Test
console.log(insert("We are doing some exercises.", "JavaScript ", 18)); // "We are doing some JavaScript exercises."
```

- Write a JavaScript function to humanized number (Formats a number to a human-readable string.) with the correct suffix such as 1st, 2nd, 3rd or 4th.

```js
/* Requirements
  @name humanize
  @parameter ( number) num
  @return String
*/
  function humanize(num) {

    
    let ans = "";
    if (num > 10 && num < 20) {
      ans = num + "th";
      }

    else {
     let lastNum = String(num)[String(num).length - 1]
     switch (Number(lastNum)) {
       case 1: ans = num + "st";
       break;
       case 2: ans = num + "nd";
       break;
       case 3: ans = num + "rd";
       break;
       default: ans = num + "th";
     }
    }
    return ans;
  }




// Test
console.log(humanize(301)); // "301st"
console.log(humanize(402)); // "402nd"
```

###

Write a function to truncates a string if it is longer than the specified number of characters. Truncated strings will end with a translatable ellipsis sequence ("…") (by default) or specified characters.

```js
/* Requirements
  @name testTruncate
  @parameter (string, number, string) text, len, postfix
  @return String
*/

function testTruncate(text, len, postfix) {
  text.padEnd(len, postfix);
}


// Test
console.log(textTruncate("We are doing JS string exercises.", 15, "!!")); //"We are doing !!"
```

- Write a JavaScript function to chop a string into chunks of a given length.

```js
/* Requirements
  @name chop
  @parameter (string, number) text, size
  @return String
*/
function chop(text, size) {
let arr = []
for (let i = 0; i < text.length; i+=2) {
	arr.push(text.substring(i, i+size))
}
return arr;
}

// Test
console.log(stringChop("hello world", 2)); // ["he", "ll", "o ", "wo", "rl", "d"]
```

- Write a function to count the occurrence of a substring in a string.

```js
/* Requirements
  @name count
  @parameter (string, string) text, char
  @return Number
*/
function count(text, char) {
  let counter = 0;
  let textArr = text.split(" ");
  for (let word of textArr) {
    if (word.toLowerCase() === char.toLowerCase()) {
      counter++;
    }
  }
	return counter;
}

// Test
console.log(count("The quick brown fox jumps over the lazy dog", "the")); // 2
```

- Write a function to strip leading and trailing spaces from a string.

```js
/* Requirements
  @name strip
  @parameter (string) text
  @return String
*/

function strip(text) {
  return text.trim();
}

// Test
console.log(strip("   Hello World ")); // "Hello World"
```

- Write a JavaScript function to truncate a string to a certain number of words.

```js
/* Requirements
  @name chopWords
  @parameter (string, number) text, words
  @return String
*/

function chopWords(text, words) {
  let arr = string.split(" ");
  return arr.slice(0, words).join(" ");
}

// Test
console.log(chopWords("The quick brown fox jumps over the lazy dog", 4)); // "The quick brown fox"
```

- Write a function to alphabetize a given string.(A - z)

```js
/* Requirements
  @name alphabetize
  @parameter (string, number) text, times
  @return String
*/

function alphabetize(text) {
  text.split("").sort().join();
}

// Test
console.log(alphabetize("United States")); // 'SUadeeinsttt'
```
