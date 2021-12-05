# Six Flags Are Not a Theme Park, They're Part of Regex -- A Regex Tutorial

As humans we're hard wired to look for patterns. It makes sense that as developers we would create an expression that helps match combinations of different characters in strings. To put it simply, this is what regex (also known as regular expression) does and what we will be discussing today.

Based on how the expression is built, regex can identify specific characters in a string--it could be a whole word, a few letters, or a string of words and characters--using dynamic pattern recognition.

One of the most useful cases in which a programmer would use a regex pattern is when trying to identify an email or password within a string. Regex can also be used to search and replace words within a body of text. 

## Summary

Today we're going to look at how a regular expression, or regex, can be used to identify an email within a string of different characters. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

A regular expression (regex) is considered a literal, or a way to notate fixed code. Therefore, all regex needs to be wrapped in slash (/) characters. For example, the regex we would use to identify an email address would look like the example below. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

Just as a ship needs to be anchored in place, so does regex. Every regex starts with an anchor tag (^) and ends with a different anchor tag ($).

^ is used at the beginning of a regex. It tells the expression that this is where we are starting. The symbol ^ can be used in two ways. 

First, ^ can be used to identify an exact string match. However, when using it this way, any text following it needs to be exact. Regex is case sensitive.

^"My Home" --> This would return results with "My" or "Home"
^"my home" --> would not return any part of My Home because regex is case sensitive. 

For example, below is a bit of the regex we spoke of in the introduction. Where you see ^ followed by `[a-z0-9_-]`E, it means that the regex is looking for anything that matches the pattern of a-z0-9. 

`/^([a-z0-9_\.-]+)`

When using $, you're saying this is the end and to use regex to find any characters before it. Just like the ^ symbol, anything before $ is case sensitive. 

In the example listed below (taken from the regex we referenced in the introduction), the $ signifies the regex has come to an end and that it will only be matching patterns between the ^ and the $ symbol. 

`([a-z\.]{2,6})$/`

### Quantifiers

To put it plainly, quantifiers set limits. Specifically, they can include the minimum and maximum amount of characters your regex is looking for. Unless you set limits, a quantifier will try to find as many sequences as it can. This means you could somehow end up with 1,000 results if your quantifiers are broad enough. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In the string above, the specific quantifier is `{2,6}`. This means we want to find a match to our regex at least 2 times and no more than 6 times. 

In the whole regex, what comes before the quantifier are the search parameters. So, in our example of looking for an email address. The regex will return between 2 and 6 results of the pattern matched in these parameters: `[a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]`

### Grouping Constructs

Grouping expressions are used to group a selection of regex. What this means in English is that a grouping construct allows you to search the same string for mulitple items. Let's go back to our email search regex.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

When looking for a full email address, the regex may need to find something repetitive like mail@mail.com. To do this, the first part of the email address is grouped in (). Anything within parentheses in a regex is known as a subexpression. In our example, `([a-z0-9_\.-]+)` this first sub expression is looking for the first part of an email address. This would be the first "mail" part in our mail@mail.com example. The subexpression listed in this paragraph is looking to match something with letters from a to z, a number between 0 and 9, or an underscore or dash.

The grouping construct after the @ symbol is looking for the "mail.com" part of our email example: mail@mail.com.

### Bracket Expressions

Bracket expressions are used to find a range of characters within a string. In our example listed above (`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`) anything within the bracket is a range of characters the regex is looking to match. 

If we use the example, `[a-z0-9_\.-]`, we can see that our regex is looking for letters between a and 9, and numbers between 0 and 9. The underscore and dash also looks for and matches underscores and dashes within a string. When using this regex to find an email, we can use _ and - to find those within an email.

It's important to note that a dash in `[a-z]` will not return any dashes. When it's placed between the two parameters, the dash means find anything between a and z.

### Character Classes

Character Classes define various characters. For example, they can help the regex distinguish between numbers and letters. Let's go back to our "find an email" example. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

In the first bit: `([a-z0-9_\.-]+)` the . has no special meaning, it only looks for a literal dot. This is helpful when looking at an email address because it could pick up the . in this example address: new.name@name.com.

### The OR Operator

What if you're looking for something in the context of either/or? This is where the OR operator comes in. Defined by a single line |, the OR operator will help find things like capital and non-capital letters (t|T). This would be important in our example because it means the regex can find an email address regardless of case. Simply put, you can make your regex NOT case sensitive. 

### Flags

I know I said at the start of this tutorial that regex needs to be wrapped in the anchors ^ and $. I'm gonna blow your mind because there is an exception to this rule, and that exception is flags. These flags are placed at the end of a regex, just after the second slash.

Flags allow for additional functionality or places extra limits on your regex. There are a total of six flags (not the theme park) you can use. 

The most common flags are: 

• g -- The g stands for global search and means the regex needs to be tested against all positive matches in a string.
• i -- This is another way to make regex not case sensitive. The i flag searches all cases of a letter.
• m -- The m flag stands for multi-line. This means that an input string with multiple lines should be treated as multiple lines.

### Character Escapes

There are times when we may want to look for more than just a literal piece of text. When this happens, you can use \ to not interpret a character literally.

An example of this is finding an email address. In most bodies of text a . would be used to end a sentence, but in an email address, a . is an important component in an email address. 

Look at name@name.com. We would want to find the ".com" in every email address. Using our regex example, the character escape can be found here: `)\.(`

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Author

This quick regex tutorial was written by Elizabeth Ireland. Her writing can be found in her portfolio, which is linked below. 
You can also view her GitHub profile which is also linked below. 

If you have any questions, please feel free to reach out via email to liz.t.ireland@gmail.com

GitHub User Page: https://github.com/liztozireland 
Writing Portfolio: https://liztireland.journoportfolio.com/ 

Resources Used:

Response Request: A Full Stack Blog, Regular Expression Tutorial
https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial 

Everything you need to know about Regular Expressions by: Slawomir Chodnicki
https://towardsdatascience.com/everything-you-need-to-know-about-regular-expressions-8f622fe10b03 
Introduction to Regular Expressions - Programming with Text by: The Coding Train
https://youtu.be/7DG3kCDx53c 