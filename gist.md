# Email Matching Using Regex

This tutorial will demonstrate and breakdown how you can use regular expressions (regex) to match email addresses using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. A useful tool when validating email addresses using technologies like Node.js.

## Summary

A regular expression, commonly referred to as regex are a sequence of characters that defines a search pattern. Depending on what you are wanting to find you can modify the expression to achieve just that. In this tutorial I will explain how you can use regex to match email addresses.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)

## Regex Components

### Anchors

They match a position before, after, or between characters. `^` is used to matches the position before the first character in a string and `$` matches the position after the last character in a string. As you will see in our example expression above.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. We use the `+` operator to connect the different components as well as the `{2,6}` quantifier to say the tail of the email should be between 2 and 6 characters.

### OR Operator

Using the pipe charcacter `|` you can match characters on the left and right of the `|` operator. This is not being used in our example.

### Character Classes

A set of characters inside of square brackets `[]`. You can do numerous types of Character Class searches depending on what you are wanting. We are using 3 different character classes. One each to filter the username `[a-z0-9_\.-]`, second-level domain `[\da-z\.-]`, and the top-level domain `[a-z\.]`.

### Flags

An optional parameter to a regex that modifies its behaviour of searching. Here are some of the flags:

<li>( d ) Generate indices for substring matches</li> 
<li>( i ) Case-insensitive search</li>
<li>( g ) Global</li>
<li>( s ) Dot All</li>
<li>( m ) Multiline</li>
<li>( y ) Sticky</li>
<li>( u ) Unicode</li>

We are not using any flags in our example.

### Grouping and Capturing

If you place part of a regular expression in parentheses, you group that part of the regex together. Allowing you to apply a quantifier to the entire group or to restrict to part of the regex. Similar to the Character classes, we are capturing 3 different groups. The username `([a-z0-9_\.-]+)`, the second-level domain `([\da-z\.-]+)`, and the top-level domain `([a-z\.]{2,6})`.

### Bracket Expressions

Use bracket expressions to match single characters in a list, or a range of characters in a list. If the first character of the list is the carat `^` then it matches characters that are not in the list. In our example of the username we use `[a-z0-9_\.-]` which says it will accept and lower case letter `a-z`, numbers `0-9` and `.` or `-` characters.

### Greedy and Lazy Match

In the greedy mode (by default) a quantified character is repeated as many times as possible. We use the `+` quantifier to give back as many matches as possible. As well as the `{}` operater.

Laziness is only enabled for the quantifier with `?`. The regexp engine tries to match the rest of the pattern before each repetition of the quantified character.

### Boundaries

Boundary markers such as `\b` allow you to match positions where one side is a work charcter and the other side is not a word character such as a space character. Not used in the example.

## Author

If you would like to view more of my work you can checkout my [GitHub](https://github.com/imjustSahen)
