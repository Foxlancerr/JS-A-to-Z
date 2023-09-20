# Comment Your JavaScript Code

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

# Declare JavaScript Variables

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

# Storing Values with the Assignment Operator

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

# Assigning the Value of One Variable to Another

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

# Initializing Variables with the Assignment Operator

    It is common to initialize a variable to an initial value in the same line as it is declared.

```js
var marks = 40;
```

Creates a new variable called marks and assigns it an initial value of 40.
