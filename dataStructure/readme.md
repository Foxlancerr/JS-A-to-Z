# Basic Data Structures

Data can be stored and accessed in many ways. You already know some common JavaScript data structures — arrays and objects.

In this Basic Data Structures course, you'll learn more about the differences between arrays and objects, and which to use in different situations. You'll also learn how to use helpful JS methods like splice() and Object.keys() to access and manipulate data.

# Total Lessons (33)

# 1-Use an Array to Store a Collection of Data

The below is an example of the simplest implementation of an array data structure. This is known as a one-dimensional array, meaning it only has one level, or that it does not have any other arrays nested within it. Notice it contains booleans, strings, and numbers, among other valid JavaScript data types:

```js
let simpleArray = ['one', 2, 'three', true, false, undefined, null];
console.log(simpleArray.length);
The console.log call displays 7.
```

All arrays have a length property, which as shown above, can be very easily accessed with the syntax Array.length. A more complex implementation of an array can be seen below. This is known as a multi-dimensional array, or an array that contains other arrays. Notice that this array also contains JavaScript objects, which we will examine very closely in our next section, but for now, all you need to know is that arrays are also capable of storing complex objects.

```js
let complexArray = [
  [
    {
      one: 1,
      two: 2,
    },
    {
      three: 3,
      four: 4,
    },
  ],
  [
    {
      a: "a",
      b: "b",
    },
    {
      c: "c",
      d: "d",
    },
  ],
];
```

### Task

We have defined a variable called yourArray. Complete the statement by assigning an array of at least 5 elements in length to the yourArray variable. Your array should contain at least one string, one number, and one boolean.

### Solution

```js
let yourArray; // Change this line
yourArray = ["ahmad", 34, true, "Bscs", "5th"];
```

# 2-Access an Array's Contents Using Bracket Notation

The fundamental feature of any data structure is, of course, the ability to not only store data, but to be able to retrieve that data on command. So, now that we've learned how to create an array, let's begin to think about how we can access that array's information.

When we define a simple array as seen below, there are 3 items in it:

```js
let ourArray = ["a", "b", "c"];
```

In an array, each array item has an index. This index doubles as the position of that item in the array, and how you reference it.

However, it is important to note, that JavaScript arrays are zero-indexed, meaning that the first element of an array is actually at the zeroth position, not the first.

In order to retrieve an element from an array we can enclose an index in brackets and append it to the end of an array, or more commonly, to a variable which references an array object.

This is known as bracket notation. For example, if we want to retrieve the a from ourArray and assign it to a variable, we can do so with the following code:

```js
let ourVariable = ourArray[0];
```

Now ourVariable has the value of a.

In addition to accessing the value associated with an index, you can also set an index to a value using the same notation:

```js
ourArray[1] = "not b anymore";
```

Using bracket notation, we have now reset the item at index 1 from the string b, to not b anymore. Now ourArray is ["a", "not b anymore", "c"].

### Task

In order to complete this challenge, set the 2nd position (index 1) of myArray to anything you want, besides the letter b.

### Solution

```js
let myArray = ["a", "b", "c", "d"];
// Only change code below this line
myArray[1] = "Something added";
// Only change code above this line
console.log(myArray);
```

# 3-Add Items to an Array with push() and unshift()

An array's length, like the data types it can contain, is not fixed. Arrays can be defined with a length of any number of elements, and elements can be added or removed over time; in other words, arrays are mutable.

In this challenge, we will look at two methods with which we can programmatically modify an array:

1. Array.push()
2. Array.unshift().

Both methods take one or more elements as parameters and add those elements to the array the method is being called on; the push() method adds elements to the end of an array, and unshift() adds elements to the beginning. Consider the following:

```js
let twentyThree = "XXIII";
let romanNumerals = ["XXI", "XXII"];

romanNumerals.unshift("XIX", "XX");
```

romanNumerals would have the value ['XIX', 'XX', 'XXI', 'XXII'].

```js
romanNumerals.push(twentyThree);
```

    romanNumerals would have the value ['XIX', 'XX', 'XXI', 'XXII', 'XXIII'].

    Notice that we can also pass variables, which allows us even greater flexibility in dynamically modifying our array's data.

