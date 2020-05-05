# String Methods

## Practice String Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (4-5 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.

Example:

1. `charAt`

   - This method accepts one parameter (index) of number data type.
   - It returns the charater on specific index (provided through parameter)
   - Example:
     ```js
     let name = "Arya Stark";
     name.charAt(2); //"y"
     let sentance = "A quick brown fox jumped over a lazy dog";
     sentance.charAt(4); // "i"
     let houseName = "Starks";
     houseName.charAt(0); // "S"
     ```
   - `charAt` accepts a index (number data type) and return the character on that index.

2. `toUpperCase`

   - This method works on the string to convert all characters of the string to uppercase, and returns the new string. Any non string values are converted to string while using them with this method.
   - Example:
     ```js
     let name = "Arya Stark";
     name.toUpperCase(); //"ARYA STARK"
     let sentence = "A quick brown fox jumped over a lazy dog";
     sentence.toUpperCase(); // "A QUICK BROWN FOX JUMPED OVER A LAZY DOG"
     let houseName = "Starks";
     houseName.toUpperCase(); // "STARKS"
     ```
3. `toLowerCase`

   - This method works on the string to convert all characters of the string to lowercase, and returns the new string. Any non string values are converted to string while using them with this method.
   - Example:
     ```js
     let name = "Arya Stark";
     name.toLowerCase(); //"arya stark"
     let sentence = "A quick brown fox jumped over a lazy dog";
     sentence.toLowerCase(); // "a quick brown fox jumped over a lazy dog"
     let houseName = "Starks";
     houseName.toLowerCase(); // "starks"
     ```
4. `trim`

   - This method works on the string to remove all white spaces from both sides of the text in the string, and returns the new string. It removes blank spaces, tabs, indentations and line breaks from both ends.
   - Example:
     ```js
     let name = "  Arya Stark  ";
     name.trim(); //"Arya Stark"
     let sentence = "  A quick brown fox jumped over a lazy dog                 ";
     sentence.trim(); // "A quick brown fox jumped over a lazy dog"
     let houseName = "  Starks  ";
     houseName.trim(); // "Starks"
     ```

5. `trimEnd`

   - This method works on the string to remove all white spaces the end of the string, and returns the new string. It removes blank spaces, tabs, indentations and line breaks from the right end, or after the text in the string. It is similar to trimRight() in it's working.
   - Example:
     ```js
     let name = "  Arya Stark  ";
     name.trimEnd(); //"  Arya Stark"
     let sentence = "  A quick brown fox jumped over a lazy dog                 ";
     sentence.trimEnd(); // "  A quick brown fox jumped over a lazy dog"
     let houseName = "Starks  ";
     houseName.trimEnd(); // "Starks"
     ```

6. `trimStart`

   - This method works on the string to remove all white spaces from the start of the string, and returns the new string. It removes blank spaces, tabs, indentations and line breaks from the left side, or before the text of the string, opposite in it's working to the above. It's similar in it's working to trimLeft()
   - Example:
     ```js
     let name = "  Arya Stark  ";
     name.trimStart(); //"Arya Stark   "
     let sentence = "  A quick brown fox jumped over a lazy dog          ";
     sentence.trimStart(); // "A quick brown fox jumped over a lazy dog          "
     let houseName = "  Starks  ";
     houseName.trimStart(); // "Starks  "
     ```
7. `concat`

   - This method can accept n number of parameters of string type. It works on the string it is applied to, and concatenates the strings in the arguments to the string. In other words, it adds the argument strings to the end of the string the function is applied to.
   - Example:
     ```js
     let name = "Arya Stark";
     name.concat(" is", " a legend"); //"Arya Stark is a legend"
     let sentence = "A quick brown fox";
     sentence.concat(" jumped over a lazy dog"); // "A quick brown fox jumped over a lazy dog"
     let houseName = "Starks";
     houseName.concat(" "); // "Starks "
     ```
