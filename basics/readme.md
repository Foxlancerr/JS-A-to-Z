# 01-Comment Your JavaScript Code

    Comments are lines of code that JavaScript will intentionally ignore. Comments are a great way to leave notes to yourself and to other people who will later need to figure out what that code does.

There are two ways to write comments in JavaScript:

### Single line comments

    Using // will tell JavaScript to ignore the remainder of the text on the current line. This is an in-line comment:

```js
const x = "js code";
// this is single line comments.
```

### Multi line comments

    You can make a multi-line comment beginning with /* and ending with */. This is a multi-line comment:

```js
const x = "js code";
/* this is multi-line comments.
   this is a multi-line comment
*/
```

### NOTE:

As you write code, you should regularly add comments to clarify the function of parts of your code. Good commenting can help communicate the intent of your code—both for others and for your future self.

<hr>
<hr>

# 02-Declare JavaScript Variables

    In computer science, data is anything that is meaningful to the computer. JavaScript provides eight different data types which are undefined, null, boolean, string, symbol, bigint, number, and object.

For example:

computers distinguish between numbers, such as the number 12, and strings, such as "12", "dog", or "123 cats", which are collections of characters. Computers can perform mathematical operations on a number, but not on a string.

    Variables allow computers to store and manipulate data in a dynamic fashion. They do this by using a "label" to point to the data rather than using the data itself. Any of the eight data types may be stored in a variable.

Variables are similar to the x and y variables you use in mathematics, which means they're a simple name to represent the data we want to refer to. Computer variables differ from mathematical variables in that they can store different values at different times.

We tell JavaScript to create or declare a variable by putting the keyword var in front of it, like so:

```js
var age;
var email = "test@example.com";
```

creates a variable called age. In JavaScript we end statements with semicolons. Variable names can be made up of numbers, letters, and $ or \_, but may not contain spaces or start with a number.

<hr>
<hr>

# 03-Storing Values with the Assignment Operator

    In JavaScript, you can store a value in a variable with the assignment operator (=).

```js
//This assigns the String value peshawar to city.
var city = "peshawar";
```

If there are any calculations to the right of the = operator, those are performed before the value is assigned to the variable on the left of the operator.

```js
var myVar;
myVar = 5;
```

First, this code creates a variable named myVar. Then, the code assigns 5 to myVar. Now, if myVar appears again in the code, the program will treat it as if it is 5.

<hr>
<hr>

# 04-Assigning the Value of One Variable to Another

After a value is assigned to a variable using the assignment operator, you can assign the value of that variable to another variable using the assignment operator.

```js
var myVar;
myVar = 5;
var myNum;
myNum = myVar;
```

The above declares a myVar variable with no value, then assigns it the value 5. Next, a variable named myNum is declared with no value. Then, the contents of myVar (which is 5) is assigned to the variable myNum. Now, myNum also has the value of 5.

<hr>
<hr>

# 05-Initializing Variables with the Assignment Operator

    It is common to initialize a variable to an initial value in the same line as it is declared.

```js
var marks = 40;
```

Creates a new variable called marks and assigns it an initial value of 40.

# 06-Declare String Variables

Previously you used the following code to declare a variable:

```js
var myName;
```

But you can also declare a string variable like this:

```js
var myName = "your name";
```

"your name" is called a string literal. A string literal, or string, is a series of zero or more characters enclosed in single or double quotes.

<hr>
<hr>

# 07-Understanding Uninitialized Variables

    When JavaScript variables are declared, they have an initial value of undefined. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a string of undefined.

```js
var a;
var b;
var c;

console.log(a);
console.log(b);
console.log(c);
```

<hr>
<hr>

# 08-Understanding Case Sensitivity in Variables

In JavaScript all variables and function names are case sensitive. This means that capitalization matters.

    MYVAR is not the same as MyVar nor myvar. It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.

### Best Practice

Write variable names in JavaScript in camelCase. In camelCase, multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized.

### Examples:

```js
var someVariable;
var anotherVariableName;
var thisVariableNameIsSoLong;
```

<hr>
<hr>

# 09-Explore Differences Between the var and let Keywords

    One of the biggest problems with declaring variables with the varkeyword is that you can easily overwrite variable declarations:

```js
var camper = "James";
var camper = "David";
console.log(camper);
```

In the code above, the camper variable is originally declared as James, and is then overridden to be David. The console then displays the string David.

In a small application, you might not run into this type of problem. But as your codebase becomes larger, you might accidentally overwrite a variable that you did not intend to. Because this behavior does not throw an error, searching for and fixing bugs becomes more difficult.

    A keyword called let was introduced in ES6, a major update to JavaScript, to solve this potential issue with the var keyword. You'll learn about other ES6 features in later challenges.

If you replace var with let in the code above, it results in an error:

```js
let camper = "James";
let camper = "David";
```

The error can be seen in your browser console.

So unlike var, when you use let, a variable with the same name can only be declared once.

<hr>
<hr>

# 10-Declare a Read-Only Variable with the const Keyword

    The keyword let is not the only new way to declare variables. In ES6, you can also declare variables using the const keyword.

    const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

The console will display an error due to reassigning the value of FAV_PET.

You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.

### Note:

It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays). You will learn more about objects, arrays, and immutable and mutable values in later challenges. Also in later challenges, you will see examples of uppercase, lowercase, or camelCase variable identifiers.

<hr>

# 11-Add Two Numbers with JavaScript

Number is a data type in JavaScript which represents numeric data.

Now let's try to add two numbers using JavaScript.

    JavaScript uses the + symbol as an addition operator when placed between two numbers.

Example:

```js
const myVar = 5 + 10;
```

myVar now has the value 15.

<hr>

# 12-Subtract One Number from Another with JavaScript

We can also subtract one number from another.

    JavaScript uses the - symbol for subtraction.

Example

```js
const myVar = 12 - 6;
```

myVar would have the value 6.

<hr>

# 13-Multiply Two Numbers with JavaScript

We can also multiply one number by another.

    JavaScript uses the * symbol for multiplication of two numbers.

Example

```js
const myVar = 13 * 13;
```

myVar would have the value 169.

<hr>

# 14-Divide One Number by Another with JavaScript

We can also divide one number by another.

    JavaScript uses the / symbol for division.

Example

```js
const myVar = 16 / 2;
```

myVar now has the value 8.

Change the 0 so that the quotient is equal to 2.

<hr>

# 15-Increment a Number with JavaScript

You can easily increment or add one to a variable with the ++ operator.

```js
i++;
// is the equivalent of
i = i + 1;
```

Note:

The entire line becomes i++;, eliminating the need for the equal sign.

<hr>

# 16-Decrement a Number with JavaScript

You can easily decrement or decrease a variable by one with the -- operator.

```js
i--;

// is the equivalent of
i = i - 1;
```

Note: The entire line becomes i--;, eliminating the need for the equal sign.

<hr>

# 17-Create Decimal Numbers with JavaScript

We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.

Note:

    when you compute numbers, they are computed with finite precision. Operations using floating points may lead to different results than the desired outcome. If you are getting one of these results, open a topic on the

<hr>

# 18-Multiply Two Decimals with JavaScript

In JavaScript, you can also perform calculations with decimal numbers, just like whole numbers.

Let's multiply two decimals together to get their product.

```js
const product = 2.0 * 4.6;
```

<hr>

# 19-Divide One Decimal by Another with JavaScript

Now let's divide one decimal by another.

```js
const divide = 10.0 / 2.2;
```

<hr>

# 20-Finding a Remainder in JavaScript

The remainder operator % gives the remainder of the division of two numbers.

Example

```js
5 % 2 = 1
5 / 2 = 2 //remainder 1
2 * 2 = 4
5 - 4 = 1
```

Usage

In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2. Even numbers have a remainder of 0, while odd numbers a remainder of 1.

```js
17 % 2 = 1
48 % 2 = 0
```

Note:

The remainder operator is sometimes incorrectly referred to as the modulus operator. It is very similar to modulus, but does not work properly with negative numbers.

<hr>

# 21-Compound Assignment With Augmented Addition

    In programming, it is common to use assignments to modify the contents of a variable. Remember that everything to the right of the equals sign is evaluated first, so we can say:

```js
myVar = myVar + 5;
```

to add 5 to myVar. Since this is such a common pattern, there are operators which do both a mathematical operation and assignment in one step.

    One such operator is the += operator.

```js
let myVar = 1;
myVar += 5;
console.log(myVar);
// 6 would be displayed in the console.
```

<hr>

# 22-Compound Assignment With Augmented Subtraction

Like the += operator, -= subtracts a number from a variable.

```js
myVar = myVar - 5;
```

will subtract 5 from myVar. This can be rewritten as:

```js
myVar -= 5;
```

# 23-Compound Assignment With Augmented Multiplication

The \*= operator multiplies a variable by a number.

```js
myVar = myVar * 5;
```

will multiply myVar by 5. This can be rewritten as:

```js
myVar *= 5;
```

<hr>

# 24-Compound Assignment With Augmented Division