### Task

We have defined a function, mixedNumbers, which we are passing an array as an argument. Modify the function by using push() and unshift() to add 'I', 2, 'three' to the beginning of the array and 7, 'VIII', 9 to the end so that the returned array contains representations of the numbers 1-9 in order.

### Solution

```js
function mixedNumbers(arr) {
  // Only change code below this line
  arr.unshift("I", 2, "three");
  arr.push(7, "VIII", 9);
  // Only change code above this line
  return arr;
}

console.log(mixedNumbers(["IV", 5, "six"]));
```

# 4-Remove Items from an Array with pop() and shift()

Both push() and unshift() have corresponding methods that are nearly functional opposites:

1. pop()
2. shift().

As you may have guessed by now, instead of adding,

    pop() removes an element from the end of an array, while shift() removes an element from the beginning.

    The key difference between pop() and shift() and their cousins push() and unshift(), is that neither method takes parameters, and each only allows an array to be modified by a single element at a time.

Let's take a look:

```js
let greetings = ["whats up?", "hello", "see ya!"];
```

```js
greetings.pop();
```

greetings would have the value ['whats up?', 'hello'].

```js
greetings.shift();
```

greetings would have the value ['hello'].

We can also return the value of the removed element with either method like this:

```js
let popped = greetings.pop();
```

greetings would have the value [], and popped would have the value hello.

### Task

We have defined a function, popShift, which takes an array as an argument and returns a new array. Modify the function, using pop() and shift(), to remove the first and last elements of the argument array, and assign the removed elements to their corresponding variables, so that the returned array contains their values.

### Solution

```js
function popShift(arr) {
  let popped = arr.pop(); // Change this line
  let shifted = arr.shift(); // Change this line
  return [shifted, popped];
}

console.log(popShift(["challenge", "is", "not", "complete"]));
```

# 5-Remove Items Using splice()

Ok, so we've learned how to remove elements from the beginning and end of arrays using shift() and pop(),

    but what if we want to remove an element from somewhere in the middle? Or remove more than one element at once? Well, that's where splice() comes in.

    splice() allows us to do just that: remove any number of consecutive elements from anywhere in an array.

splice() can take up to 3 parameters,

but for now, we'll focus on just the first 2.The first two parameters of splice() are integers which represent indexes, or positions, of items in the array that splice() is being called upon. And remember, arrays are zero-indexed, so to indicate the first element of an array, we would use 0. splice()'s first parameter represents the index on the array from which to begin removing elements, while the second parameter indicates the number of elements to delete. For example:

```js
let array = ["today", "was", "not", "so", "great"];

array.splice(2, 2);
```

Here we remove 2 elements, beginning with the third element (at index 2). array would have the value ['today', 'was', 'great'].

splice() not only modifies the array it's being called on, but it also returns a new array containing the value of the removed elements:

```js
let array = ['I', 'am', 'feeling', 'really', 'happy'];

let newArray = array.splice(3, 2);
newArray has the value ['really', 'happy'].
```

### Task

We've initialized an array arr. Use splice() to remove elements from arr, so that it only contains elements that sum to the value of 10.

### Solution

```js
const arr = [2, 4, 5, 1, 7, 5, 2, 1];
// Only change code below this line
const newarr = arr.splice(1, 4);
// Only change code above this line
console.log(arr);
```

# 6-Add Items Using splice()

Remember in the last challenge we mentioned that splice() can take up to three parameters? Well, you can use the third parameter, comprised of one or more element(s), to add to the array. This can be incredibly useful for quickly switching out an element, or a set of elements, for another.

```js
const numbers = [10, 11, 12, 12, 15];
const startIndex = 3;
const amountToDelete = 1;

numbers.splice(startIndex, amountToDelete, 13, 14);
console.log(numbers);
```

The second occurrence of 12 is removed, and we add 13 and 14 at the same index. The numbers array would now be [ 10, 11, 12, 13, 14, 15 ].

Here, we begin with an array of numbers. Then, we pass the following to splice(): The index at which to begin deleting elements (3), the number of elements to be deleted (1), and the remaining arguments (13, 14) will be inserted starting at that same index. Note that there can be any number of elements (separated by commas) following amountToDelete, each of which gets inserted.

