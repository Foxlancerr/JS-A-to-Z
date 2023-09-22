# Regular Expressions

    Regular expressions, often shortened to "regex" or "regexp",
    are patterns that help programmers match, search, and replace text.
    Regular expressions are very powerful, but can be hard to read
    because they use special characters to make more complex, flexible matches.

    In this course, you'll learn how to use special characters, capture groups,
    positive and negative lookaheads, and other techniques to match any text you want.

# Total Lessons (33)

# 1-Using the Test Method

    Regular expressions are used in programming languages to match parts of strings.
    You create patterns to help you do that matching.

If you want to find the word the in the string The dog chased the cat, you could use the following regular expression: /the/. Notice that quote marks are not required within the regular expression.

- JavaScript has multiple ways to use regexes.
  One way to test a regex is using the .test() method. The .test() method takes the regex, applies it to a string (which is placed inside the parentheses), and returns true or false if your pattern finds something or not.

```js
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr);
```

The test method here returns true.

### Task

Apply the regex myRegex on the string myString using the .test() method.

```js
let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex;
```

### Solution

```js
let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex.test(myString);
// Change this line
console.log(result);
```

# 2-Match Literal Strings

    In the last challenge, you searched for the word Hello using the regular expression /Hello/.
    That regex searched for a literal match of the string Hello.
    Here's another example searching for a literal match of the string Kevin:

```js
let testStr = "Hello, my name is Kevin.";
let testRegex = /Kevin/;
testRegex.test(testStr);
```

This test call will return true.

Any other forms of Kevin will not match. For example, the regex /Kevin/ will not match kevin or KEVIN.

```js
let wrongRegex = /kevin/;
wrongRegex.test(testStr);
```

This test call will return false.

A future challenge will show how to match those other forms as well.

### Task

Complete the regex waldoRegex to find "Waldo" in the string waldoIsHiding with a literal match.

```js
let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
let waldoRegex = /search/; // Change this line
let result = waldoRegex.test(waldoIsHiding);
```

### Solution

```js
let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
let waldoRegex = /Waldo/; // Change this line
let result = waldoRegex.test(waldoIsHiding);
console.log(result);
```

# 3-Match a Literal String with Different Possibilities

    Using regexes like /coding/, you can look for the pattern coding in another string.

This is powerful to search single strings, but it's limited to only one pattern. You can search for multiple patterns using the alternation or OR operator: |.

This operator matches patterns either before or after it. For example, if you wanted to match the strings yes or no, the regex you want is /yes|no/.

You can also search for more than just two patterns. You can do this by adding more patterns with more OR operators separating them, like <code>/yes|no|maybe/</code>

### Task

Complete the regex petRegex to match the pets dog, cat, bird, or fish.

```js
let petString = "James has a pet cat.";
let petRegex = /change/; // Change this line
let result = petRegex.test(petString);
```

### Solution

```js
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/; // Change this line
let result = petRegex.test(petString);
```

# 4-Ignore Case While Matching

Up until now, you've looked at regexes to do literal matches of strings.

But sometimes, you might want to also match case differences.

    Case (or sometimes letter case) is the difference between
    uppercase letters and lowercase letters. Examples of uppercase
    are A, B, and C. Examples of lowercase are a, b, and c.

You can match both cases using what is called a flag. There are other flags but here you'll focus on the flag that ignores case -the i flag.

    You can use it by appending it to the regex. An example of using this flag is /ignorecase/i.

```js
let fccRegex = /freecodecamp/i;
// here i flag is used to handle case insensitive,ingnore lowercase and uppercase and treated as same.
```

This regex can match the strings ignorecase, igNoreCase, and IgnoreCase.

### Task

Write a regex fccRegex to match freeCodeCamp, no matter its case. Your regex should not match any abbreviations or variations with spaces.

```js
let myString = "freeCodeCamp";
let fccRegex = /change/; // Change this line
let result = fccRegex.test(myString);
```

### Solution

```js
let myString = "freeCodeCamp";
let fccRegex = /freecodecamp/i;
let result = fccRegex.test(myString);
console.log(result);
```

# 5-Extract Matches

So far, you have only been checking if a pattern exists or not within a string. You can also extract the actual matches you found with the .match() method.

    To use the .match() method, apply the method on a string and pass in the regex inside the parentheses.

Here's an example:

```js
"Hello, World!".match(/Hello/);
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
```

Here the first match would return ["Hello"] and the second would return ["expressions"].

### Note

That the .match syntax is the "opposite" of the .test method you have been using thus far:

```js
"string".match(/regex/);
/regex/.test("string");
```

### Task

Apply the .match() method to extract the string coding.