8. `endsWith`

   - This method can accept as argument two values, the first being a string and the secod (optional) being a number which is taken as the length of the string t consider for this method. The number defaults to the length of the string if not specified. When applied to a string, it checks if the string it is applied to ends with the string in the argument, and returns tru or false depending on whether it matches the ending. 
   - Example:
     ```js
     let name = "Arya Stark";
     name.endsWith("k"); //true
     let sentence = "A quick brown fox";
     sentence.endsWith("brown", 13); // true
     let houseName = "Starks";
     houseName.endsWith("k"); // false
    ```


9. `includes`

   - This method can accept as argument two values, the first being a string and the secod (optional) being a number which is taken as the index position to start checking from. The number defaults to 0 if not specified. When applied to a string, it checks if the string it is applied to includes/contains the string in the argument, and returns true or false depending on whether it includes the specified string. 
   - Example:
     ```js
     let name = "Arya Stark";
     name.includes("k"); //true
     let sentence = "A quick brown fox";
     sentence.includes("brown", 15); // false
     let houseName = "Starks";
     houseName.contains("k", 3); // true
     ```
10. `indexOf`

   - This method can accept as argument two values, the first being a string and the secod (optional) being a number which is taken as the index position in the string to start checking from. When applied to a string, it checks if the string it is applied to contains the string in the argument, and returns the index position of the first instance of the argument string, if found. If it is not found, it returns -1. By default, the number part of the argument is 0 if not manually specified. 
   - Example:
     ```js
     let name = "Arya Stark";
     name.indexOf("k"); //9
     let sentence = "A quick brown fox";
     sentence.indexOf("brown", 13); // -1
     let houseName = "starks";
     houseName.indexOf("s"); // 0
     ```

11. `lastIndexOf`

   - Similar to the above method, this returns the index position of the last instance of the specified string. The arguments, defaults and return values being the same as above.
   - Example:
     ```js
     let name = "Arya Stark";
     name.lastIndexOf("a"); //7
     let sentence = "A quick brown fox";
     sentence.lastIndexOf("brown", 3); // 8
     let houseName = "Starks";
     houseName.lastIndexOf("k"); // 4
     ```

12. `padEnd`

   - Accepts two arguments, one being a number specifying the target/desired length of the padded string, and the other argument being a string, which is the text to be used for padding. This method adds the padding text from the argument to the end of the string to bring the total string length to the desired ength (specifid in first argument). The default value for the padding string is " ". 
   - Example:
     ```js
     let name = "Arya Stark";
     name.padEnd(15, "_"); // "Arya Stark_____"
     let sentence = "A quick brown fox";
     sentence.padEnd("21", "ba"); // "A quick brown foxbaba"
     let houseName = "Starks";
     houseName.padEnd(10, "k"); // "Starkskkkk"
     ```

13. `padStart`

   - Same as the above, except that the padding is applied to the start of the string, and not the end. 
   - Example:
     ```js
     let name = "Arya Stark";
     name.padStart(15, "_"); // "_____Arya Stark"
     let sentence = "A quick brown fox";
     sentence.padStart("21", "ba"); // "babaA quick brown fox"
     let houseName = "Starks";
     houseName.padStart(10, "k"); // "kkkkStarks" 
     ```

14. `repeat`

   - This ethod accepts one argument of number type, and returns a new string type value. It takes the string it is applied to and repeats it the number of times specified in the argument to the method, concatenating each repeated string to the end of the original string.
   - Example:
     ```js
     let name = "arya";
     name.padStart(0); // ""
     let sentence = "no";
     sentence.padStart(2); // "nono"
     let houseName = "pingu";
     houseName.padStart(1); // "pingu" 
     ```


15. `replace`

UNDERSTAND regEx


