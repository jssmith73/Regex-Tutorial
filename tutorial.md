# Regex HTML Match Tutorial

Welcome to my Regex tutorial for matching a HTML tag.

## Summary

This tutorial breaks down the following regex expression used to identify a HTML tag. 

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

## Table of Contents

- [Anchors](#anchors)
- [Grouping Constructs](#grouping-contructs)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)

## Regex Components

### Anchors

The symbols ^ and $ are both considered to be anchors. The ^ signifies a string that begins with the characters that follow it, in this case: '<'. This can be in the format of '^For' where the string begins with the word For but not 'for' due to case sensitivity, or in the form of curly brackets which refer to a range of matches. This will be explained in more detailed in the following sections.

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
 ^                                       ^

### Grouping Constructs

As a regex gets longer and more complicated, you can check multiple parts of a string to see if different parts meet different requirements. To break these sections into different parts you use Grouping Constructs. The way to use these is with parentheses (()). Each group inside of these is call a subexpression. The following example is of two seperate subexpressions: (123):(456)

The first subexpression in looking for the part of a string that matches '123' exactly. The same concept for the second group but looking for '456'.

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
   ^      ^^     ^ ^   ^  ^             ^

### Bracket Expressions

Brackets expressions are for finding a range of characters between square brackets ([]). An example for this is [abcdefg]. This expression will look for a string with a b c d e f or g. So any of the following would match: "brad", "grad", "abra", "caged", "grabbed", etc.

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
    ^   ^   ^  ^  

### Quantifiers

Quantifiers set limits for the string that the regex matches. They include the minimum and maximum number a characters your regex is looking for. Quantifiers match as many occurrences of particular patterns as possible. Including:

* - Matches the pattern zero or more times

+ - Matches the pattern one or more times

? - Matches the pattern zero or one time

{} - Curly brackets can provide three different way to set limits for a match: 
 
 1. { n } - Matches the patter exactly n number of times

 2. { n, } - Matches the pattern at least n number of times

 3. { n, x } - Matches the pattern from a minimum of n number of times to a maximum of x number of times


 Each quantifier can be made 'lazy' by adding the ? symbol afterwards. This means it will match as few times as possible.

 /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
          ^      ^ ^      ^          ^

 
### OR Operator 

The OR operator is used to match one of two or more expressions. It is placed between two expressions using "|".

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
                                 ^ 

### Character Classes

A character class in a regex defines a set of characters, any of which can occur in an input string to find a match.

. - Matches any character except the newline character (/n)

\d - Matches number digits. This class is the same as the bracket expression [0-9]

\w - Matches alphanumeric charaters from the basic Latin alphabet, including the underscore (_)

\s - Matches a single whitespace character, including tabs and line breaks

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
                                   ^

### Flags

Flags are placed at the end of a regex, after the second slash, and they define functionalitiy or limits for the regex. The three most likely to be used are: 

Global (g) - The regex should be tested against all possible matches in a string

Case Insensitive Search (i) - Case should be ignored while attempting a match in a string

Multi-line Search (m) - Mulit-line inputs should be tested as mulitiple lines


## Author

My name is Josiah Smith and I am a Junior Web Developer. 
I wrote this tutorial as a project for my university but I hope it comes in handy to someone besides myself one day.
Any notes or constructive criticism can be forwarded to me at:

Github: https://github.com/jssmith73

Email: josiahsmith1359@gmail.com