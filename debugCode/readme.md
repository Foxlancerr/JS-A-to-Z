# Debugging

Debugging is the process of going through your code, finding any issues, and fixing them.

Issues in code generally come in three forms: syntax errors that prevent your program from running, runtime errors where your code has unexpected behavior, or logical errors where your code doesn't do what you intended.

In this course, you'll learn how to use the JavaScript console to debug programs and prevent common issues before they happen.

# Total Lessons (12)

# 1-Use the JavaScript Console to Check the Value of a Variable

    Both Chrome and Firefox have excellent JavaScript consoles, also known as DevTools, for debugging your JavaScript.

You can find Developer tools in your Chrome's menu or Web Console in Firefox's menu. If you're using a different browser, or a mobile phone, we strongly recommend switching to desktop Firefox or Chrome.

The console.log() method, which "prints" the output of what's within its parentheses to the console, will likely be the most helpful debugging tool. Placing it at strategic points in your code can show you the intermediate values of variables. It's good practice to have an idea of what the output should be before looking at what it is. Having check points to see the status of your calculations throughout your code will help narrow down where the problem is.

Here's an example to print the string Hello world! to the console:

```js
console.log("Hello world!");
```

### Task

Use the console.log() method to print the value of the variable a where noted in the code.

### Solution

```js
let a = 5;
let b = 1;
a++;
console.log(a);

let sumAB = a + b;
console.log(sumAB);
```

# 2-Understanding the Differences between the freeCodeCamp and Browser Console

    You may have noticed that some freeCodeCamp challenges include their own console. This console behaves a little differently than the browser console.

There are many methods to use with console to output messages. log, warn, and clear to name a few. The freeCodeCamp console will only output log messages, while the browser console will output all messages. When you make changes to your code, it will automatically run and show the logs. The freeCodeCamp console is then cleared each time your code runs.

### Task

- First, open your browser console so you can see the logs. To do that, you can right-click the freeCodeCamp navigation bar at the top and click inspect on most browsers. Then find the console tab in the window that opens.

- After that, use console.log to log the output variable. View the two consoles to see the log. Finally, use console.clear after your log to clear the browser console. View the difference in the two consoles.

### Solution

```js
let output =
  "Get this to show once in the freeCodeCamp console and not at all in the browser console";
console.log(output);
console.clear();
```

# 3-Use typeof to Check the Type of a Variable

You can use typeof to check the data structure, or type, of a variable. This is useful in debugging when working with multiple data types.

If you think you're adding two numbers, but one is actually a string, the results can be unexpected. Type errors can lurk in calculations or function calls.

Be careful especially when you're accessing and working with external data in the form of a JavaScript Object Notation (JSON) object.

Here are some examples using typeof:

```js
console.log(typeof "");
console.log(typeof 0);
console.log(typeof []);
console.log(typeof {});
```

In order, the console will display the strings string, number, object, and object.

JavaScript recognizes seven primitive (immutable) data types: Boolean, Null, Undefined, Number, String, Symbol (new with ES6), and BigInt (new with ES2020), and one type for mutable items: Object. Note that in JavaScript, arrays are technically a type of object.

### Task

Add two console.log() statements to check the typeof each of the two variables seven and three in the code.

### Solution

```js
let seven = 7;
let three = "3";
console.log(seven + three);
console.log(typeof seven);
console.log(typeof three);
```

# 4-Catch Misspelled Variable and Function Names

    The console.log() and typeof methods are the two primary ways to check intermediate values and types of program output.

Now it's time to get into the common forms that bugs take. One syntax-level issue that fast typers can commiserate with is the humble spelling error.

Transposed, missing, or mis-capitalized characters in a variable or function name will have the browser looking for an object that doesn't exist - and complain in the form of a reference error. JavaScript variable and function names are case-sensitive.

### Task

Fix the two spelling errors in the code so the netWorkingCapital calculation works.

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = recievables - payable;
console.log(`Net working capital is: ${netWorkingCapital}`);
```

### Solution

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);
```

# 5-Catch Unclosed Parentheses, Brackets, Braces and Quotes

Another syntax error to be aware of is that all opening parentheses, brackets, curly braces, and quotes have a closing pair.

Forgetting a piece tends to happen when you're editing existing code and inserting items with one of the pair types.

