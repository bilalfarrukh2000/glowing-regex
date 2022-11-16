# Regex

Regular Expressions (regex) are expressions used to match string patterns

## Summary

The regex below determines if a string is an email address or not. This can be extremely useful for login form data validation

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Grouping and Bracket Expressions](#grouping-and-bracket-expressions) 
- [Quantifiers](#quantifiers)
- [Anchors](#anchors)
- [Character Classes](#character-classes)
- [Explanation](#explanation)


### Anchors

Anchors do not match any characters, rather they tell the regex engine where matches can begin and end

```^```  anchor is called a Caret and it fixes a regex match to the beginning of a line
```$``` anchor is called a dollar and it fixes a regex to match the end of a line

As can be seen, the email regex has a caret at the start and a dollar at the end

### Quantifiers

Quantifiers specify how many instances of a character should be in the input for a match

Examples:

```{n}``` Matches exactly n times

```{n,m}``` Matches from n to m times.


### Character Classes

Character classes tell the regex engine to match only one out of several character types.

Examples:

```\w``` Matches any alphanumeric character from the basic latin alphabet 
```\d``` Matches any digit. Equivalent to ```[0-9]```
```.``` Matches any character except a newline
```\.``` Matches a period. The backslash indicates that the following character should be treated as an "escaped" character