The /= operator divides a variable by another number.

```js
myVar = myVar / 5;
```

Will divide myVar by 5. This can be rewritten as:

```js
myVar /= 5;
```

<hr>

# 25-Escaping Literal Quotes in Strings

When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: " or ' inside of your string?

    In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash (\) in front of the quote.

```js
const sampleStr = 'Alan said, "Peter is learning JavaScript".';

//without slash this will throw error
console.log('lets"s start');
```

This signals to JavaScript that the following quote is not the end of the string, but should instead appear inside the string. So if you were to print this to the console, you would get:

```js
Alan said, "Peter is learning JavaScript".
```

<hr>

# 26-Quoting Strings with Single Quotes

    String values in JavaScript may be written with single or double quotes, as long as you start and end with the same type of quote. Unlike some other programming languages, single and double quotes work the same in JavaScript.

```js
const doubleQuoteStr = "This is a string";
const singleQuoteStr = "This is also a string";
```

The reason why you might want to use one type of quote over the other is if you want to use both in a string. This might happen if you want to save a conversation in a string and have the conversation in quotes. Another use for it would be saving an \<a> tag with various attributes in quotes, all within a string.

```js
const conversation = 'Finn exclaims to Jake, "Algebraic!"';
```

However, this becomes a problem if you need to use the outermost quotes within it. Remember, a string has the same kind of quote at the beginning and end. But if you have that same quote somewhere in the middle, the string will stop early and throw an error.

```js
const goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"';
const badStr = 'Finn responds, "Let's go!"';
```

Here badStr will throw an error.

In the goodStr above, you can use both quotes safely by using the backslash \ as an escape character.

Note:

The backslash \ should not be confused with the forward slash /. They do not do the same thing.

<hr>

# 27-Escape Sequences in Strings

Quotes are not the only characters that can be escaped inside a string. Escape sequences allow you to use characters you may not otherwise be able to use in a string.

```js
Code	Output
\'	single quote
\"	double quote
\\	backslash
\n	newline
\t	tab
\r	carriage return
\b	backspace
\f	form feed
```

Note that the backslash itself must be escaped in order to display as a backslash.

```js
console.log("FirstLine\n\t\\SecondLine\nThirdLine")
// the output will look like

FirstLine
        \SecondLine
ThirdLine
```

<hr>

# 28-Concatenating Strings with Plus Operator

In JavaScript, when the + operator is used with a String value, it is called the concatenation operator. You can build a new string out of other strings by concatenating them together.

Example

```js
console.log("My name is Alan," + " I concatenate.");
```

Note: Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

```js
const ourStr = "I come first. " + "I come second.";
```

The string I come first. I come second. would be displayed in the console.

<hr>

# 29-Concatenating Strings with the Plus Equals Operator

We can also use the <code>+=</code> operator to concatenate a string onto the end of an existing string variable. This can be very helpful to break a long string over several lines.

Note:

Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

```js
let ourStr = "I come first. ";
ourStr += "I come second.";
```

ourStr now has a value of the string I come first. I come second..

Build myStr over several lines by concatenating these two strings:

    This is the first sentence. and This is the second sentence.

<hr>

# 30-Constructing Strings with Variables

    Sometimes you will need to build a string. By using the concatenation operator (+), you can insert one or more variables into a string you're building.

Example:

```js
const ourName = "Muhammad";
const ourStr = "Hello, My name is " + ourName + ", how are you?";
```

ourStr would have a value of the string Hello, our name is freeCodeCamp, how are you?.

<hr>

# 31-Appending Variables to Strings

    Just as we can build a string over multiple lines out of string literals, we can also append variables to a string using the plus equals (+=) operator.

Example:

```js
const anAdjective = "awesome!";
let ourStr = "what a catch ";
ourStr += anAdjective;

const someAdjective = "better way to boost your skill";
let myStr = "Learning to code is ";
myStr += someAdjective;
```

ourStr would have the value what a catch awesome!.

<hr>

# 32-Find the Length of a String

    You can find the length of a String value by writing .length after the string variable or string literal.

```js
console.log("Alan Peter".length);
```

The value 10 would be displayed in the console.

Note that the space character between "Alan" and "Peter" is also counted.

    For example, if we created a variable const firstName = "Ada", we could find out how long the string Ada is by using the firstName.length property.

<hr>

# 33-Use Bracket Notation to Find the First Character in a String

    Bracket notation is a way to get a character at a specific index within a string.

Most modern programming languages, like JavaScript, don't start counting at 1 like humans do. They start at 0. This is referred to as Zero-based indexing.

    For example, the character at index 0 in the word Charles is C. So if const firstName = "Charles", you can get the value of the first letter of the string by using firstName[0].

Example:

```js
const firstName = "Charles";
console.log(firstName[0]);
console.log(firstName[1]);
console.log(firstName[2]);
```

The output is look like

```
C
h
a
```

<hr>

# 34-Understand String Immutability

    In JavaScript, String values are immutable, which means that they cannot be altered once created.

For example, the following code will produce an error because the letter B in the string Bob cannot be changed to the letter J:

```js
let myStr = "Bob";
myStr[0] = "J";
```

Note that this does not mean that myStr could not be re-assigned. The only way to change myStr would be to assign it with a new value, like this:

```js
let myStr = "Bob";
myStr = "Job";
```

In case of array it work perfectly

```js
var array = ["ahmad", "sudais", "kamran"];
console.log(array);
array[0] = "imran";
console.log(array);
```

<hr>

# 35-Use Bracket Notation to Find the Nth Character in a String

    You can also use bracket notation to get the    character at other positions within a string.

    Remember that computers start counting at 0, so the first character is actually the zeroth character.

### Example:

```js
const firstName = "Ada";
const secondLetterOfFirstName = firstName[1];
```

<code>secondLetterOfFirstName</code> would have a value of the string d.

<hr>

# 35-Use Bracket Notation to Find the Last Character in a String

In order to get the last letter of a string, you can subtract one from the string's length.

    For example, if const firstName = "Ada", you can get the value of the last letter of the string by using

    firstName[firstName.length - 1].

### Example:

```js
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
console.log(lastName[lastName.length - 1]);
```

<code>lastLetter</code> would have a value of the string <code>a</code>

<hr>

# 36-Use Bracket Notation to Find the Nth-to-Last Character in a String

You can use the same principle we just used to retrieve the last character in a string to retrieve the Nth-to-last character.

    For example, you can get the value of the third-to-last letter of the const firstName = "Augusta" string by using

    firstName[firstName.length - 3]

Example:

```js
const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length - 3];
console.log(lastName[lastName.length - 2]);
```

thirdToLastLetter would have a value of the string s.

<hr>

# 37-Word Blanks

    You are provided sentences with some missing words, like nouns, verbs, adjectives and adverbs. You then fill in the missing pieces with words of your choice in a way that the completed sentence makes sense.

Consider this sentence:

    It was really ____, and we ____ ourselves ____.

This sentence has three missing pieces- an adjective, a verb and an adverb, and we can add words of our choice to complete it. We can then assign the completed sentence to a variable as follows:

```js
const sentence =
  "It was really " +
  "hot" +
  ", and we " +
  "laughed" +
  " ourselves " +
  "silly" +
  ".";
```

## Task

In this challenge, we provide you with a noun, a verb, an adjective and an adverb. You need to form a complete sentence using words of your choice, along with the words we provide.

    You will need to use the string concatenation operator + to build a new string, using the provided variables: myNoun, myAdjective, myVerb, and myAdverb. You will then assign the formed string to the wordBlanks variable. You should not change the words assigned to the variables.

    You will also need to account for spaces in your string, so that the final sentence has spaces between all the words. The result should be a complete sentence.

## code

```js
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

// Only change code below this line
const wordBlanks =
  "The " + myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb; // Change this line
// Only change code above this line
console.log(
  "The " + myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb
);
```

<hr>

# 38-Store Multiple Values in one Variable using JavaScript Arrays

    With JavaScript array variables, we can store several pieces of data in one place.

You start an array declaration with an opening square bracket, end it with a closing square bracket, and put a comma between each entry, like this:

```js
const sandwich = ["peanut butter", "jelly", "bread"];
```

<hr>

# 39-Nest one Array within Another Array

    You can also nest arrays within other arrays, like below:

```js
const teams = [
  ["Bulls", 23],
  ["White Sox", 45],
];

const myArray = [
  ["ahmad", 23],
  ["sudais", 34],
  ["kamran", 21],
];
```

This is also called a multi-dimensional array.

<hr>

# 40-Access Array Data with Indexes

    We can access the data inside arrays using indexes.

Array indexes are written in the same bracket notation that strings use, except that instead of specifying a character, they are specifying an entry in the array. Like strings, arrays use zero-based indexing, so the first element in an array has an index of 0.

### Example

```js
const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];
//The console.log(array[0]) prints 50, and data has the value 60.
```

<hr>

# 41-Modify Array Data With Indexes

Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with const.

### Example

