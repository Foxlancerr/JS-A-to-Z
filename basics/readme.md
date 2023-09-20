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

# Return a Value from a Function with Return

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