16. `slice`

   - Accepts two arguments of number type. THe first argument specifies the start position and second (optional | defaults to full string length) specifies the end position. It returns the part of the string specified according to the arguments given to the method. 
   - Example:
     ```js
     let name = "Arya Stark";
     name.slice(1); // "rya Stark"
     let sentence = "A quick brown fox";
     sentence.slice(2, 6); // "quic"
     let houseName = "Starks";
     houseName.slice(1, -2); // "tar" 
     ```

17. `split`

   -Accepts two arguments, first being a string and second (optional being a non negative number). When applied to a string, it looks for the first argument in the string and splits it at every occurence of the specified argument string and returns an array with all separated items. THe second argument specifies the limit, or the max number of items that should be contained in the array. Once the array has these many values, the method stops.

      - Example:
     ```js
     let name = "Arya Stark";
     name.split(" "); // ["Arya", "Stark"]
     let sentence = "quick";
     sentence.split("", 3); // ["q", "u", "i"]
     let houseName = "Starks";
     houseName.split(s); // ["Stark", ""] 
     ```


18. `substring`


   - THis method, when applied to a string, returns the part of the string beginning and ending with the index position numbers specified in the arguments. It accepts two arguments of number type, the second being optional (defaults to end of string).

      - Example:
     ```js
     let name = "Arya Stark";
     name.substring(1, 3); // "ra"
     let sentence = "quick";
     sentence.substring(0, 4); // "quic"
     let houseName = "Starks";
     houseName.substring(3); // "rk"
     ```


## writeCode

Using above methods you practiced above, do the following.

```js
let from = "Syrio Forel";
let quote = "There is only one thing we say to death: Not today";
let to = "Arya Stark";

/*
1. Find the index of the first 'is' in the variable quote. And store it in a new variable named indexOfIs
*/
let indexOfIs = quote.indexOf("is");

/*
2. Find the character at, the index indexOfIs (Problem 1) in quote.
*/
quote.charAt(indexOfIs);

/*
3. Log the message saying `The index of first is in quote is 7`
*/
console.log("The index of first is in quote is " + indexOfIs)

/*
4. Log the message for first 6 characters of quote like this.
The character at index 0 is 'T'
The character at index 1 is 'h'
The character at index 2 is 'e'
The character at index 3 is 'r'
The character at index 4 is 'e'
The character at index 5 is ' '
*/
for (let i=0; i<6; i++) {
  console.log("THe character at index " + i + " is " + quote.charAt(i));
}

/*
5. Using the variable from , to and quote variable dispaly this message
"Syrio Forel said There is only one thing we say to death: Not today to Arya Stark." (use concat method)
*/

console.log(from.concat(" said ", quote, " to ", to));

/*
6. Does from, to and quote ends with "rk". Check all three.
*/

from.endsWith("rk");
quote.endsWith("rk");
to.endsWith("rk");

/*
7. Does quote includes the word "Only"
*/

quote.includes("Only");

/*
8. Does quote includes the word " we"
*/

quote.includes("we");

/*
9. Find the index of the the word `we` in quote
*/

quote.indexOf("we");

/*
10. Split the quote into individual word and store it in a variable name quoteSplitted
*/

let quoteSplitted = quote.split(" ");


/*
11. Change the word "today" in quoteSplitted to "tomorrow" and join all the words to form a sentance.
*/

ARRAY METHOD!


/*
12. Find the index of second "o" in quote. Use indexOf
*/

let pos = quote.indexOf("o");
let secondPos = quote.indexOf("o", pos + 1);

/*
13. Find the last index of letter "a" in quote.
*/quote.lastIndexOf("a");



/*
14. Find the second last index of letter "a" in quote.
*/

let pos = quote.lastIndexOf("a");
let secondPos = quote.lastIndexOf("a", pos - 1);

/*
15. Make the quote 70 character long. If it has less characters add rest as .......
Example: "Hello" (convert to 10 characters) => "Hello....."
*/

quote.padEnd(70, ".");

/*
16. Do same as (15) but the ... should come in start.
*/

quote.padStart(70, ".");

/*
17. Log the repeat of "Hello World!" 10 times.
*/

console.log("Hello World".repeat(10));


/*
18. Replace today to tomorrow in quote.
*/

quote.replace("today", "tomorrow");

/*
19. Replace Stark to Lannister in quoteTo
*/

to.replace("Stark", "Lannister");

/*
20. Make the quote of length 30 and put ... at the end. (use slice)
*/

quote.slice()

UNCLEAR

/*
21. Find out does quote, quoteFrom, quoteTo starts with "A"
*/

quote.startsWith("A");
to.startsWith("A");
from.startsWith("A");


```

