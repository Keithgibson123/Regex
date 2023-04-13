# Regex Tutorial

A regular expression is a sequence of characters that defines a search pattern. It consists of various components, including:

Literals: These are the characters or strings that you want to match exactly. For example, if you want to match the word "hello" in a string, you can use the literal "hello" in your regular expression.

Metacharacters: These are special characters that have a specific meaning in a regular expression. For example, the dot (.) is a metacharacter that matches any single character, while the asterisk (\*) matches zero or more occurrences of the preceding character.

Character classes: These are sets of characters that you want to match. For example, the character class [aeiou] matches any vowel, while [0-9] matches any digit.

Anchors: These are special characters that match the beginning or end of a string, or the beginning or end of a line within a string. For example, the caret (^) matches the beginning of a string, while the dollar sign ($) matches the end of a string.

Quantifiers: These are symbols that indicate how many times a preceding character or group should be matched. For example, the plus sign (+) matches one or more occurrences of the preceding character, while the question mark (?) matches zero or one occurrence.

Flags: These are optional modifiers that can be used to change the behavior of a regular expression. For example, the global (g) flag searches for all occurrences of a pattern, while the case-insensitive (i) flag ignores case when matching.

By combining these components, you can create complex regular expressions that can match a wide range of patterns.

## Summary

In this tutorial, I am going to explain about Regex or regular expression. Regex are a series of special characters that define a search pattern. by the end of this tutorial you will fully understand how this works!!
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Regex components are building blocks used to create regular expressions. These components include:

Anchors - ^ and $ - which represent the start and end of the string respectively.
Quantifiers - ?, \*, +, {n}, {n,}, and {n,m} - which specify the number of occurrences of the preceding character or group.
Grouping Constructs - ( ) - which group expressions together to be treated as a single pattern.
Bracket Expressions - [ ] - which match a single character that is within the brackets.
Character Classes - \d, \w, \s, and . - which match specific types of characters such as digits, word characters, whitespace characters, and any character except newline, respectively.
OR Operator - | - which matches either the expression before or after the operator.
Flags - i, g, m, s, y, and u - which modify the behavior of the regular expression.
Character Escapes - \ - which is used to escape special characters so that they can be used as literal characters in the regular expression.
By combining these components, developers can create powerful regular expressions that can match complex patterns in text

### Anchors

In regular expressions, anchors are used to specify the position of the pattern match within the string being searched. There are two types of anchors in regex:

^ - caret anchor: Matches the start of the string.
Example: /^hello/ will match "hello" at the start of a string but not if it appears in the middle or at the end.

$ - dollar anchor: Matches the end of the string.
Example: /world$/ will match "world" at the end of a string but not if it appears in the middle or at the start.

Using both anchors (^ and $) together will match the entire string.
Example: /^hello world$/ will match only "hello world" as a whole string.

Anchors can be useful in many scenarios, such as validating user input, extracting specific data from a string, or searching for specific patterns within a string.

### Quantifiers

In regular expressions (regex), quantifiers are used to specify how many times a particular character or group of characters should be matched. Quantifiers are represented by special characters and can be applied to individual characters, character classes, and groups.

Here are some common quantifiers in regex:

(asterisk): Matches the preceding character zero or more times. For example, the regex ca\*t matches "ct", "cat", "caat", "caaat", and so on.
(plus): Matches the preceding character one or more times. For example, the regex ca+t matches "cat", "caat", "caaat", and so on, but not "ct".
? (question mark): Matches the preceding character zero or one time. For example, the regex colou?r matches "color" and "colour".

{n} (curly braces): Matches the preceding character exactly n times. For example, the regex ca{3}t matches "caaat" but not "cat" or "caat".

{n,m} (curly braces with two values): Matches the preceding character at least n times but no more than m times. For example, the regex ca{2,4}t matches "caat", "caaat", and "caaaat", but not "cat" or "caaat".

{n,} (curly braces with one value and a comma): Matches the preceding character at least n times. For example, the regex ca{2,}t matches "caat", "caaat", "caaaat", and so on.

Quantifiers can be very powerful tools for matching patterns in text. However, they can also be dangerous if used incorrectly, as they may result in very broad or very narrow matches. It's important to use quantifiers carefully and test them thoroughly before deploying them in production code.

### Grouping Constructs

Contininuing with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We can talk about grouping and capturing.

([a-z0-9_\.-]+) is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. ([\da-z\.-]+) is the second group that appears in our regex. ([a-z\.]{2,6}) is the third group that appears in our regex.

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group

### Bracket Expressions

Represents a character set via a list of characters enclosed by the square brackets. "[" and "]". It matches the target with any single character from the list. Bracket expressions in thie regex: [a-z0-9_.-] --> matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "\_" , "-" , and "."; [\da-z.-] --> matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z.] --> matches any character a-z(case senstive) and the character "."

### Flags

In regular expressions, flags are used to modify the behavior of the matching process. Here are some common flags:

g: Global matching. By default, regular expressions only match the first occurrence of a pattern. Adding the g flag causes the matching process to continue until the end of the string, finding all matches.

i: Case-insensitive matching. By default, regular expressions are case-sensitive. Adding the i flag causes the matching process to ignore case.

m: Multi-line matching. By default, regular expressions only match the beginning and end of the string. Adding the m flag causes the matching process to consider each line of the string as a separate entity, and match the beginning and end of each line.

### Character Escapes

\w --> word (program identifier) character: [A-Za-z0-9_] \w --> non-word character: [^a-za-z0-9_] \s --> whitespace character: [ \f\n\r\t] \s --> non-whitespace character: [^ \f\n\r\t] \d --> digit character: [0-9] \D --> non-digit character: [^0-9

## Author

the author is me