```js
const ourArray = [50, 40, 30];
ourArray[0] = 15;
//ourArray now has the value [15, 40, 30].
```

### Note:

There shouldn't be any spaces between the array name and the square brackets, like array [0]. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

<hr>

# 42-Access Multi-Dimensional Arrays With Indexes

    One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outermost (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

### Example

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

    In this example, subarray has the value [[10, 11, 12], 13, 14], nestedSubarray has the value [10, 11, 12], and element has the value 11 .

### Note:

    There shouldn't be any spaces between the array name and the square brackets, like array [0][0] and even this array [0] [0] is not allowed. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

### Task code

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[2][1];
console.log(myData);
console.log(myArray[3][1], myArray[0][1]);
```

<hr>

# 43-Manipulate Arrays With push Method

    An easy way to append data to the end of an array is via the push() method.

    The push() method takes one or more arguments and appends them to the end of the array, in the order in which they appear. It returns the new length of the array.

### Examples:

```js
const arr1 = [1, 2, 3];
arr1.push(4, 5);
// arr1 now has the value [1, 2, 3, 4, 5]

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
// arr2 has the value ["Stimpson", "J", "cat", ["happy", "joy"]].
```

### task code

```js
// Setup
const myArray = [
  ["John", 23],
  ["cat", 2],
];

// before push
console.log(myArray);
myArray.push(["dog", 3]);
// after push
console.log(myArray);
```

<hr>

# 44-Manipulate Arrays With pop Method

    Another way to change the data in an array is with the .pop() function.

    .pop() is used to pop a value off of the end of an array. We can store this popped off value by assigning it to a variable. In other words, .pop() removes the last element from an array and returns that element.

Any type of entry can be popped off of an array - numbers, strings, even nested arrays.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```

The first console.log will display the value 6, and the second will display the value [1, 4].

```js
// Setup
const myArray = [
  ["John", 23],
  ["cat", 2],
];

// Only change code below this line
const removedFromMyArray = myArray.pop();
console.log(removedFromMyArray);
```

# 45-Manipulate Arrays With shift Method

    pop() always removes the last element of an array. What if you want to remove the first?

    That's where .shift() comes in. It works just like .pop(), except it removes the first element instead of the last.

### Example:

```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```

    removedFromOurArray would have a value of the string Stimpson, and ourArray would have ["J", ["cat"]]

```js
// Setup
const myArray = [
  ["John", 23],
  ["dog", 3],
];

console.log(myArray);
// Only change code below this line
const removedFromMyArray = myArray.shift();
console.log(myArray);
```

This will not worked on strings

```js
const str = "hello";
console.log(str);
str.shift();
// will throw error str.shift() is not function
```

<hr>

# 46-Manipulate Arrays With unshift Method

    Not only can you shift elements off of the beginning of an array, you can also unshift elements to the beginning of an array i.e. add elements in front of the array.

    .unshift() works exactly like .push(), but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.

### Example:

```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```

    After the shift, ourArray would have the value ["J", "cat"]. After the unshift, ourArray would have the value ["Happy", "J", "cat"].

### Task Code

```js
// Setup
const myArray = [
  ["John", 23],
  ["dog", 3],
];
myArray.shift();
// Only change code below this line
myArray.unshift(["Paul", 35]);
console.log(myArray);
```

<hr>

# 47-Shopping List

Create a shopping list in the variable myList. The list should be a multi-dimensional array containing several sub-arrays.

The first element in each sub-array should contain a string with the name of the item. The second element should be a number representing the quantity i.e.

```js
["Chocolate Bar", 15];
```

There should be at least 5 sub-arrays in the list.

### Solution

```js
const myList = [
  ["Iphone", 23],
  ["HandFree", 13],
  ["MicroPhone", 83],
  ["Device", 63],
  ["Nokia", 33],
];
```

<hr>

# 48-Write Reusable JavaScript with Functions

In JavaScript, we can divide up our code into reusable parts called functions.

Here's an example of a function:

```js
// declare the function
function functionName() {
  console.log("Hello World");
}
// call the function
functionName();
```

You can call or invoke this function by using its name followed by parentheses, like this: functionName(); Each time the function is called it will print out the message Hello World on the dev console. All of the code between the curly braces will be executed every time the function is called.

1. Create a function called reusableFunction which prints the string Hi World to the dev console.
2. Call the function.

```js
function reusableFunction() {
  console.log("Hi World");
}
reusableFunction();
reusableFunction();
reusableFunction();
reusableFunction();
```

<hr>

# 49-Passing Values to Functions with Arguments

    Parameters are variables that act as placeholders for the values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called are known as arguments.

Here is a function with two parameters, param1 and param2:

```js
function testFun(param1, param2) {
  console.log(param1, param2);
}
```

Then we can call testFun like this: <code>testFun("Hello", "World");</code> We have passed two string arguments, Hello and World. Inside the function, param1 will equal the string Hello and param2 will equal the string World. Note that you could call testFun again with different arguments and the parameters would take on the value of the new arguments.

### Task

1. Create a function called functionWithArgs that accepts two arguments and outputs their sum to the dev console.
2. Call the function with two numbers as arguments.

```js
function functionWithArgs(param1, param2) {
  console.log(param1 + param2);
}

functionWithArgs(50, 30); //80
functionWithArgs(45, 34); //79
functionWithArgs(40, 34); //74
```

<hr>

# 50-Return a Value from a Function with Return

We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.

### Example

```js
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
// answer has the value 8.
```

plusThree takes an argument for num and returns a value equal to num + 3.

### Task

    Create a function timesFive that accepts one argument, multiplies it by 5, and returns the new value.

### Solution

```js
function timeFive(num) {
  return num * 5;
}

console.log(timeFive(10)); //50
console.log(timeFive(20)); //100
console.log(timeFive(6)); //30
```

<hr>

# 51-Global Scope and Functions

    In JavaScript, scope refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.

    Variables which are declared without the let or const keywords are automatically created in the global scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with let or const.

### Task

1. Using let or const, declare a global variable named myGlobal outside of any function. Initialize it with a value of 10.

2. Inside function fun1, assign 5 to oopsGlobal without using the var, let or const keywords.

### Solution

```js
let myGlobal = 10;
function fun1() {
  // here we cannot assign any datatypes so it will act as a global scope and access from every where
  oopsGlobal = 5;
}

// in here we can access the oppsGlobal variable
function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```

<hr>

# 52-Local Scope and Functions

    Variables which are declared within a function, as well as the function parameters, have local scope. That means they are only visible within that function.

Here is a function myTest with a local variable called loc.

```js
function myTest() {
  const loc = "foo";
  console.log(loc);
}

myTest();
console.log(loc);
```

The myTest() function call will display the string foo in the console. The console.log(loc) line (outside of the myTest function) will throw an error, as loc is not defined outside of the function.

The editor has two console.logs to help you see what is happening. Check the console as you code to see how it changes. Declare a local variable myVar inside myLocalScope and run the tests.

### Note:

The console will still display ReferenceError: myVar is not defined, but this will not cause the tests to fail.

```js
function myLocalScope() {
  // Only change code below this line
  var myVar = 20;

  console.log("inside myLocalScope", myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log("outside myLocalScope", myVar);
```

<hr>

# 53-Global vs. Local Scope in Functions

    It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.

In this example:

```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}
```

The function myFun will return the string Head because the local version of the variable is present.

### Task

Add a local variable to myOutfit function to override the value of outerWear with the string sweater.

```js
// Setup
const outerWear = "T-Shirt";
console.log(outerWear);

function myOutfit() {
  const outerWear = "sweater";
  console.log(outerWear);
  return outerWear;
}

console.log(outerWear);

myOutfit();
```

<hr>

# 54-Understanding Undefined Value returned from a Function

    A function can include the return statement but it does not have to. In the case that the function doesn't have a return statement, when you call it, the function processes the inner code but the returned value is undefined.

### Example

```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}

addSum(3);
```

addSum is a function without a return statement. The function will change the global sum variable but the returned value of the function is undefined.

### Task

Create a function addFive without any arguments. This function adds 5 to the sum variable, but its returned value is undefined.

```js
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}

// Only change code below this line

function addFive() {
  sum += 5;
}

// Only change code above this line

console.log(addThree()); //undefined
console.log(addFive()); //undefined
```

<hr>

# 55-Assignment with a Returned Value

    If you'll recall from our discussion about Storing Values with the Assignment Operator, everything to the right of the equal sign is resolved before the value is assigned. This means we can take the return value of a function and assign it to a variable.

Assume we have defined a function sum which adds two numbers together.

```js
ourSum = sum(5, 12);
```

Calling the sum function with the arguments of 5 and 12 produces a return value of 17. This return value is assigned to the ourSum variable.

### Task

1. Call the processArg function with an argument of 7 and assign its return value to the variable processed.

### Solution

```js
// Setup
let processed = 0;

function processArg(num) {
  return (num + 3) / 5;
}

// Only change code below this line
processed = processArg(7);
```

<hr>

# 56-Stand in Line

    In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

### Task

1. Write a function nextInLine which takes an array (arr) and a number (item) as arguments.

2. Add the number to the end of the array, then remove the first element of the array.

3. The nextInLine function should then return the element that was removed.

### Solution

```js
function nextInLine(arr, item) {
  arr.push(item);
  return (item = arr.shift());
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code

console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```

### Note

    1. JSON.stringify(obj) method will convert object into string

    2. There is another method which will convert string into Object,That method is JSON.parse(string)

<hr>

# 57-Understanding Boolean Values

    Another data type is the Boolean. Booleans may only be one of two values: true or false. They are basically little on-off switches, where true is on and false is off. These two states are mutually exclusive.

### Note

Boolean values are never written with quotes. The strings "true" and "false" are not Boolean and have no special meaning in JavaScript.

### Task

Modify the welcomeToBooleans function so that it returns true instead of false.

```js
function welcomeToBooleans() {
  // Only change code below this line

  return true; // Change this line

  // Only change code above this line
}
```

<hr>

# 57-Use Conditional Logic with If Statements

    if statements are used to make decisions in code. The keyword if tells JavaScript to execute the code in the curly braces under certain conditions, defined in the parentheses. These conditions are known as Boolean conditions and they may only be true or false.

    When the condition evaluates to true, the program executes the statement inside the curly braces. When the Boolean condition evaluates to false, the statement inside the curly braces will not execute.

### Pseudocode

```js
if (condition is true) {
  //statement is executed
}
```

### Example

```js
function test(myCondition) {
  if (myCondition) {
    return "It was true";
  }
  return "It was false";
}

test(true);
test(false);
```

test(true) returns the string It was true, and test(false) returns the string It was false.

    When test is called with a value of true, the if statement evaluates myCondition to see if it is true or not. Since it is true, the function returns It was true. When we call test with a value of false, myCondition is not true and the statement in the curly braces is not executed and the function returns It was false.

### Task

Create an if statement inside the function to return Yes, that was true if the parameter wasThatTrue is true and return No, that was false otherwise.

```js
function trueOrFalse(wasThatTrue) {
  // Only change code below this line
  if (wasThatTrue) {
    return "Yes, that was true";
  } else {
    return "No, that was false";
  }
}
const trueR = trueOrFalse(true);
const falseR = trueOrFalse(false);
console.log(trueR);
console.log(falseR);
```

<hr>

# 58-Comparison with the Equality Operator

There are many comparison operators in JavaScript. All of these operators return a boolean true or false value.

    The most basic operator is the equality operator ==. The equality operator compares two values and returns true if they're equivalent or false if they are not. Note that equality is different from assignment (=), which assigns the value on the right of the operator to a variable on the left.

```js
function equalityTest(myVal) {
  if (myVal == 10) {
    return "Equal";
  }
  return "Not Equal";
}
```

If myVal is equal to 10, the equality operator returns true, so the code in the curly braces will execute, and the function will return Equal. Otherwise, the function will return Not Equal. In order for JavaScript to compare two different data types (for example, numbers and strings), it must convert one type to another. This is known as Type Coercion. Once it does, however, it can compare terms as follows:

```js
1 == 1; // true
1 == 2; // false
1 == "1"; // true
"3" == 3; // true
```

### Task

1. Add the equality operator to the indicated line so that the function will return the string Equal when val is equivalent to 12.

### Solution

```js
// Setup
function testEqual(val) {
  if (val == 12) {
    // Change this line
    return "Equal";
  }
  return "Not Equal";
}

testEqual(10);
```

<hr>

# 59-Comparison with the Strict Equality Operator

    Strict equality (===) is the counterpart to the equality operator (==). However, unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion.

If the values being compared have different types, they are considered unequal, and the strict equality operator will return false.

### Examples

```js
3 === 3; // true
3 === "3"; // false
```

In the second example, 3 is a Number type and '3' is a String type.

### Task

1. Use the strict equality operator in the if statement so the function will return the string Equal when val is strictly equal to 7.

### Solution

```js
// Setup
function testStrict(val) {
  if (val === 7) {
    // Change this line
    return "Equal";
  }
  return "Not Equal";
}

testStrict(7);
```

<hr>

# 60-Practice comparing different values

    In the last two challenges, we learned about the equality operator (==) and the strict equality operator (===). Let's do a quick review and practice using these operators some more.

If the values being compared are not of the same type, the equality operator will perform a type conversion, and then evaluate the values. However, the strict equality operator will compare both the data type and value as-is, without converting one type to the other.

### Examples

    3 == '3' returns true because JavaScript performs type conversion from string to number. 3 === '3' returns false because the types are different and type conversion is not performed.

### Note:

In JavaScript, you can determine the type of a variable or a value with the typeof operator, as follows:

```js
typeof 3;
typeof "3";
```

typeof 3 returns the string number, and typeof '3' returns the string string.

### Task

1. The compareEquality function in the editor compares two values using the equality operator. Modify the function so that it returns the string Equal only when the values are strictly equal.

### Solution

```js
// Setup
function compareEquality(a, b) {
  if (a === b) {
    // Change this line
    return "Equal";
  }
  return "Not Equal";
}

compareEquality(10, "10");
```

<hr>

# 61-Comparison with the Inequality Operator

    The inequality operator (!=) is the opposite of the equality operator. It means not equal and returns false where equality would return true and vice versa. Like the equality operator, the inequality operator will convert data types of values while comparing.

### Examples

```js
1 != 2; // true
1 != "1"; // false
1 != "1"; // false
1 != true; // false
0 != false; // false
```

### Task

Add the inequality operator != in the if statement so that the function will return the string Not Equal when val is not equivalent to 99.

### Solution

```js
// Setup
function testNotEqual(val) {
  if (val != 99) {
    // Change this line
    return "Not Equal";
  }
  return "Equal";
}

testNotEqual(10);
```

<hr>

# 62-Comparison with the Strict Inequality Operator

    The strict inequality operator (!==) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns false where strict equality would return true and vice versa. The strict inequality operator will not convert data types.

### Examples

```js
3 !== 3; // false
3 !== "3"; // true
4 !== 3; // true
```

### Task

Add the strict inequality operator to the if statement so the function will return the string Not Equal when val is not strictly equal to 17

### Solution

```js
// Setup
function testStrictNotEqual(val) {
  if (val !== 17) {
    // Change this line
    return "Not Equal";
  }
  return "Equal";
}

testStrictNotEqual(10);
```

<hr>

# 63-Comparison with the Greater Than Operator

The greater than operator (>) compares the values of two numbers. If the number to the left is greater than the number to the right, it returns true. Otherwise, it returns false.

Like the equality operator, the greater than operator will convert data types of values while comparing.

### Examples

```js
5 > 3; // true
7 > "3"; // true
2 > 3; // false
"1" > 9; // false
```

### Task

Add the greater than operator to the indicated lines so that the return statements make sense.

### Solution

```js
function testGreaterThan(val) {
  if (val > 100) {
    // Change this line
    return "Over 100";
  }

  if (val > 10) {
    // Change this line
    return "Over 10";
  }

  return "10 or Under";
}

testGreaterThan(10);
```

<hr>

# 64-omparison with the Greater Than Or Equal To Operator

    The greater than or equal to operator (>=) compares the values of two numbers. If the number to the left is greater than or equal to the number to the right, it returns true. Otherwise, it returns false.

Like the equality operator, the greater than or equal to operator will convert data types while comparing.

### Examples

```js
6 >= 6; // true
7 >= "3"; // true
2 >= 3; // false
"7" >= 9; // false
```

### Task

1. dd the greater than or equal to operator to the indicated lines so that the return statements make sense.

```js
function testGreaterOrEqual(val) {
  if (val >= 20) {
    // Change this line
    return "20 or Over";
  }

  if (val >= 10) {
    // Change this line
    return "10 or Over";
  }

  return "Less than 10";
}

testGreaterOrEqual(10);
```

<hr>

# 65-Comparison with the Less Than Operator

    The less than operator (<) compares the values of two numbers. If the number to the left is less than the number to the right, it returns true. Otherwise, it returns false. Like the equality operator, the less than operator converts data types while comparing.

### Examples

```js
2 < 5; // true
"3" < 7; // true
5 < 5; // false
3 < 2; // false
"8" < 4; // false
```

### Task

1. Add the less than operator to the indicated lines so that the return statements make sense.

### Solution

```js
function testLessThan(val) {
  if (val < 25) {
    // Change this line
    return "Under 25";
  }

  if (val < 55) {
    // Change this line
    return "Under 55";
  }

  return "55 or Over";
}

testLessThan(10);
```

<hr>

# 66-Comparison with the Less Than Or Equal To Operator

    The less than or equal to operator (<=) compares the values of two numbers. If the number to the left is less than or equal to the number to the right, it returns true. If the number on the left is greater than the number on the right, it returns false. Like the equality operator, the less than or equal to operator converts data types.

### Examples

```js
"7" <= 7; // true
5 <= 5; // true
3 <= 2; // false
"8" <= 4; // false
4 <= 5; // true
```

### Task

1. Add the less than or equal to operator to the indicated lines so that the return statements make sense.

### Solution

```js
function testLessOrEqual(val) {
  if (val <= 12) {
    // Change this line
    return "Smaller Than or Equal to 12";
  }

  if (val <= 24) {
    // Change this line
    return "Smaller Than or Equal to 24";
  }
  return "More Than 24";
}

console.log(testLessOrEqual(10));
console.log(testLessOrEqual(45));
console.log(testLessOrEqual(22));
```

<hr>

# 67-Comparisons with the Logical And Operator

    Sometimes you will need to test more than one thing at a time. The logical and operator (&&) returns true if and only if the operands to the left and right of it are true.

The same effect could be achieved by nesting an if statement inside another if.

```js
if (num > 5) {
  if (num < 10) {
    return "Yes";
  }
}
return "No";
```

This code will return Yes if num is greater than 5 and less than 10. The same logic can be written with the logical and operator.

```js
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
```

### Task

1. Replace the two if statements with one statement, using the && operator, which will return the string Yes if val is less than or equal to 50 and greater than or equal to 25. Otherwise, will return the string No.

### Solution

```js
function testLogicalAnd(val) {
  // Only change code below this line

  if (val <= 50 && val >= 25) {
    return "Yes";
  }

  // Only change code above this line
  return "No";
}

console.log(testLogicalAnd(10));
console.log(testLogicalAnd(33));
console.log(testLogicalAnd(63));
```

<hr>

# 68-Comparisons with the Logical Or Operator

    The logical or operator (||) returns true if either of the operands is true. Otherwise, it returns false.

    The logical or operator is composed of two pipe symbols: (||). This can typically be found between your Backspace and Enter keys.

The pattern below should look familiar from prior waypoints.

```js
if (num > 10) {
  return "No";
}
if (num < 5) {
  return "No";
}
return "Yes";
```

This code will return Yes if num is between 5 and 10 (5 and 10 included). The same logic can be written with the logical or operator.

```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
```

### Task

Combine the two if statements into one statement which returns the string Outside if val is not between 10 and 20, inclusive. Otherwise, return the string Inside.

### Solution

```js
function testLogicalOr(val) {
  // Only change code below this line

  if (val < 10 || val > 20) {
    return "Outside";
  }
  // Only change code above this line
  return "Inside";
}

console.log(testLogicalOr(5));
console.log(testLogicalOr(15));
console.log(testLogicalOr(25));
```

<hr>

# 69-Introducing Else Statements

    When a condition for an if statement is true, the block of code following it is executed. What about when that condition is false? Normally nothing would happen. With an else statement, an alternate block of code can be executed.

```js
if (num > 10) {
  return "Bigger than 10";
} else {
  return "10 or Less";
}
```

### Task

Combine the if statements into a single if/else statement.

### Solution

```js
function testElse(val) {
  let result = "";
  // Only change code below this line

  if (val > 5) {
    result = "Bigger than 5";
  } else {
    result = "5 or Smaller";
  }

  // Only change code above this line
  return result;
}

console.log(testElse(4));
```

<hr>

# 70-Introducing Else If Statements

    If you have multiple conditions that need to be addressed, you can chain if statements together with else if statements.

```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

Convert the logic to use else if statements.

```js
function testElseIf(val) {
  if (val > 10) {
    return "Greater than 10";
  } else if (val < 5) {
    return "Smaller than 5";
  } else {
    return "Between 5 and 10";
  }
}

console.log(testElseIf(7));
console.log(testElseIf(3));
console.log(testElseIf(34));
```

<hr>

# 71-Logical Order in If Else Statements

    Order is important in if, else if statements.

    The function is executed from top to bottom so you will want to be careful of what statement comes first.

Take these two functions as an example.

1. Here's the first:

```js
function foo(x) {
  if (x < 1) {
    return "Less than one";
  } else if (x < 2) {
    return "Less than two";
  } else {
    return "Greater than or equal to two";
  }
}
```

2. And the second just switches the order of the statements:

```js
function bar(x) {
  if (x < 2) {
    return "Less than two";
  } else if (x < 1) {
    return "Less than one";
  } else {
    return "Greater than or equal to two";
  }
}
```

While these two functions look nearly identical if we pass a number to both we get different outputs.

```js
foo(0);
bar(0);
```

foo(0) will return the string Less than one, and bar(0) will return the string Less than two.

### Task

Change the order of logic in the function so that it will return the correct statements in all cases.

```js
function orderMyLogic(val) {
  if (val < 5) {
    return "Less than 5";
  } else if (val < 10) {
    return "Less than 10";
  } else {
    return "Greater than or equal to 10";
  }
}

console.log(orderMyLogic(7));
console.log(orderMyLogic(3));
console.log(orderMyLogic(70));
```

<hr>

# 72-Chaining If Else Statements

    if/else statements can be chained together for complex logic. Here is pseudocode of multiple chained if / else if statements:

### Syntex

```js
if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else if (condition3) {
  statement3
. . .
} else {
  statementN
}
```

### Task

1. Write chained if/else if statements to fulfill the following conditions:

```js
num < 5 - return Tiny
num < 10 - return Small
num < 15 - return Medium
num < 20 - return Large
num >= 20 - return Huge

```

### Solution

```js
function testSize(num) {
  // Only change code below this line
  if (num < 5) {
    return "Tiny";
  } else if (num < 10) {
    return "Small";
  } else if (num < 15) {
    return "Medium";
  } else if (num < 20) {
    return "Large";
  } else if (num >= 20) {
    return "Huge";
  } else {
    return "Change Me";
  }
  // Only change code above this line
}

console.log(testSize(2));
console.log(testSize(7));
console.log(testSize(13));
console.log(testSize(18));
console.log(testSize(45));
```

<hr>

# 73-Golf Code

    In the game of Golf, each hole has a par, meaning, the average number of strokes a golfer is expected to make in order to sink the ball in the hole to complete the play. Depending on how far above or below par your strokes are, there is a different nickname.

    Your function will be passed par and strokes arguments. Return the correct string according to this table which lists the strokes in order of priority; top (highest) to bottom (lowest):

Strokes | Return

```
1	"Hole-in-one!"
<= par - 2	"Eagle"
par - 1	"Birdie"
par	"Par"
par + 1	"Bogey"
par + 2	"Double Bogey"
>= par + 3	"Go Home!"
```

par and strokes will always be numeric and positive. We have added an array of all the names for your convenience.

### Solution

```js
const names = [
  "Hole-in-one!",
  "Eagle",
  "Birdie",
  "Par",
  "Bogey",
  "Double Bogey",
  "Go Home!",
];

function golfScore(par, strokes) {
  // Only change code below this line
  if (strokes == 1) {
    return names[0];
  } else if (strokes <= par - 2) {
    return names[1];
  } else if (strokes == par - 1) {
    return names[2];
  } else if (strokes == par) {
    return names[3];
  } else if (strokes == par + 1) {
    return names[4];
  } else if (strokes == par + 2) {
    return names[5];
  } else {
    return names[6];
  }

  // Only change code above this line
}

console.log(golfScore(4, 1));
console.log(golfScore(4, 2));
console.log(golfScore(5, 2));
console.log(golfScore(4, 3));
console.log(golfScore(4, 4));
console.log(golfScore(1, 1));
console.log(golfScore(5, 5));
console.log(golfScore(4, 5));
console.log(golfScore(4, 6));
console.log(golfScore(4, 7));
console.log(golfScore(5, 9));
```

<hr>

# 74-Selecting from Many Options with Switch Statements

    If you need to match one value against many options, you can use a switch statement. A switch statement compares the value to the case statements which define various possible values. Any valid JavaScript statements can be executed inside a case block and will run from the first matched case value until a break is encountered.

Here is an example of a switch statement:

```js
switch (fruit) {
  case "apple":
    console.log("The fruit is an apple");
    break;
  case "orange":
    console.log("The fruit is an orange");
    break;
}
```

    case values are tested with strict equality (===). The break tells JavaScript to stop executing statements. If the break is omitted, the next statement will be executed.

### Task

1. Write a switch statement which tests val and sets answer for the following conditions:

   ```
   1 - alpha
   2 - beta
   3 - gamma
   4 - delta
   ```

### Solution

```js
function caseInSwitch(val) {
  let answer = "";
  // Only change code below this line
  switch (val) {
    case 1:
      answer = "alpha";
      break;
    case 2:
      answer = "beta";
      break;
    case 3:
      answer = "gamma";
      break;
    case 4:
      answer = "delta";
      break;
  }

  // Only change code above this line
  return answer;
}
console.log(caseInSwitch(1));
console.log(caseInSwitch(2));
console.log(caseInSwitch(3));
console.log(caseInSwitch(4));
```

<hr>

# 75-Adding a Default Option in Switch Statements

    In a switch statement you may not be able to specify all possible values as case statements. Instead, you can add the default statement which will be executed if no matching case statements are found. Think of it like the final else statement in an if/else chain.

A default statement should be the last case.

```js
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
  default:
    defaultStatement;
    break;
}
```

### Task

1. Write a switch statement to set answer for the following conditions:
   ```
   a - apple
   b - bird
   c - cat
   default - stuff
   ```

### Solution

```js
function switchOfStuff(val) {
  let answer = "";
  // Only change code below this line
  switch (val) {
    case "a":
      answer = "apple";
      break;
    case "b":
      answer = "bird";
      break;
    case "c":
      answer = "cat";
      break;
    default:
      answer = "stuff";
      break;
  }

  // Only change code above this line
  return answer;
}