## Practice Array Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (2-3 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.
6. Does it mutate the original value (check https://doesitmutate.xyz)

Example:

1. `concat`

   - n(any) number of values (number, string, boolean, array, null, undefined, object and function.)
   - It returns a single Array consisting of by all the values passed as parameters in the same order.
   - Example:
     ```js
     let numbers = [1, 2, 3];
     numbers.concat(4); //[1,2,3,4]
     let sentanceArray = "A quick brown fox jumped over a lazy".split(" ");
     sentanceArray.concat("dog").join(" "); //"A quick brown fox jumped over a lazy dog"
     let colors = ["red", "green", "blue"];
     colors.concat("black", "red", 21, true); // ['red','green','blue','black', 'red', 21, true]
     ```
   - `concat` accepts n number of values and returns one array with all the values in same order. It doesnot change the original array.
   - No it doesnot mutate the original array

2. `join`

   - Accepts one parameter (optional) that specifies the separating character to be used. This method takes all the items in the array that it is applied to and concatenates them, and returns a string. If no concatenating/separating characer is specified in the argument, the method uses ',' be default as a separator.
   - Example:
     ```js
     let numbers = [1, 2, 3];
     numbers.join(); //"1,2,3,4"
     let myArray = ["a", "b", "c", "d"];
     myArray.join("dog") //"Adogbdogcdogd"
     let colors = ["red", "green", "blue"];
     colors.join(" "); // 'red green blue'
     ```


3. `flat`

    - The flat method removes nested arrays from within the array it is applied to and adds their items to the parent array and returns this result as a new array. It accepts one optional argument (default 1) that specifies how many levels of nested arrays this method will apply to or affect.
    - Example:
    ```js
    let numbers = [1, 2, 3, [4, 5]];
     numbers.flat(); //[1, 2, 3, 4, 5]
     let myArray = ["a", "b", ["c", ["d"]]];
     myArray.flat() //["a", "b", "c", ["d"]]
     let colors = ["a", "b", ["c", ["d"]]];
     colors.flat(2); //["a", "b", "c", "d"]
    ```
4. `push`

    - This method adds an element(accepted as argument) to the end of the array it is applied to, and returns the new length of the array. It can accept any number of arguments, and will add them all, in order, at the end of the array.
    - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.push(6); //returns 6. Array set to [1, 2, 3, 4, 5, 6]
     let myArray = ["a", "b", "c", "d"];
     myArray.push("e", "f") //returns 6. Array : ["a", "b", "c", "d", "e", "f"]
     let colors = ["a", "b", ["c", ["d"]]];
     colors.push(2); //returns 4. Array : ["a", "b", ["c", ["d"]], 6]
    ```

5. `indexOf`

    - Accepts two arguments, the first being the element it needs to check the index of, and the second (optional) being the index to start searching from, defaults to 0. This method, when applied to an array, checks if the element specified in the argument exists in the array, and if it does, returns the index position of the first instance of that element. If the element does not exist, it returns -1.

      - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.indexOf(3); //returns 2
     let myArray = ["a", "b", "c", "d"];
     myArray.indexOf("b", 2) //returns -1
     let colors = ["a", "b", "c", "d"];
     colors.indexOf("b", 1); //returns 1
    ```


6. `lastIndexOf`

    - Similar to IndexOf, except that it returns the last instance of the element, and not the first. This method starts searching from the end of the array, backwards, and returns the first instace it finds while moving backwards. Accepts two arguments: 1) element to check for. 2) Index position to start looking backwards from.

      - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.lastIndexOf(3); //returns 2
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.lastIndexOf("b", 2) //returns 1
     let colors = ["a", "b", "c", "b", "d"];
     colors.lastIndexOf("b"); //returns 3
    ```


7. `includes`

    - Checks if the element specified as the first argument exists as an element within the array, and returns true or false depending on if it does. The second argument (optional | default : 0) specifies what index position to start searching from within the array.

          - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.includes(3); //returns true
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.includes("b", 2) //returns true
     let colors = ["a", "b", "c", "b", "d"];
     colors.includes("b", 4); //returns false
    ```

