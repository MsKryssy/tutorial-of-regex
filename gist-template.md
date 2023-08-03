# Tutorial of Regex

This will be a short tutorial of Regex and an overview of its components. This gist file will assist with
remembering and understanding how Regex works and its use when working with it. Although this is my first week 
reviewing Regex, its powerful patterns used for text matching and manipulation is supported in many programming
languages and text editors.

## Summary

The Regex I will be describing is the Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Regex Components are: Anchors, Quantifiers, Grouping Constructs, Bracket Expressions, Character Classes, OR Operators, Flags, and Character Escapes.

### Anchors

Anchors are used to specify the position of a pattern within the text. The most common ones are:
* `^`: Will be the beginning of the regex line.
* `$`: Will be the ending of the regex line. 

In this example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` you can clearly see the beginning and ending
of the line. 

### Quantifiers

Quantifiers specify how many times a character of group of characters should appear in the input.
* The `+` in this example is used to allow one of more occurences of specific character classes, which in turn enables the local part and domain name to be varying lengths.

### Grouping Constructs
Grouping is used to treat multiple characters as a single unit, created using `()`. These can create groups for the local parts, domain name, and TLD so that specific parts of the email address can be extracted if needed.

### Bracket Expressions
The bracket expresssions matches a set of individual characters that are enclosed in `[]`. For this expression, these are all expressions that can match at specific positions:
* `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`

### Character Classes
AKA bracket expressions. Allows you to define a set of characters that match. Examples:
* `[abc]`: This will match any single character 'a', 'b', or 'c'.
* `[a-z]`: Will match any lowercase from 'a' to 'z'.
* `[0-9]`: This will match any digit from 0-9.

### The OR Operator
The OR Operator `|` allows you to specify the alternatives. It will match either a pattern on the left or the pattern on the right.

### Flags
Flags are optional parameters that modifies how a regular expression is interpreted. There are some common flags that are used:
* `g`: (global) - will match all occurences in the input, just not the first one.
* `i`: (case-insensitive) - will match the characters regardless of their case. 
* `m`: (multiline) - will change the behavior of the beginning `^` and ending `$` anchors.

### Character Escapes
Certain characters have special meaning and in order to match these characters as literals, you'll need to escape them using the backslash `\`. Using the `\` before the dot helps escape the dot, making it match a literal dot character.

## Author

My name is Krystal Richardson and I've created a short document that assist with remembering the functions and components of Regex! For any questions or comments, please contact me via GitHub: [github.com/MsKryssy](https://github.com/github.com/MsKryssy).