console.log(switchOfStuff(1));
console.log(switchOfStuff("a"));
console.log(switchOfStuff("b"));
console.log(switchOfStuff("c"));
```

<hr>

# 76-Multiple Identical Options in Switch Statements

    If the break statement is omitted from a switch statement's case, the following case statement(s) are executed until a break is encountered. If you have multiple inputs with the same output, you can represent them in a switch statement like this:

```js
let result = "";
switch (val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```

    Cases for 1, 2, and 3 will all produce the same result.

### Task

1. Write a switch statement to set answer for the following ranges:

```
  1-3 - Low
  4-6 - Mid
  7-9 - High
```

Note: You will need to have a case statement for each number in the range.

### SOlution

```js
function sequentialSizes(val) {
  let answer = "";

  // Only change code below this line
  switch (val) {
    case 1:
    case 2:
    case 3:
      answer = "Low";
      break;
    case 4:
    case 5:
    case 6:
      answer = "Mid";
      break;
    case 7:
    case 8:
    case 9:
      answer = "High";
      break;
    default:
      answer = "out of range";
      break;
  }

  // Only change code above this line
  return answer;
}

console.log(sequentialSizes(1));
console.log(sequentialSizes(2));
console.log(sequentialSizes(3));
console.log(sequentialSizes(4));
console.log(sequentialSizes(5));
console.log(sequentialSizes(6));
console.log(sequentialSizes(7));
console.log(sequentialSizes(8));
console.log(sequentialSizes(9));
console.log(sequentialSizes(20));
console.log(sequentialSizes(40));
```

<hr>

# 77-Replacing If Else Chains with Switch

    If you have many options to choose from, a switch statement can be easier to write than many chained if/else if statements. The following:

```js
if (val === 1) {
  answer = "a";
} else if (val === 2) {
  answer = "b";
} else {
  answer = "c";
}
```

can be replaced with:

```js
switch (val) {
  case 1:
    answer = "a";
    break;
  case 2:
    answer = "b";
    break;
  default:
    answer = "c";
}
```

### Task

Change the chained if/else if statements into a switch statement.

```js
function chainToSwitch(val) {
  let answer = "";
  // Only change code below this line

  if (val === "bob") {
    answer = "Marley";
  } else if (val === 42) {
    answer = "The Answer";
  } else if (val === 1) {
    answer = "There is no #1";
  } else if (val === 99) {
    answer = "Missed me by this much!";
  } else if (val === 7) {
    answer = "Ate Nine";
  }

  // Only change code above this line
  return answer;
}

chainToSwitch(7);
```

### Solution

```js
function chainToSwitch(val) {
  let answer = "";
  // Only change code below this line

  switch (val) {
    case "bob":
      answer = "Marley";
      break;
    case 42:
      answer = "The Answer";
      break;
    case 1:
      answer = "There is no #1";
      break;
    case 99:
      answer = "Missed me by this much!";
      break;
    case 7:
      answer = "Ate Nine";
      break;
    default:
      answer = "";
      break;
  }
  // Only change code above this line
  return answer;
}

console.log(chainToSwitch(7));
console.log(chainToSwitch("bob"));
console.log(chainToSwitch(42));
console.log(chainToSwitch(1));
console.log(chainToSwitch(99));
console.log(chainToSwitch("156"));
```

<hr>

# 78-Returning Boolean Values from Functions

    You may recall from Comparison with the Equality Operator that all comparison operators return a boolean true or false value.

Sometimes people use an if/else statement to do a comparison, like this:

```js
function isEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}
```

But there's a better way to do this. Since === returns true or false, we can return the result of the comparison:

```js
function isEqual(a, b) {
  return a === b;
}
```

### Task

Fix the function isLess to remove the if/else statements.

```js
function isLess(a, b) {
  // Only change code below this line
  if (a < b) {
    return true;
  } else {
    return false;
  }
  // Only change code above this line
}

