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

# 9-Match Numbers and Letters of the Alphabet

    Using the hyphen (-) to match a range of characters is not limited to letters.
    It also works to match a range of numbers.

For example, /[0-5]/ matches any number between 0 and 5, including the 0 and 5.

Also, it is possible to combine a range of letters and numbers in a single character set.

```js
let jennyStr = "Jenny8675309";
let myRegex = /[a-z0-9]/gi;
jennyStr.match(myRegex);
```

### Task

Create a single regex that matches a range of letters between h and s, and a range of numbers between 2 and 6. Remember to include the appropriate flags in the regex.

```js
let quoteSample = "Blueberry 3.141592653s are delicious.";
let myRegex = /change/; // Change this line
let result = myRegex; // Change this line
```

### Solution

```js
let quoteSample = "Blueberry 3.141592653s are delicious.";
let myRegex = /[h-s2-6]/gi; // Change this line
let result = quoteSample.match(myRegex); // Change this line
```

# 10-Match Single Characters Not Specified

So far, you have created a set of characters that you want to match,

    but you could also create a set of characters that you do not want to match.
    These types of character sets are called negated character sets.

    To create a negated character set, you place a caret character (^) after the opening bracket and before the characters you do not want to match.

For example,

    /[^aeiou]/gi

    matches all characters that are not a vowel. Note that characters like ., !, [, @, / and white space are matched - the negated vowel character set only excludes the vowel characters.

### Task

Create a single regex that matches all characters that are not a number or a vowel. Remember to include the appropriate flags in the regex.

### Solution

```js
let quoteSample = "3 blind mice.";
let myRegex = /[^aeiou1-9]/gi; // Change this line
let result = quoteSample.match(myRegex);
console.log(result);
```

# 11-Match Characters that Occur One or More Times

    Sometimes, you need to match a character (or group of characters)
    that appears one or more times in a row. This means it
    occurs at least once, and may be repeated.

You can use the + character to check if that is the case. Remember, the character or pattern has to be present consecutively. That is, the character has to repeat one after the other.

For example,

    /a+/g
    would find one match in abc and return ["a"]. Because of the +, it would also find a single match in aabc and return ["aa"].

If it were instead checking the string abab, it would find two matches and return ["a", "a"] because the a characters are not in a row - there is a b between them. Finally, since there is no a in the string bcd, it wouldn't find a match.

### Task

You want to find matches when the letter s occurs one or more times in Mississippi. Write a regex that uses the + sign.

### Solution

```js
let difficultSpelling = "Mississippi";
let myRegex = /s+/gi; // Change this line
let result = difficultSpelling.match(myRegex);
console.log(result);
```

# 12-Match Characters that Occur Zero or More Times

The last challenge used the plus + sign to look for characters that occur one or more times.

    There's also an option that matches characters that occur zero or more times.

The character to do this is the asterisk or star: \*.

```js
let soccerWord = "gooooooooal!";
let gPhrase = "gut feeling";
let oPhrase = "over the moon";
let goRegex = /go\*/;
soccerWord.match(goRegex);
gPhrase.match(goRegex);
oPhrase.match(goRegex);
```

In order, the three match calls would return the values ["goooooooo"], ["g"], and null.

### Task

For this challenge, chewieQuote has been initialized as the string Aaaaaaaaaaaaaaaarrrgh! behind the scenes. Create a regex chewieRegex that uses the \* character to match an uppercase A character immediately followed by zero or more lowercase a characters in chewieQuote. Your regex does not need flags or character classes, and it should not match any of the other quotes.

### Solution

```js
// Only change code below this line
let chewieRegex = /Aa*/; // Change this line
// Only change code above this line

let result = chewieQuote.match(chewieRegex);
console.log(result);
```

# 13-Find Characters with Lazy Matching

In regular expressions, a greedy match finds the longest possible part of a string that fits the regex pattern and returns it as a match. The alternative is called a lazy match, which finds the smallest possible part of the string that satisfies the regex pattern.

You can apply the regex <code>/t[a-z]\*i/</code>to the string "titanic". This regex is basically a pattern that starts with t, ends with i, and has some letters in between.

Regular expressions are by default greedy, so the match would return <code>["titani"]</code>. It finds the largest sub-string possible to fit the pattern.

However, you can use the ? character to change it to lazy matching. "titanic" matched against the adjusted regex of <code>/t[a-z]\*?i/</code> returns ["ti"].

### Note:

Parsing HTML with regular expressions should be avoided, but pattern matching an HTML string with regular expressions is completely fine.

### Task

1. Fix the regex <code>/<.\*>/</code> to return the HTML tag <h1\> and not the text "<h1\>Winter is coming</h1>". Remember the wildcard . in a regular expression matches any character.

### Solution

```js
let text = "<h1>Winter is coming</h1>";
let myRegex = /<.*?>/i; // Change this line
let result = text.match(myRegex);
console.log(result);
```

# 14-Find One or More Criminals in a Hunt

Time to pause and test your new regex writing skills. A group of criminals escaped from jail and ran away, but you don't know how many. However, you do know that they stay close together when they are around other people. You are responsible for finding all of the criminals at once.

Here's an example to review how to do this:

The regex /z+/ matches the letter z when it appears one or more times in a row. It would find matches in all of the following strings:

```js
"z";
"zzzzzz";
"ABCzzzz";
"zzzzABC";
"abczzzzzzzzzzzzzzzzzzzzzabc";
```

But it does not find matches in the following strings since there are no letter z characters:

```js
"";
"ABC";
"abcabc";
```

### Task

Write a greedy regex that finds one or more criminals within a group of other people. A criminal is represented by the capital letter C.

### Solution

```js
let reCriminals = /C+/; // Change this line
let str = "P1P5P4CCCcP2P6P3";
const res = str.match(reCriminals);
console.log(res);
```

# 15-Match Beginning String Patterns

Prior challenges showed that regular expressions can be used to look for a number of matches. They are also used to search for patterns in specific positions in strings.

In an earlier challenge, you used the caret character (^) inside a character set to create a negated character set in the form [^thingsThatWillNotBeMatched]. Outside of a character set, the caret is used to search for patterns at the beginning of strings.

```js
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
```

The first test call would return true, while the second would return false.

### Task

Use the caret character in a regex to find Cal only in the beginning of the string rickyAndCal.

### Solution

```js
let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /^Cal/; // Change this line
let result = calRegex.test(rickyAndCal);
let result1 = rickyAndCal.match(calRegex);
console.log(result);
console.log(result1);
```

# 16-Match Ending String Patterns

In the last challenge, you learned to use the caret character to search for patterns at the beginning of strings. There is also a way to search for patterns at the end of strings.

You can search the end of strings using the dollar sign character $ at the end of the regex.

```js
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding);
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding);
```

The first test call would return true, while the second would return false.

### Task

Use the anchor character ($) to match the string caboose at the end of the string caboose.

### Solution

```js
let caboose = "The last car on a train is the caboose";
let lastRegex = /caboose$/; // Change this line
let result = lastRegex.test(caboose);
let result1 = caboose.match(lastRegex);
console.log(result);
console.log(result1);
```

# 17-Match All Letters and Numbers

Using character classes, you were able to search for all letters of the alphabet with [a-z]. This kind of character class is common enough that there is a shortcut for it, although it includes a few extra characters as well.

The closest character class in JavaScript to match the alphabet is \w. This shortcut is equal to [A-Za-z0-9_]. This character class matches upper and lowercase letters plus numbers. Note, this character class also includes the underscore character (\_).

```js
let longHand = /[A-Za-z0-9_]+/;
let shortHand = /\w+/;
let numbers = "42";
let varNames = "important_var";
longHand.test(numbers);
shortHand.test(numbers);
longHand.test(varNames);
shortHand.test(varNames);
```

All four of these test calls would return true.

These shortcut character classes are also known as shorthand character classes.

### Task

1. Use the shorthand character class \w to count the number of alphanumeric characters in various quotes and strings.

### Solution

```js
let quoteSample = "The five boxing wizards jump quickly.";
let alphabetRegexV2 = /\w/g; // Change this line
let result = quoteSample.match(alphabetRegexV2).length;
console.log(result);
```

# 18-Match Everything But Letters and Numbers

You've learned that you can use a shortcut to match alphanumerics [A-Za-z0-9_] using \w. A natural pattern you might want to search for is the opposite of alphanumerics.

You can search for the opposite of the \w with \W. Note, the opposite pattern uses a capital letter. This shortcut is the same as [^A-Za-z0-9_].

```js
let shortHand = /\W/;
let numbers = "42%";
let sentence = "Coding!";
numbers.match(shortHand);
sentence.match(shortHand);
```

The first match call would return the value ["%"] and the second would return ["!"].

### Task

1. Use the shorthand character class \W to count the number of non-alphanumeric characters in various quotes and strings.

### Solution

```js
let quoteSample = "The five boxing wizards jump quickly.";
let nonAlphabetRegex = /\W/g; // Change this line
let result = quoteSample.match(nonAlphabetRegex).length;
console.log(result);
```

# 19-Match All Numbers

You've learned shortcuts for common string patterns like alphanumerics. Another common pattern is looking for just digits or numbers.

The shortcut to look for <code>digit characters is \d</code>, with a lowercase d. This is equal to the character class [0-9], which looks for a single character of any number between zero and nine.

### Task

Use the shorthand character class \d to count how many digits are in movie titles. Written out numbers ("six" instead of 6) do not count.

### Solution

```js
let movieName = "2001: A Space Odyssey";
let numRegex = /\d/g; // Change this line
let result = movieName.match(numRegex).length;
console.log(result);
```

# 20-Match All Non-Numbers

The last challenge showed how to search for digits using the shortcut \d with a lowercase d.

You can also search for non-digits using a similar shortcut that uses an <code>uppercase \D</code> instead.

The shortcut to look for non-digit characters is \D. This is equal to the character class [^0-9], which looks for a single character that is not a number between zero and nine.

### Task

Use the shorthand character class for non-digits \D to count how many non-digits are in movie titles.

### Solution

```js
let movieName = "2001: A Space Odyssey";
let noNumRegex = /\D/g; // Change this line
let result = movieName.match(noNumRegex).length;
console.log(result);
```

# 21-Restrict Possible Usernames

Usernames are used everywhere on the internet. They are what give users a unique identity on their favorite sites.

You need to check all the usernames in a database. Here are some simple rules that users have to follow when creating their username.

- Usernames can only use alpha-numeric characters.
- The only numbers in the username have to be at the end. There can be zero or more of them at the end.
- Username cannot start with the number.
- Username letters can be lowercase and uppercase.
- Usernames have to be at least two characters long. - A two-character username can only use alphabet letters as characters.

### Task

Change the regex userCheck to fit the constraints listed above.

### Solution

```js
let username = "JackOfAllTrades";
let userCheck = /^[a-z][a-z]+\d*$|[a-z]\d\d+$/gi; // Change this line
let result = username.match(userCheck);
console.log(result);
```

### Code Explanation

- ^ - start of input
- [a-z] - first character is a letter
- [a-z]+ - following characters are letters
- \d\*$ - input ends with 0 or more digits
- | - or
- ^[a-z] - first character is a letter
- \d\d+ - following characters are 2 or more digits
- $ - end of input

# 22-Match Whitespace

The challenges so far have covered matching letters of the alphabet and numbers. You can also match the whitespace or spaces between letters.

You can search for whitespace using <code>\s</code>, which is a lowercase s.

This pattern not only matches whitespace, but also carriage return, tab, form feed, and new line characters. You can think of it as similar to the character class [ \r\t\f\n\v].

```js
let whiteSpace = "Whitespace. Whitespace everywhere!";
let spaceRegex = /\s/g;
whiteSpace.match(spaceRegex);
```

This match call would return [" ", " "].

### Task

Change the regex countWhiteSpace to look for multiple whitespace characters in a string.

### Solution

```js
let sample = "Whitespace is important in separating words";
let countWhiteSpace = /\s/g; // Change this line
let result = sample.match(countWhiteSpace);
console.log(result);
```

# 23-Match Non-Whitespace Characters

You learned about searching for whitespace using \s, with a lowercase s. You can also search for everything except whitespace.

Search for non-whitespace using <code>\S</code>, which is an uppercase s.

This pattern will not match whitespace, carriage return, tab, form feed, and new line characters. You can think of it being similar to the character class [^ \r\t\f\n\v].

```js
let whiteSpace = "Whitespace. Whitespace everywhere!";
let nonSpaceRegex = /\S/g;
whiteSpace.match(nonSpaceRegex).length;
```

The value returned by the .length method would be 32.

### Task

Change the regex countNonWhiteSpace to look for multiple non-whitespace characters in a string.

### Solution

```js
let sample = "Whitespace is important in separating words";
let countNonWhiteSpace = /\S/g; // Change this line
let result = sample.match(countNonWhiteSpace);
console.log(result);
```

<hr>

# 24-Specify Upper and Lower Number of Matches

Recall that you use the plus sign + to look for one or more characters and the asterisk \* to look for zero or more characters. These are convenient but sometimes you want to match a certain range of patterns.

    You can specify the lower and upper number of patterns with quantity specifiers.

Quantity specifiers are used with <code>curly brackets ({</code> and <code>})</code>. You put two numbers between the curly brackets - for the lower and upper number of patterns.

For example, to match only the letter a appearing between 3 and 5 times in the string ah, your regex would be /a{3,5}h/.

```js
let A4 = "aaaah";
let A2 = "aah";
let multipleA = /a{3,5}h/;
multipleA.test(A4);
multipleA.test(A2);
```

The first test call would return true, while the second would return false.

### Task

Change the regex ohRegex to match the entire phrase Oh no only when it has 3 to 6 letter h's.

### Solution

```js
let ohStr = "Ohhh no";
let ohRegex = /oh{3,6}\sno/gi; // Change this line
let result = ohStr.match(ohRegex);
console.log(result);
```

<hr>

# 25-Specify Only the Lower Number of Matches

You can specify the lower and upper number of patterns with quantity specifiers using curly brackets.

    Sometimes you only want to specify the lower number of patterns with no upper limit.

To only specify the lower number of patterns, keep the first number followed by a comma.

For example, to match only the string hah with the letter a appearing at least 3 times, your regex would be /ha{3,}h/.

```js
let A4 = "haaaah";
let A2 = "haah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleA = /ha{3,}h/;
multipleA.test(A4);
multipleA.test(A2);
multipleA.test(A100);
```

In order, the three test calls would return true, false, and true.

### Task

Change the regex haRegex to match the word Hazzah only when it has four or more letter z's.

### Solution

```js
let haStr = "Hazzzzah";
let haRegex = /haz{4,}ah/gi; // Change this line
let result = haStr.match(haRegex);
console.log(result);
```

<hr>

# 26-Specify Exact Number of Matches

You can specify the lower and upper number of patterns with quantity specifiers using curly brackets. Sometimes you only want a specific number of matches.

To specify a certain number of patterns, just have that one number between the curly brackets.

For example, to match only the word hah with the letter a 3 times, your regex would be /ha{3}h/.

```js
let A4 = "haaaah";
let A3 = "haaah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleHA = /ha{3}h/;
multipleHA.test(A4);
multipleHA.test(A3);
multipleHA.test(A100);
```

In order, the three test calls would return false, true, and false.

### Task

Change the regex timRegex to match the word Timber only when it has four letter m's.

### Solution

```js
let timStr = "Timmmmber";
let timRegex = /tim{4}ber/gi; // Change this line
let result = timRegex.test(timStr);
```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```

<hr>

# 23-

### Task

```js

```

### Solution

```js

```