### Task

We have defined a function, htmlColorNames, which takes an array of HTML colors as an argument. Modify the function using splice() to remove the first two elements of the array and add 'DarkSalmon' and 'BlanchedAlmond' in their respective places.

### Solution

```js
function htmlColorNames(arr) {
  // Only change code below this line
  arr.splice(0, 2, "DarkSalmon", "BlanchedAlmond");
  // Only change code above this line
  return arr;
}

console.log(
  htmlColorNames([
    "DarkGoldenRod",
    "WhiteSmoke",
    "LavenderBlush",
    "PaleTurquoise",
    "FireBrick",
  ])
);
```

# 7-Copy Array Items Using slice()

The next method we will cover is slice(). Rather than modifying an array,

slice() copies or extracts a given number of elements to a new array, leaving the array it is called upon untouched.

    slice() takes only 2 parameters
    1.  the first is the index at which to begin extraction,
    2. and the second is the index at which to stop extraction (extraction will occur up to, but not including the element at this index). Consider this:

```js
let weatherConditions = ["rain", "snow", "sleet", "hail", "clear"];

let todaysWeather = weatherConditions.slice(1, 3);
```

todaysWeather would have the value ['snow', 'sleet'], while weatherConditions would still have ['rain', 'snow', 'sleet', 'hail', 'clear'].

In effect, we have created a new array by extracting elements from an existing array.

### Task

1. We have defined a function, forecast, that takes an array as an argument. Modify the function using slice() to extract information from the argument array and return a new array that contains the string elements warm and sunny.

### Solution

```js
function forecast(arr) {
  // Only change code below this line
  arr = arr.slice(2, 4);
  return arr;
}

// Only change code above this line
console.log(
  forecast(["cold", "rainy", "warm", "sunny", "cool", "thunderstorms"])
);
```

# 8-Copy an Array with the Spread Operator

While slice() allows us to be selective about what elements of an array to copy, among several other useful tasks,

    ES6's new spread operator allows us to easily copy all of an array's elements,
    in order, with a simple and highly readable syntax.

    The spread syntax simply looks like this: ...

In practice, we can use the spread operator to copy an array like so:

```js
let thisArray = [true, true, undefined, false, null];
let thatArray = [...thisArray];
```

thatArray equals [true, true, undefined, false, null]. thisArray remains unchanged and thatArray contains the same elements as thisArray.

### Task

We have defined a function, copyMachine which takes arr (an array) and num (a number) as arguments. The function is supposed to return a new array made up of num copies of arr. We have done most of the work for you, but it doesn't work quite right yet. Modify the function using spread syntax so that it works correctly (hint: another method we have already covered might come in handy here!).

```js
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
    // Only change code below this line

    // Only change code above this line
    num--;
  }
  return newArr;
}

console.log(copyMachine([true, false, true], 2));
```

### Solution

```js
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
    // Only change code below this line
    newArr.push([...arr]);
    // Only change code above this line
    num--;
  }
  return newArr;
}

console.log(copyMachine([true, false, true], 2));
```

# 8-Combine Arrays with the Spread Operator

    Another huge advantage of the spread operator is the ability to combine arrays, or to insert all the elements of one array into another, at any index.

     With more traditional syntaxes, we can concatenate arrays, but this only allows us to combine arrays at the end of one, and at the start of another. Spread syntax makes the following operation extremely simple:

```js
let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];

let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
thatArray would have the value ['basil', 'cilantro', 'sage', 'rosemary', 'parsley', 'thyme', 'coriander'].
```

Using spread syntax, we have just achieved an operation that would have been more complex and more verbose had we used traditional methods.

### Task

We have defined a function spreadOut that returns the variable sentence. Modify the function using the spread operator so that it returns the array ['learning', 'to', 'code', 'is', 'fun'].

### Solution

```js
function spreadOut() {
  let fragment = ["to", "code"];
  let sentence = ["learning", ...fragment, "is", "fun"];
  return sentence;
}

console.log(spreadOut());
```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```

# 7-

### Task

```js

```

### Solution

```js

```