isLess(10, 15);
```

### Solution

```js
function isLess(a, b) {
  // Only change code below this line
  return a < b;
  // Only change code above this line
}

isLess(10, 15);
```

<hr>

# 79-Return Early Pattern for Functions

    When a return statement is reached, the execution of the current function stops and control returns to the calling location.

### Example

```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye");
}
myFun();
```

The above will display the string Hello in the console, and return the string World. The string byebye will never display in the console, because the function exits at the return statement.

### Task

1. Modify the function abTest so that if a or b are less than 0 the function will immediately exit with a value of undefined.

```js
// Setup
function abTest(a, b) {
  // Only change code below this line

  // Only change code above this line

  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

abTest(2, 2);
```

### Hint

Remember that undefined is a keyword, not a string.

```js
// Setup
function abTest(a, b) {
  // Only change code below this line

  // Only change code above this line
  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

abTest(2, 2);
```

### Solution

```js
// Setup
function abTest(a, b) {
  // Only change code below this line
  if (a < 0 || b < 0) return undefined;
  // Only change code above this line

  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

console.log(abTest(5, -7));
console.log(abTest(3, 5));
```

<hr>

# 80-Counting Cards

    In the casino game Blackjack, a player can determine whether they have an advantage on the next hand over the house by keeping track of the relative number of high and low cards remaining in the deck. This is called Card Counting.

    Having more high cards remaining in the deck favors the player. Each card is assigned a value according to the table below. When the count is positive, the player should bet high. When the count is zero or negative, the player should bet low.

```js
// Count Change	Cards
+1 =>	2, 3, 4, 5, 6
0	 => 7, 8, 9
-1 =>	10, 'J', 'Q', 'K', 'A'
```

You will write a card counting function. It will receive a card parameter, which can be a number or a string, and increment or decrement the global count variable according to the card's value (see table). The function will then return a string with the current count and the string Bet if the count is positive, or Hold if the count is zero or negative. The current count and the player's decision (Bet or Hold) should be separated by a single space.

Example Outputs: -3 Hold or 5 Bet

### Hint

Do NOT reset count to 0 when value is 7, 8, or 9.
Do NOT return an array.
Do NOT include quotes (single or double) in the output.

### Solution

```js
var count = 0;

function cc(card) {
  switch (card) {
    case 2:
    case 3:
    case 4:
    case 5:
    case 6:
      count++;
      break;
    case 10:
    case "J":
    case "Q":
    case "K":
    case "A":
      count--;
      break;
  }

  var holdbet = "Hold";
  if (count > 0) {
    holdbet = "Bet";
  }

  return count + " " + holdbet;
}

cc(2);
cc("/k");
cc(7);
cc("K");
cc("A");
console.log(cc(4));
console.log(cc("K"));
console.log(cc(10));
console.log(cc(4));
```

### Code Explanation

    Check the value of each card via a switch statement.
    The variable count:
    Increases by 1 if the card is a 2, 3, 4, 5, or 6.
    Since 7, 8, and 9 aren’t worth anything, we ignore those cards in our switch statement.
    Decreases by 1 if the card is a 10, ‘J’, ‘Q’, ‘K’, or ‘A’.
    Check the value of count and return the appropriate response.

### Example Run

    cc(2); runs.
    The switch statement hits case 2, jumps down and adds 1 to the variable count.
    The switch statement then hits the break and cc(3); runs.
    This cycle continues until the final call is made, cc('A');.
    After the switch statement, the if statement checks count, which is now 0.
    This then drops down to the else statement, which will return 0 Hold.

### Note:

As mentioned earlier, the switch statement could have also been an else if statement.

<hr>

# 81-Build JavaScript Objects

You may have heard the term object before.

    Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.

    Objects are useful for storing data in a structured way, and can represent real world objects, like a cat.

Here's a sample cat object:

```js
const cat = {
  name: "Whiskers",
  legs: 4,
  tails: 1,
  enemies: ["Water", "Dogs"],
};
```

In this example, all the properties are stored as strings, such as name, legs, and tails. However, you can also use numbers as properties. You can even omit the quotes for single-word string properties, as follows:

```js
const anotherObject = {
  make: "Ford",
  5: "five",
  model: "focus",
};
```

However, if your object has any non-string properties, JavaScript will automatically typecast them as strings.

### Task

1. Make an object that represents a dog called myDog which contains the properties name (a string), legs, tails and friends.

2. You can set these object properties to whatever values you want, as long as name is a string, legs and tails are numbers, and friends is an array.

### Solution

```js
const myDog = {
  // Only change code below this line
  name: "Yashmi",
  legs: 4,
  tails: 1,
  friends: ["Human", "Dog"],

  // Only change code above this line
};
```

<hr>

# 82-Accessing Object Properties with Dot Notation

    There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.

    Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

Here is a sample of using dot notation (.) to read an object's property:

```js
const myObj = {
  prop1: "val1",
  prop2: "val2",
};

const prop1val = myObj.prop1;
const prop2val = myObj.prop2;
```

prop1val would have a value of the string val1, and prop2val would have a value of the string val2.

### Task

1. Read in the property values of testObj using dot notation. Set the variable hatValue equal to the object's property hat and set the variable shirtValue equal to the object's property shirt.

### Solution

```js
// Setup
const testObj = {
  hat: "ballcap",
  shirt: "jersey",
  shoes: "cleats",
};

// Only change code below this line
const hatValue = testObj.hat; // Change this line
const shirtValue = testObj.shirt; // Change this line
```

<hr>

# 83-Accessing Object Properties with Bracket Notation

    The second way to access the properties of an object is bracket notation ([]). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

    However, you can still use bracket notation on object properties without spaces.

Here is a sample of using bracket notation to read an object's property:

```js
const myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  NoSpace: "USS Enterprise",
};

myObj["Space Name"];
myObj["More Space"];
myObj["NoSpace"];
```

    myObj["Space Name"] would be the string Kirk, myObj['More Space'] would be the string Spock, and myObj["NoSpace"] would be the string USS Enterprise.

Note that property names with spaces in them must be in quotes (single or double).

### Task

1. Read the values of the properties an entree and the drink of testObj using bracket notation and assign them to entreeValue and drinkValue respectively.

### Solution

```js
// Setup
const testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water",
};

// Only change code below this line
const entreeValue = testObj["an entree"]; // Change this line
const drinkValue = testObj["the drink"]; // Change this line

console.table([entreeValue, drinkValue]);
```

<hr>

# 84-Accessing Object Properties with Variables

    Another use of bracket notation on objects is to access a property which is stored as the value of a variable. This can be very useful for iterating through an object's properties or when accessing a lookup table.

Here is an example of using a variable to access a property:

```js
const dogs = {
  Fido: "Mutt",
  Hunter: "Doberman",
  Snoopie: "Beagle",
};

const myDog = "Hunter";
const myBreed = dogs[myDog];
console.log(myBreed);
```

The string Doberman would be displayed in the console.

### Note

that we do not use quotes around the variable name when using it to access the property because we are using the value of the variable, not the name.

### Task

1. Set the playerNumber variable to 16. Then, use the variable to look up the player's name and assign it to player.

### Solution

```js
// Setup
const testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas",
};