```js
let extractStr = "Extract the word 'coding' from this string.";
let codingRegex = /change/; // Change this line
let result = extractStr; // Change this line
```

### Solution

```js
let extractStr = "Extract the word 'coding' from this string.";
let codingRegex = /coding/i; // Change this line
let result = extractStr.match(codingRegex); // Change this line
```

# 6-Find More Than the First Match

So far, you have only been able to extract or search a pattern once.

```js
let testStr = "Repeat, Repeat, Repeat";
let ourRegex = /Repeat/;
testStr.match(ourRegex);
```

Here match would return ["Repeat"].

To search or extract a pattern more than once, you can use the <code>global search flag: g</code>

```js
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
```

And here match returns the value ["Repeat", "Repeat", "Repeat"]

### Task

Using the regex starRegex, find and extract both Twinkle words from the string twinkleStar.

### Note

You can have multiple flags on your regex like /search/gi

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /change/; // Change this line
let result = twinkleStar; // Change this line
```

### Solution

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /twinkle/gi; // Change this line
let result = twinkleStar.match(starRegex); // Change this line
console.log(result);
```

# 7-Match Anything with Wildcard Period

    Sometimes you won't (or don't need to) know the exact characters in your patterns.
    Thinking of all words that match, say, a misspelling would take a long time.
    Luckily, you can save time using the wildcard character: .

The wildcard character <code>.</code> will match any one character. The wildcard is also called dot and period. You can use the wildcard character just like any other character in the regex.

### For example

if you wanted to match hug, huh, hut, and hum, you can use the regex /hu./ to match all four words.

```js
let humStr = "I'll hum a song";
let hugStr = "Bear hug";
let huRegex = /hu./;
huRegex.test(humStr);
huRegex.test(hugStr);
```

Both of these test calls would return true.

### Task

1. Complete the regex unRegex so that it matches the strings run, sun, fun, pun, nun, and bun. Your regex should use the wildcard character.

```js
let exampleStr = "Let's have fun with regular expressions!";
let unRegex = //change this
let result = unRegex.test(exampleStr);
// here we used dot notation which allow all the match words
```

### Solution

```js
let exampleStr = "Let's have fun with regular expressions!";
let unRegex = /.un/i;
let result = unRegex.test(exampleStr);
// here we used dot notation which allow all the match words
```

# 8-Match Single Character with Multiple Possibilities

You learned how to match literal patterns (/literal/) and wildcard character (/./). Those are the extremes of regular expressions, where one finds exact matches and the other matches everything. There are options that are a balance between the two extremes.

    You can search for a literal pattern with some flexibility with character classes.
    Character classes allow you to define a group of characters
    you wish to match by placing them inside square ([ and ]) brackets.

### For example

you want to match bag, big, and bug but not bog. You can create the regex /b[aiu]g/ to do this. The [aiu] is the character class that will only match the characters a, i, or u.

```js
let bigStr = "big";
let bagStr = "bag";
let bugStr = "bug";
let bogStr = "bog";
let bgRegex = /b[aiu]g/;
bigStr.match(bgRegex);
bagStr.match(bgRegex);
bugStr.match(bgRegex);
bogStr.match(bgRegex);
```

In order, the four match calls would return the values ["big"], ["bag"], ["bug"], and null.

### Task

1. Use a character class with vowels (a, e, i, o, u) in your regex vowelRegex to find all the vowels in the string quoteSample.

2. Note:Be sure to match both upper- and lowercase vowels.

```js
let quoteSample =
  "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /change/; // Change this line
let result = vowelRegex; // Change this line
```

### Solution

```js
let quoteSample =
  "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /[aeiou]/gi; // here is solution
let result = quoteSample.match(vowelRegex); // Change this line
```

# 9-Match Letters of the Alphabet

You saw how you can use character sets to specify a group of characters to match, but that's a lot of typing when you need to match a large range of characters (for example, every letter in the alphabet). Fortunately, there is a built-in feature that makes this short and simple.

Inside a character set, you can define a range of characters to match using a hyphen character: -.

For example, to match lowercase letters a through e you would use [a-e].

```js
let catStr = "cat";
let batStr = "bat";
let matStr = "mat";
let bgRegex = /[a-e]at/;
catStr.match(bgRegex);
batStr.match(bgRegex);
matStr.match(bgRegex);
```

In order, the three match calls would return the values ["cat"], ["bat"], and null.

### Task

- Match all the letters in the string quoteSample.

- Note: Be sure to match both uppercase and lowercase letters.

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /change/; // Change this line
let result = alphabetRegex; // Change this line
```

### Solution

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /[a-z]/gi; // Change this line
let result = quoteSample.match(alphabetRegex); // Change this line
```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```

# 1-

### Task

```js

```

### Solution

```js

```