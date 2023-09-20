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