// Only change code below this line
const playerNumber = 16; // Change this line
const player = testObj[playerNumber]; // Change this line
console.log(player);
```

<hr>

# 85-Updating Object Properties

    After you've created a JavaScript object, you can update its properties at any time just like you would update any other variable. You can use either dot or bracket notation to update.

For example, let's look at ourDog:

```js
const ourDog = {
  name: "Camper",
  legs: 4,
  tails: 1,
  friends: ["everything!"],
};
```

    Since he's a particularly happy dog, let's change his name to the string Happy Camper. Here's how we update his object's name property: ourDog.name = "Happy Camper"; or ourDog["name"] = "Happy Camper"; Now when we evaluate ourDog.name, instead of getting Camper, we'll get his new name, Happy Camper.

### Task

1. Update the myDog object's name property. Let's change her name from Coder to Happy Coder. You can use either dot or bracket notation.

### Solution

```js
// Setup
const myDog = {
  name: "Coder",
  legs: 4,
  tails: 1,
  friends: ["freeCodeCamp Campers"],
};

console.log((myDog["name"] = "Happy Coder"));

// Only change code below this line
```

<hr>

# 86-Add New Properties to a JavaScript Object

    You can add new properties to existing JavaScript objects the same way you would modify them.

Here's how we would add a bark property to ourDog:

```js
ourDog.bark = "bow-wow";
// or
ourDog["bark"] = "bow-wow";
```

Now when we evaluate ourDog.bark, we'll get his bark, bow-wow.

### Example:

```js
const ourDog = {
  name: "Camper",
  legs: 4,
  tails: 1,
  friends: ["everything!"],
};

