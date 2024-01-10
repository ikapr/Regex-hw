# Regex-hw

Regular expression, widely known as regex, is used to find data within a string. This too has a variety of uses such as searching for and replacing certain strings, validating information by making sure the input adheres to any rules you put in place, extracting data, and a lot more. Regex uses different characters and symbols to express the rules.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This is a regex made to ensure that the sequence of string entered follows the format emails are written in.

const emailRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;

function validateEmail(email) {
  return emailRegex.test(email);
}

const emailToValidate = "user@example.com";
if (validateEmail(emailToValidate)) {
  console.log(`${emailToValidate} is a valid email address.`);
} else {
  console.log(`${emailToValidate} is not a valid email address

This is a function that tells users if they put in a valid email by making sure the email follows the parameters in the regex. The function of all the sybmols in this regex will be explained.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes/Bracket Expression](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors are used to signify where the string starts and where it ends; the “^” signifies the start of the string and the “$” the end. Without anchors, regexes wouldn’t know where to where the beginning and ending point of strings should be. Say a regex that was supposed to find the word “can” was created, without the anchors instead of the regex only identifying “can”  the regex will identify any string with can like “cantine” and “cannibal”.

### Quantifiers
Quantifiers are symbols that represent the number of times characters appear.
+ means the previous character must occur at least once.
? means  the previous character's occurrence is optional.
* matches zero or more of the preceding characters.
{n} Matches exactly n occurrences of the preceding character or group.
{n,} matches n or more occurrences of the preceding character.
{n,m} matches between n and m occurrences of the preceding element.

### OR Operator
In regular expressions, the "or" operator is represented by the pipe character |. It allows you to create patterns that match either one expression or another. The "or" operator works by evaluating the expressions on either side of the pipe, and if any of them match, the entire pattern is considered a match.

### Character Classes/Bracket Expressions
In regular expressions, a character class is a way to match one character out of a set of characters. It allows you to define a group of characters and specify that the pattern should match any single character from that group. Character classes are enclosed in square brackets in order to create a set of desired characters. Character classes provide a concise way to express patterns that involve sets of characters. They are versatile and can be used in combination with other regular expression elements like quantifiers (*, +, ?) and anchors (^, $) to create more complex patterns. Some example of character class:
[123456]: Matches any digit from 1 to 6.
[a-z]: Matches any lowercase letter.
[a-zA-Z0-9]: Matches any alphanumeric character.

### Flags
Flags in regular expressions are like settings that you can add at the end of a pattern to change how it behaves. You can combine flags based on what you need. When using regular expressions in a programming language, you add flags when creating the regular expression. They give you more control over how your pattern matches text. Here are some simple explanations:
Case Insensitivity (i): This flag makes the pattern ignore whether letters are uppercase or lowercase. It treats them the same.
Global (g): This flag makes the pattern find all occurrences in a string, not just the first one.
Multiline (m): This flag changes how ^ and $ work. They match the start and end of each line in a multiline string.
Dot All (s): This flag makes the dot (.) match any character, including newline characters.
Unicode (u): This flag allows the pattern to work with Unicode characters and properties.

### Grouping and Capturing
In regular expressions, grouping and capturing are techniques that allow you to treat part of a pattern as a single unit and, in some cases, capture the matched text for later use. These are accomplished using parentheses ().  

### Greedy and Lazy Match
In regular expressions, "greedy" quantifiers, such as * and +, aim to match as much of the input as possible while still allowing the overall pattern to succeed. For example, .* would match the longest sequence of characters between specified elements. On the contrary, "lazy" quantifiers, denoted by adding ? after the quantifier (e.g., *? or +?), match as little as possible while still allowing the pattern to match. This is helpful when you want to capture the shortest possible sequence between occurrences of a pattern, providing more control in specific matching scenarios.

### Boundaries
In regular expressions, boundaries define specific points in a string where a match should occur. The most common boundaries are the caret ^ and the dollar sign $, which respectively represent the start and end of a line or string. The \b (word boundary) asserts that the pattern is at the beginning or end of a word, ensuring it is not part of a larger word. Conversely, \B asserts a non-word boundary, requiring the pattern to be within a word. Boundaries help refine pattern matching by anchoring it to specific positions or word boundaries in the input string, providing precise control over where a match should occur.

### Back-references
In regular expressions, a back-reference is a feature that allows you to refer back to a captured group within the same regular expression. This is particularly useful when you want to match repeated occurrences of the same pattern or ensure consistency within a string. Back-references are typically denoted by \ followed by the group number (e.g., \1, \2) and are used within the same regular expression pattern.

### Look-ahead and Look-behind
In regular expressions, lookbehind and lookahead assertions are advanced features that allow you to check for the presence or absence of certain patterns before or after the current position in the string, without including them in the match. Lookbehind, denoted as (?<=...), checks for a pattern that precedes the current position, while lookahead, denoted as (?=...), checks for a pattern that follows the current position. These assertions enable more sophisticated pattern matching by providing context-based conditions. For instance, a lookbehind could ensure that a certain word is preceded by another specific word, and a lookahead could verify that a particular string is followed by a specific pattern without including it in the matched result. These techniques enhance the precision and flexibility of regular expressions in scenarios where the matching criteria depend on the surrounding context.

## Author
I'm new developer trying to discover my place in the coding world. https://github.com/ikapr
