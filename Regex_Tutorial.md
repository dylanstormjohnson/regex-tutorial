# Regex Tutorial
A README about a regular expression, or regex!!

[![Regex](https://img.shields.io/badge/Regex-Reference-blue)](https://en.wikipedia.org/wiki/Regular_expression)

- Herein lies a tutorial for a Regex, or Regular Expression, which allows for the finding of specific words or characters within a string.

- The expression we will be discussing is as follows:
  - ```/c(\W?)+h(\W?)+[i1l](\W?)+c(\W?)+k(\W?)+[e3](\W?)+n|p(\W?)+[o0](\W?)+n(\W?)+y(\W?)+t(\W?)+a(\W?)+[i1l](\W?)+[l1i]/i```

## Summary

- In this document, I will be providing you with an overview of a Regex designed to identify particular words or phrases within a string. This has many advantageous uses, such as a sacrilege and profanity filter for usernames. Perhaps you don't want the same name as an important character used for something the player can name like a location or item. Maybe you want to create a random name generator and want to make sure it doesn't generate anything sacrilegious or profane. The filter is capable of checking for specific words despite capitalization, spaces between, special characters between, and specific numbers in place of letters they look like (ie: "1" in place of "l" and "3" in place of "E"). Currently, the regex checks only for the words "chicken" and "ponytail", however, user's could expand on the concept relatively easily to add whatever words they would like.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

- This regex features "/", "(\W?)+", "[i1l]", "[e3]", "[o0]", "[l1i]", "|", and "/i".

### Anchors

- This particular regex does not include any anchors, as it may limit its useability. For instance, the common anchors of "^" to indicate the beginning and "$" to indicate the end of a pattern would allow the regex to flag "chicken" correctly, but disavow it from flagging "chickens", thus rendering the point of its functionality invalid.

### Quantifiers

- There are two quantifiers mentioned in this regex expression: "(\W?)" and "(\W?)+". Their functionality is listed below.

  - "(\W?)": This is a non-word character "\W" with the quantifier of "?" applied to it. This checks for zero or one occurrence of the element listed before. Therefore, "c(\W?)" tries to see if there is a "c" element within the string.

  - "(\W?)+": This applies the "+" quantifier to the aforementioned quantifier, allowing it to detect multiple elements in a row. Therefore, "c(\W?)+h(\W?)" tries to see if there is a "c" element followed by an "h" element within the string.

### Grouping Constructs

- These are some of the grouping constructs mentioned in this regex expression: "(\W?)", "(\W?)+", "(\W?)+[i1l]", "(\W?)+[e3]", "(\W?)+[o0]", and "(\W?)+[l1i]". Their functionality is listed below.

  -"(\W?)": This captures a single non-word character optionally.

  -"(\W?)+": This makes the aforementioned group work one or more times.

  -"(\W?)+[i1l]": This captures a particular group followed by "i", "1", or "l".

  -"(\W?)+[e3]": This captures a particular group followed by "e" or "3".

  -"(\W?)+[o0]": This captures a particular group followed by "o" or "0".

  -"(\W?)+[l1i]": This captures a particular group followed by "l", "1", or "i".

### Bracket Expressions

- There are four bracket expressions mentioned in this regex expression: "[i1l]", "[e3]", "[o0]", and "[l1i]". Their functionality is listed below.

  -"[i1l]": This checks for a set of characters to be matched (as indicated within the square brackets). In this case, the characters are: "i", "1", and "l".

  -"[e3]": This checks for a set of characters to be matched (as indicated within the square brackets). In this case, the characters are: "e" and "3".

  -"[o0]": This checks for a set of characters to be matched (as indicated within the square brackets). In this case, the characters are: "o" and "0".

  -"[l1i]": This checks for a set of characters to be matched (as indicated within the square brackets). In this case, the characters are: "l", "1", and "i".

### Character Classes

- There are two character classes in this regex expression: "\W" and "[]". Their functionality is listed below.

  -"\W": This matches any non word character.

  -"[]": This matches one instance of what is contained within the brackets (i.e.: [o0] will match "o" or "0").

### The OR Operator

- The OR operator of "|" is mentioned in this regex expression. This allows for the checking of multiple patterns, separated by "|". The designated patterns are listed below.

  -```/c(\W?)+h(\W?)+[i1l](\W?)+c(\W?)+k(\W?)+[e3](\W?)+n|```: This pattern matches elements that combine to create the word "chicken" or a word in its likeness. The "|" indicates that another pattern will follow this pattern to be checked as well.

  -```|p(\W?)+[o0](\W?)+n(\W?)+y(\W?)+t(\W?)+a(\W?)+[i1l](\W?)+[l1i]```: This pattern matches elements that combine to create the word "ponytail" or a word in its likeness. The "|" indicates that this pattern follows another pattern and is to be checked as well.

### Flags

- The "i" flag is used within this regex. This is the case-insensitive flag, indicated after the "/"'s used to identify which part of the expression should use this flag ("/" at the start of the regex and "/i" at the end). With this flag, "c" also checks for "C" and "[o0]" checks for "o", "O", and "0".

### Character Escapes

- The character escape of "/W" is used to represent a non-word character.

## Author

- This regex tutorial was written by Dylan Storm Johnson. If you have any questions regarding this or my other projects, my GitHub account is [Dylan's GitHub account] (https://github.com/dylanstormjohnson).

---