ourDog.bark = "bow-wow";
```

### Task

Add a bark property to myDog and set it to a dog sound, such as "woof". You may use either dot or bracket notation.

### Solution

```js
const myDog = {
  name: "Happy Coder",
  legs: 4,
  tails: 1,
  friends: ["freeCodeCamp Campers"],
};
console.log(myDog);
myDog.bark = "woof";
console.log(myDog);
```

<hr>

# 87-Delete Properties from a JavaScript Object

    We can also delete properties from objects like this:

delete ourDog.bark;
Example:

```js
const ourDog = {
  name: "Camper",
  legs: 4,
  tails: 1,
  friends: ["everything!"],
  bark: "bow-wow",
};

delete ourDog.bark;
```

After the last line shown above, ourDog looks like:

```js
{
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
}
```

### Task

Delete the tails property from myDog. You may use either dot or bracket notation.

### Solution

```js
// Setup
const myDog = {
  name: "Happy Coder",
  legs: 4,
  tails: 1,
  friends: ["freeCodeCamp Campers"],
  bark: "woof",
};

// Only change code below this line
console.log(myDog);
delete myDog.tails;
console.log(myDog);
```

<hr>

# 88-Using Objects for Lookups

    Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to lookup values rather than a switch statement or an if/else chain. This is most useful when you know that your input data is limited to a certain range.

Here is an example of an article object:

```js
const article = {
  title: "How to create objects in JavaScript",
  link: "https://www.freecodecamp.org/news/a-complete-guide-to-creating-objects-in-javascript-b0e2450655e8/",
  author: "Kaashan Hussain",
  language: "JavaScript",
  tags: "TECHNOLOGY",
  createdAt: "NOVEMBER 28, 2018",
};

const articleAuthor = article["author"];
const articleLink = article["link"];

const value = "title";
const valueLookup = article[value];
```

    articleAuthor is the string Kaashan Hussain, articleLink is the string https://www.freecodecamp.org/news/a-complete-guide-to-creating-objects-in-javascript-b0e2450655e8/, and valueLookup is the string How to create objects in JavaScript.

### task

Convert the switch statement into an object called lookup. Use it to look up val and assign the associated string to the result variable.

```js
// Setup
function phoneticLookup(val) {
  let result = "";

  // Only change code below this line
  switch (val) {
    case "alpha":
      result = "Adams";
      break;
    case "bravo":
      result = "Boston";
      break;
    case "charlie":
      result = "Chicago";
      break;
    case "delta":
      result = "Denver";
      break;
    case "echo":
      result = "Easy";
      break;
    case "foxtrot":
      result = "Frank";
  }

  // Only change code above this line
  return result;
}

phoneticLookup("charlie");
```

### Solution

```js
// Setup
function phoneticLookup(val) {
  let result = "";

  const lookup = {
    alpha: "Adams",
    bravo: "Boston",
    charlie: "Chicago",
    delta: "Denver",
    echo: "Easy",
    foxtrot: "Frank",
  };
  result = lookup[val];

  // Only change code above this line
  return result;
}

console.log(phoneticLookup("charlie"));
console.log(phoneticLookup("echo"));
console.log(phoneticLookup("delta"));
console.log(phoneticLookup("foxtrot"));
console.log(phoneticLookup("alpha"));
```

<hr>

# 89-Testing Objects for Properties

    To check if a property on a given object exists or not, you can use the .hasOwnProperty() method. someObject.hasOwnProperty(someProperty) returns true or false depending on if the property is found on the object or not.

### Example

```js
function checkForProperty(object, property) {
  return object.hasOwnProperty(property);
}

checkForProperty({ top: "hat", bottom: "pants" }, "top"); // true
checkForProperty({ top: "hat", bottom: "pants" }, "middle"); // false
```

The first checkForProperty function call returns true, while the second returns false.

# Task

1. Modify the function checkObj to test if the object passed to the function parameter obj contains the specific property passed to the function parameter checkProp. If the property passed to checkProp is found on obj, return that property's value. If not, return Not Found.

```js
function checkObj(obj, checkProp) {
  // Only change code below this line
  return "Change Me!";
  // Only change code above this line
}
```

### Solution

```js
function checkObj(obj, checkProp) {
  // Only change code below this line
  if (obj.hasOwnProperty(checkProp)) return obj[checkProp];
  else {
    return "Not Found";
  }
  // Only change code above this line
}