8. `reverse`

    - Does not take arguments, and reverses the order of the elements in the array it is applied to, making the first element shift to the last, the second to second-last and so on. Returns the reversed array.

              - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.reverse(); //returns [5, 4, 3, 2, 1]
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.reverse() //returns ["d", "b", "c", "b", "a"]
     let colors = ["a", "b", "c", "b", "d"];
     colors.reverse(; //returns ["d", "b", "c", "b", "a"]
    ```

9. `every`

    - This method works on an array, taking a callback function as an argument, and checking if the condition of the callback function is satisfied by each element in the array. If every element on of the array satisfies the condition, the method returns true. If it finds even one value that returns false against the condition in the argument, the method returns false.

              - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.every(x => x>=1); //returns true
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.every(x => x === "a") //returns false
     let colors = ["a", "b", "c", "b", "d"];
     colors.every(x => x === "a"); //returns false
    ```

10. `shift`

    - Removes first element from the array it is applied to and returns the removed element.

              - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.shift(); //returns 1
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.shift() //returns "a"
     let colors = ["b", "c", "b", "d"];
     colors.shift(); //returns "b"
    ```


11. `splice`

    - This method is used to remove and/or replace items from an array. It accepts three arguments : 1) Index to start working from. 2) THe number of elements to delete, starting from the index in argument 1 (optional | default: 0). 3) The elements to add into the array, starting from the index position specified in argument 1 (optional | default: will not add any elements). This method returns an array of deleted elements. If no elements are deleted, it will return an empty array.

              - Example:
    ```js
    let numbers = [1, 2, 3, 4, 5];
     numbers.splice(2, 1, "added"); //returns [3]
     let myArray = ["a", "b", "c", "b", "d"];
     myArray.splice(2, "add") //returns ["c", "b", "d"]
     let colors = ["b", "c", "b", "d"];
     colors.splice(1, 0); //returns []
    ```


12. `find`

    -       


13. `unshift`

    - Adds the element(s) specified in argument at the beginning of the array and returns the new length of the array. Accepts any number of arguments and adds them in order at the start of the array.

14. `findIndex`

    - callback

15. `filter`

    - THis method accepts a condition/function as an argument, and calls that function with each element of the array it is applied to. The funciton/condition should return true or false, and all values that result in true will be added to a new array and returned. 

16. `forEach`

    - This method accepts a callback function as an argument, and applies that callback function with each element of the array. This funciton does not return anything, merely calls the function on each element of the array it is applied to.

17. `map`

    - This method accepts a callback function as argument, calls the function with each element of the array it is applied to, and returns a new array with the elements after the function has been called on them. Difference being that forEach returns undefined, always, while map returns a ew array. 

18. `pop`

    - THis method removes an item from the end of the array it is applied to and returns the removed element. 

29. `reduce`

    - callback

20. `slice`

    -THis method accepts two arguments, specifying the start and end index positions to slice out from the array. THe first argument, specifying the start position, defaults to 0, and specifies which element to take as the first for the returned array. The second argument, defaulting to the length of the array, specifies till which position the in the array should the method slice. This method returns a new array from the startIndex (arg 1) (included) till the lastIndex (arg2) (not included) from the array it is applied to.


21. `some`

    - This method accepts a callback function as an argument, applies it to each element in the array. If any element returns true when passed to the callback function, the method returns tru. If no "true" value is received as a return value, the method returns false. 

## writeCode

Using above methods you practiced above, do the following.

```js
// Use the below two arrays and practice array methods
var numbers = [1, 12, 4, 18, 9, 7, 11, 3, 101, 5, 6, 9];
var strings = ["This", "is", "a", "collection", "of", "words"];

// - Find the index of `101` in numbers

numbers.indexOf(101);

// - Find the last index of `9` in numbers

numberslastIndexOf(9);

// - Convert value of strings array into a sentance like "This is a collection of words"

strings.join(" ");

// - Add two new words in the strings array "called" and "sentence"

strings.push("called", "sentence");

// - Again convert the updated array (strings) into sentance like "This is a collection of words called sentance"

strings.join(" ");

// - Remove the first word in the array (strings)

strings.shift();

// - Find all the words that contain 'is' use string method 'includes'

let arr = [];
for (word of strings) {
  if (word.includes("is")) {
    arr.push(word);
  }
}

// - Find all the words that contain 'is' use string method 'indexOf'

let arr = [];
function checkIs(word) {
  if (word.includes("is")) {
    arr.push(word);
  }
}

strings.forEach(checkIs);

// - Check if all the numbers in numbers array are divisible by three use array method (every)

numbers.every( n => ((n % 3) == 0));

// -  Sort Array from smallest to largest

function compareNumbers(a, b) {
  return a - b;
}
numbers.sort(compareNumbers);


// - Remove the last word in strings

strings.pop();

// - Find largest number in numbers

(numbers.sort(compareNumbers)).pop();

// - Find longest string in strings

function compareString(a, b) {
  return a.length - b.length;
}
strings.sort(compareString);

// - Find all the even numbers

numbers.filter(x => x % 2 == 0);

// - Find all the odd numbers

numbers.filter(x => x % 2 != 0);

// - Place a new word at the start of the array use (unshift)

strings.unshift("word");

// - Make a subset of numbers array [18,9,7,11]

numbers.slice(3, 7);

// - Make a subset of strings array ['a','collection']

strings.slice(2, 4)

// - Replace 12 & 18 with 1221 and 1881

numbers.splice(1, 1, 1221)
numbers.splice(3, 1, 1881)


// - Replace words in strings array with the length of the word

function replace(word) {
  let l = word.length;
  word = l;
}

strings.forEach(replace);

// - Find the sum of the length of words using above question

let sum = 0;
function addUp(word) {
  sum += word.length;
}

strings.forEach(addUp);


// - Customers Array
var customers = [
  { firstname: "Joe", lastname: "Blogs" },
  { firstname: "John", lastname: "Smith" },
  { firstname: "Dave", lastname: "Jones" },
  { firstname: "Jack", lastname: "White" }
];
// - Find all customers whose firstname starts with 'J'

let newArr = []
customers.filter(x => {x.firstname.startsWith("J")})

// - Create new array with only first name

newArr = []
customers.forEach(x => newArr.push(x.firstname))

// - Create new array with all the full names (ex: "Joe Blogs")

newArr = []
customers.forEach(x => {
  if ((x.firstname != Joe) && (x.lastname != "Blogs")) {
    newArr.push(x.firstname + " " + x.lastname)
  }
}
)


// - Sort the array created above alphabetically

SORT NETHOD NOT CLEAR

// - Create a new array that contains only user who has at least one vowel in the firstname.

let newArr = [];
let vowels = ["a", "e", "i", "o", "u"];
customers.forEach(x => {
  let name = x.firstname.toLowerCase();
  for (let letter of name) {
    if vowels.includes(letter) {
      newArr.push(x);
      break;
    }
  }
} )


UNCLEAR

```
