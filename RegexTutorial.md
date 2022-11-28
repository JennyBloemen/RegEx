# Regex Tutorial : Matching an Email

## Summary

This tutorial explains how the regex (regular expression) matching an email, functions by breaking down each part of the expression and describing what it does.
Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

### Anchors

    Anchors are used to match a position before, after, or between characters. The anchors used in this regex expression for matching an email are:

    - ^ indicates the beginning of the string.
    - $ indicates the ending of the string.

### Quantifiers

    Quantifiers specify how many instances a character, group, or character class must be present in the input for a match to be found. Quantifiers in this regex include the following:

    - [+] operator, which will connect the users email name + email service + .com.
    - {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping Constructs

    A group is a part of a regex pattern enclosed in parentheses ().

    - group #1 in this expression is ([a-z0-9_\.-]+) and matches the user email name.
    - group #2 ([\da-z\.-]+) matches the email service.
    - group #3 is ([a-z\.]{2,6}) captures the .com.

### Bracket Expressions

    Bracket expressions are enclosed in a set of [] square brackets. They require a match to the list of expressions contained in the brackets. This expression for email validation includes the following:

    - [a-z0-9_\.-], matches any letter a-z and is case sensitive, matches a character 0-9 and matches the characters "\_" , "-" , and ".";
    - [\da-z\.-], matches a single digit from 0-9, any character a-z (case sensitive), and the characters "." and "-".;
    - [a-z\.] matches any character a-z(case sensitive) and the character ".".

### Character Classes

    Character classes distinguish between letters and digits. The character class in this expression is \d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44".
    - [a-z]: allows all letters in lowercase from a to z.
    - [0-9]: allows digits from 0-9.

### The OR Operator

    The "OR" Operator is designated by using the pipe character | which separates characters contained within each (....) group. Our matching email regex is not using any OR operators.

### Flags

    There are six regular expression flags in java script; i, g, m, u, and y. Each flags affects the search and this regular expression is not using any flags.

### Character Escapes

    The backslash is can be used to prepend a special character you want to escape. The following is a character escape in our regex:
    - /.

## Author

Jenny Bloemen
https://github.com/JennyBloemen/RegEx.git

## References

- https://www.ocpsoft.org/tutorials/regular-expressions/or-in-regex/
- https://www.regular-expressions.info/
- https://www.oreilly.com/library/view/regular-expressions-cookbook/9781449327453/ch04s01.html
- https://www.oreilly.com/library/view/regular-expressions-cookbook/9781449327453/ch04s01.html
- https://pynative.com/python-regex-capturing-groups/#:~:text=of%20Groups%20Matches-,What%20is%20Group%20in%20Regex%3F,'%2C%20and%20't'.
- https://learn.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions
- https://javascript.info/regexp-introduction