checkObj({ gift: "pony", pet: "kitten", bed: "sleigh" }, "gift");
checkObj({ gift: "pony", bed: "sleigh" }, "house");
```

<hr>

# 90-Manipulating Complex Objects

    Sometimes you may want to store data in a flexible Data Structure. A JavaScript object is one way to handle flexible data. They allow for arbitrary combinations of strings, numbers, booleans, arrays, functions, and objects.

Here's an example of a complex data structure:

```js
const ourMusic = [
  {
    artist: "Daft Punk",
    title: "Homework",
    release_year: 1997,
    formats: ["CD", "Cassette", "LP"],
    gold: true,
  },
];
```

    This is an array which contains one object inside.
    The object has various pieces of metadata about an album.
    It also has a nested formats array. If you want to add
    more album records, you can do this by adding records to
    the top level array. Objects hold data in a property,
    which has a key-value format. In the example above,
    "artist": "Daft Punk" is a property that has a key of
    artist and a value of Daft Punk.

### Note:

You will need to place a comma after every object in the array, unless it is the last object in the array.

### Task

Add a new album to the myMusic array. Add artist and title strings, release_year number, and a formats array of strings.

### Solution

```js
const myMusic = [
  {
    artist: "Billy Joel",
    title: "Piano Man",
    release_year: 1973,
    formats: ["CD", "8T", "LP"],
    gold: true,
  },
  {
    artist: "john Dave",
    title: "Laila",
    release_year: 2003,
    formats: ["CD", "DvT", "LP"],
    gold: false,
  },
];
```

<hr>

# 91-Accessing Nested Objects

    The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

Here is a nested object:

```js
const ourStorage = {
  desk: {
    drawer: "stapler",
  },
  cabinet: {
    "top drawer": {
      folder1: "a file",
      folder2: "secrets",
    },
    "bottom drawer": "soda",
  },
};

ourStorage.cabinet["top drawer"].folder2;
ourStorage.desk.drawer;
```

ourStorage.cabinet["top drawer"].folder2 would be the string secrets, and ourStorage.desk.drawer would be the string stapler.

### Task

Access the myStorage object and assign the contents of the glove box property to the gloveBoxContents variable. Use dot notation for all properties where possible, otherwise use bracket notation.

### Solution

```js
const myStorage = {
  car: {
    inside: {
      "glove box": "maps",
      "passenger seat": "crumbs",
    },
    outside: {
      trunk: "jack",
    },
  },
};

const gloveBoxContents = myStorage.car.inside["glove box"];
console.log(gloveBoxContents);
```

<hr>

# 92-Accessing Nested Arrays

    As we have seen in earlier examples, objects can contain both nested objects and nested arrays. Similar to accessing nested objects, array bracket notation can be chained to access nested arrays.

Here is an example of how to access a nested array:

```js
const ourPets = [
  {
    animalType: "cat",
    names: ["Meowzer", "Fluffy", "Kit-Cat"],
  },
  {
    animalType: "dog",
    names: ["Spot", "Bowser", "Frankie"],
  },
];

ourPets[0].names[1];
ourPets[1].names[0];
```

ourPets[0].names[1] would be the string Fluffy, and ourPets[1].names[0] would be the string Spot.

### task

Using dot and bracket notation, set the variable secondTree to the second item in the trees list from the myPlants object.

### Solution

```js
const myPlants = [
  {
    type: "flowers",
    list: ["rose", "tulip", "dandelion"],
  },
  {
    type: "trees",
    list: ["fir", "pine", "birch"],
  },
];

const secondTree = myPlants[1].list[1];
console.log(secondTree);
```

<hr>

# 93-Record Collection

    You are creating a function that aids in the maintenance of a musical album collection.
    The collection is organized as an object that contains multiple albums which are also objects.
    Each album is represented in the collection with a unique id as the property name.
    Within each album object, there are various properties describing information about the album.
    Not all albums have complete information.

The updateRecords function takes 4 arguments represented by the following function parameters:

1. records - an object containing several individual albums
2. id - a number representing a specific album in the records object
3. prop - a string representing the name of the album’s property to update
4. value - a string containing the information used to update the album’s property

Complete the function using the rules below to modify the object passed to the function.

- Your function must always return the entire records object.
- If value is an empty string, delete the given prop property from the album.
- If prop isn't tracks and value isn't an empty string, assign the value to that album's prop.
- If prop is tracks and value isn't an empty string, you need to update the album's tracks array. First, if the album does not have a tracks property, assign it an empty array. Then add the value as the last item in the album's tracks array.

### Note:

A copy of the recordCollection object is used for the tests. You should not directly modify the recordCollection object.

### Solution

```js
// Setup
const recordCollection = {
  2548: {
    albumTitle: "Slippery When Wet",
    artist: "Bon Jovi",
    tracks: ["Let It Rock", "You Give Love a Bad Name"],
  },
  2468: {
    albumTitle: "1999",
    artist: "Prince",
    tracks: ["1999", "Little Red Corvette"],
  },
  1245: {
    artist: "Robert Palmer",
    tracks: [],
  },
  5439: {
    albumTitle: "ABBA Gold",
  },
};

// Only change code below this line

function updateRecords(records, id, prop, value) {
  if (value === "") {
    delete records[id][prop];
  } else if (prop !== "tracks" && value !== "") {
    records[id][prop] = value;
  } else if (prop === "tracks" && value !== "") {
    if (records[id].hasOwnProperty("tracks") === false) {
      records[id][prop] = [];
    }
    records[id][prop].push(value);
  }
  return records;
}

updateRecords(recordCollection, 5439, "artist", "ABBA");
updateRecords(recordCollection, 5439, "tracks", "Take a Chance on Me");
updateRecords(recordCollection, 2548, "artist", "");
updateRecords(recordCollection, 1245, "tracks", "Addicted to Love");
updateRecords(recordCollection, 2468, "tracks", "Free");
updateRecords(recordCollection, 1245, "albumTitle", "Riptide");
updateRecords(recordCollection, 2548, "tracks", "");
```

### Code Explanation

This version of the code explicitly handles every possible case with separate if clauses.

- First it checks if the value is an empty string. If it is, then the prop is deleted.
- Then, if prop is not "tracks" and the value is not an empty string. The prop is set to the value.
- If that check doesn’t pass, it next checks if prop is equal to tracks, the value is not an empty string, and the record does not have a tracks array. The "tracks" array is initialized with the only contents being value.
- It next checks if prop is equal to tracks, the value is not an empty string. The "tracks" array must exist because the case above was not true. The value is pushed onto the end of the "tracks" array.
- Lastly, the entire records object is returned.
<hr>

# 94-Iterate with JavaScript While Loops

You can run the same code multiple times by using a loop.

    The first type of loop we will learn is called a while loop because it runs while a specified condition is true and stops once that condition is no longer true.

```js
const ourArray = [];
let i = 0;

while (i < 5) {
  ourArray.push(i);
  i++;
}
```

In the code example above, the while loop will execute 5 times and append the numbers 0 through 4 to ourArray.

Let's try getting a while loop to work by pushing values to an array.

### Task

Add the numbers 5 through 0 (inclusive) in descending order to myArray using a while loop.

```js
// Setup
const myArray = [];
let i = 5;

while (i >= 0) {
  myArray.push(i);
  i--;
}
console.log(myArray);
```

<hr>

# 95-Iterate with JavaScript For Loops

You can run the same code multiple times by using a loop.

    The most common type of JavaScript loop is called a for loop because it runs for a specific number of times.

For loops are declared with three optional expressions separated by semicolons:

<code>for (a; b; c)</code>

- where a is the initialization statement,
- b is the condition statement,
- and c is the final expression.

      The initialization statement is executed one time only before the loop starts. It is typically used to define and setup your loop variable.

      The condition statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to true. When the condition is false at the start of the iteration, the loop will stop executing. This means if the condition starts as false, your loop will never execute.

      The final expression is executed at the end of each loop iteration, prior to the next condition check and is usually used to increment or decrement your loop counter.

In the following example we initialize with i = 0 and iterate while our condition i < 5 is true. We'll increment i by 1 in each loop iteration with i++ as our final expression.

```js
const ourArray = [];

for (let i = 0; i < 5; i++) {
  ourArray.push(i);
}
// ourArray will now have the value [0, 1, 2, 3, 4].
```

### Task

Use a for loop to push the values 1 through 5 onto myArray.

```js
// Setup
const myArray = [];
for (let i = 1; i <= 5; i++) {
  console.log(i);
  myArray.push(i);
}
console.log(myArray);
// Only change code below this line
```

<hr>

# 96-Iterate Odd Numbers With a For Loop

    For loops don't have to iterate one at a time. By changing our final-expression, we can count by even numbers.

We'll start at i = 0 and loop while i < 10. We'll increment i by 2 each loop with i += 2.

```js
// Print Even number like [0,2,4,6,8....]
const ourArray = [];

for (let i = 0; i < 10; i += 2) {
  ourArray.push(i);
}
```

ourArray will now contain [0, 2, 4, 6, 8]. Let's change our initialization so we can count by odd numbers.

Push the odd numbers from 1 through 9 to myArray using a for loop.

```js
// Print Odd number like [1,3,5,7,9....]
const myArray = [];

// Only change code below this line
for(let i = 1; i<10; i+=2){
  console.log(i)
  myArray.push(i)
}
console.log(myArray)
```
<hr>

# 97-

<hr>

# 98-

<hr>

# 99-

<hr>

# 100-

<hr>
````
