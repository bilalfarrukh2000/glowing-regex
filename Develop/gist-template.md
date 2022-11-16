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
- [Details](#details)


### Grouping and Bracket Expressions

We can group characters or provide a range using brackets to match multiple patterns

```[xyz]``` Matches any one of the enclosed characters

A range can also be specified.
```[0-0]``` matches any character between ```0``` and ```9```

The ```+``` sign indicates one or more occurences of the preceding element

```ab+c``` matches ```abc```, ```abbc```, ```abbbc```, and so on, but not ```ac```


### Quantifiers

Quantifiers specify how many instances of a character should be in the input for a match

Examples:

```{n}``` Matches exactly n times

```{n,m}``` Matches from n to m times.


### Anchors

Anchors do not match any characters, rather they tell the regex engine where matches can begin and end

```^```  anchor is called a Caret and it fixes a regex match to the beginning of a line
```$``` anchor is called a dollar and it fixes a regex to match the end of a line

As can be seen, the email regex has a caret at the start and a dollar at the end



### Character Classes

Character classes tell the regex engine to match only one out of several character types.

Examples:

```\w``` Matches any alphanumeric character from the basic latin alphabet 
```\d``` Matches any digit. Equivalent to ```[0-9]```
```.``` Matches any character except a newline
```\.``` Matches a period. The backslash indicates that the following character should be treated as an "escaped" character



### Details

```^``` specifies the start anchor

```/^([a-z0-9_\.-]+)``` matches lowercase letters between a-z, numbers between 0-9, and ```_```, ```.``` or ```-```

An @ sign must be present after this

```([\da-z\.-]+)```  matches a domain pattern that can be digits, a letter between a and z and ```_```, ```.``` or ```-```

After the domain a period must follow

```([a-z\.]{2,6})``` Matches a group of letters or periods 2-6 characters long.

```$``` is the end anchor which marks the end of the regex


## Author

Bilal Farrukh holds an Associate Degree in Business Information Systems. He loves to watch and play sports. He also loves videogames.
GitHub Profile: https://github.com/bilalfarrukh2000/
