# Email Matching Regex Tutorial

This is a tutorial on the matching email regular expression, or regex for short. Hopefully by the end of this tutorial, you will have a deeper understanding of regex components. In this case study, we will break down the components of the matching email regex and explain how each part makes email validation work.

## Summary

We will breaking down the regex below. We will see the different components of a regex: anchors, quantifiers, grouping constucts, bracket expressions, character classes, the or operator, flags, and character escapes.

The Regex that we will be focusing on is:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Summary](#summary)

## Regex Components

### Anchors

Anchors are special characters that definte the position of the pattern inside of the input string. The anchors that are used in this regex are `^` , which shows the beginning of the string and `$`, wich shows the end. Some other regex may use `m` to indicate multi lines but that is not used here.

These achors ensure that the pattern mathces both the start and end of the string. This is important for our regex becuase we need to make sure the input string matches the enitre pattern in order, not just a snippet.

### Quantifiers

Quanifiers specify the minnimum and maximum times the pattern should mathces. This regex uses `+` and `{2,6}` to show how many times the preceding character should occur. The `+` specifies that the email user name shoudl connect to email provider and then .com. The `{2,6}` specifies that there should be 2-6 characters that match the correct character set. This the first `+)` matches on or more lowercase letters, numbers, underscores or dots. There should be then an `@`. In between the first `a`and the second `+` show shows there should be a string that matches one or more lowercase letters, numbers, underscores, dots, or hypehns. The `{2,6}` should be 2-6 characters, for exmaple .com.

### Grouping Constructs

Grouping constructs group together at least one charcter and treat them as one in the expression. They are grouped together using parentehsis.

In this expression our grouping constructs are:
`([a-z0-9_\.-]+)` user name
`([\da-z\.-]+)` email provider
`([a-z\.]{2,6})` - domain ending

### Bracket Expressions

Bracket expressions define a set of characters that can be matched in a text string. They are enclosed in square brackets. For example, in our regex there are three bracket expressions.

`[a-z0-9_\.-]` string inputs must be lower case letter a-z, digit 0-9, underscore, period, or hyphen
`[\da-z\.-]` string inputs must be a nubmer 0-9 or a-z. /d is short for 0-9
`[a-z]` stinrg in put must be lower case letter a-z

### Character Classes

Character classes are defined within square brackets and show the range of which the characters of the input can match. They are a sub division fo bracket classes. While bracket classes can be more vauge character classes show which characters can be matched.

### The OR Operator

The OR operator allows acceptable alterative patterns. This regex does not feature any operators which makes sense since emails need to have this exact pattern.

### Flags

Flags can modify a regex by enabling or disabling certain features by appending certain characters outside of slashes. However, this regex does not use any flags.

### Character Escapes

Character escapes allow you to use characters that may mean something else in the code.
In our regex, our . is escaped by a backslash. A . can mean something else in regex's uusally but if we just want to use it as string text we can add a character escape.

### Summary

By combining all of these parts, the regex can make sure that the email adress is properly strucutred.

Start
`/^`

username (any regular letters, number, underscore, or period) +
`([a-z0-9_\.-]+)`

@sign
`@`

email provider(any regular letters) +

`([\da-z\.-]+)\`

. before domain ending
`.`

domain ending (any regular letters)
`([a-z\.]{2,6})`

End
`$/`

## Author

I'm Aileen, a new web developer that is practicing my knowledge my creating tutorials so that I can understand concepts a little better. Hopefully this helped you out too!

If you want to see more of my work or have any questions or comments checkout my [Github](https://github.com/nguyenaileen)