Also, take care when nesting code blocks into others, such as adding a callback function as an argument to a method.

    One way to avoid this mistake is as soon as the opening character is typed,
    immediately include the closing match, then move the cursor back between them and continue coding.

    Fortunately, most modern code editors generate the second half of the pair automatically.

### Task

Fix the two pair errors in the code.

```js
let myArray = [1, 2, 3;
let arraySum = myArray.reduce((previous, current =>  previous + current);
console.log(`Sum of array values is: ${arraySum}`);
```

### Solution

```js
let myArray = [1, 2, 3];
let arraySum = myArray.reduce((previous, current) => previous + current);
console.log(`Sum of array values is: ${arraySum}`);
```

# 6-Catch Mixed Usage of Single and Double Quotes

JavaScript allows the use of both single (') and double (") quotes to declare a string. Deciding which one to use generally comes down to personal preference, with some exceptions.

    Having two choices is great when a string has contractions
    or another piece of text that's in quotes. Just be careful that you don't
    close the string too early, which causes a syntax error.

Here are some examples of mixing quotes:

```js
const grouchoContraction = "I've had a perfectly wonderful evening, but this wasn't it.";
const quoteInString = "Groucho Marx once said 'Quote me as saying I was mis-quoted.'";
const uhOhGroucho = 'I've had a perfectly wonderful evening, but this wasn't it.';
```

The first two are correct, but the third is incorrect.

    Of course, it is okay to use only one style of quotes. You can escape the quotes inside the string by using the backslash (\) escape character:

```js
const allSameQuotes =
  "I've had a perfectly wonderful evening, but this wasn't it.";
```

### Task

Fix the string so it either uses different quotes for the href value, or escape the existing ones. Keep the double quote marks around the entire string.

```js
let innerHtml = "<p>Click here to <a href="#Home">return home</a></p>";
console.log(innerHtml);
```

### Solution

```js
let innerHtml = '<p>Click here to <a href="#Home">return home</a></p>';
console.log(innerHtml);
```

# 7-Catch Use of Assignment Operator Instead of Equality Operator

Branching programs, i.e. ones that do different things if certain conditions are met, rely on if, else if, and else statements in JavaScript. The condition sometimes takes the form of testing whether a result is equal to a value.

This logic is spoken (in English, at least) as "if x equals y, then ..." which can literally translate into code using the =, or assignment operator. This leads to unexpected control flow in your program.

    As covered in previous challenges, the assignment operator (=) in JavaScript assigns
    a value to a variable name. And the == and === operators check for
    equality (the triple === tests for strict equality, meaning both
    value and type are the same).

The code below assigns x to be 2, which evaluates as true. Almost every value on its own in JavaScript evaluates to true, except what are known as the "falsy" values: false, 0, "" (an empty string), NaN, undefined, and null.

```js
let x = 1;
let y = 2;
if ((x = y)) {
} else {
}
```

In this example, the code block within the if statement will run for any value of y, unless y is falsy. The else block, which we expect to run here, will not actually run.

### Task

Fix the condition so the program runs the right branch, and the appropriate value is assigned to result.

### Solution

```js
let x = 7;
let y = 9;
let result = "to come";

if (x == y) {
  result = "Equal!";
} else {
  result = "Not equal!";
}

console.log(result);
```

# 8-Catch Missing Open and Closing Parenthesis After a Function Call

When a function or method doesn't take any arguments, you may forget to include the (empty) opening and closing parentheses when calling it.

Often times the result of a function call is saved in a variable for other use in your code. This error can be detected by logging variable values (or their types) to the console and seeing that one is set to a function reference, instead of the expected value the function returns.

The variables in the following example are different:

```js
function myFunction() {
  return "You rock!";
}
let varOne = myFunction;
let varTwo = myFunction();
```

Here varOne is the function myFunction, and varTwo is the string You rock!.

### Task

1. Fix the code so the variable result is set to the value returned from calling the function getNine.

### Solution

```js
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine();
console.log(result);
```

# 9-Using the Test Method

### Task

```js

```

### Solution

```js

```

# 9-Using the Test Method

### Task

```js

```

### Solution

```js

```

# 10-Using the Test Method

### Task

```js

```

### Solution

```js

```

# 1-Using the Test Method

### Task

```js

```

### Solution

```js

```

# 1-Using the Test Method

### Task

```js

```

### Solution

```js

```

# 1-Using the Test Method

### Task

```js

```

### Solution

```js

```
