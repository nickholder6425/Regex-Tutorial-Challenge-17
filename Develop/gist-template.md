# Computer Science for JavaScript Challenge: Regex Tutorial

## Summary

Regular expressions, commonly known as regex, serve as powerful tools for pattern matching and text search operations. This tutorial will delve into the process of utilizing regex to match email addresses. Each element of the expression will be dissected and elucidated, providing insights into the workings of a standard email regex pattern.

The featured regex pattern is meticulously crafted to identify valid email addresses. The following code snippet showcases the regex in action:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

This regex expression proves invaluable for validating email addresses, ensuring they adhere to a predefined format. Throughout the tutorial, we will elucidate the distinct components of this regex and elucidate their respective functionalities.

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
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to specify the position of the match within the text. In the email regex pattern, we use the ^ and $ anchors:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{2,}$/;

-The ^ anchor matches the start of a line. -The $ anchor matches the end of a line.
By using these anchors, we ensure that the entire email address matches the pattern from start to end.

### Quantifiers

Quantifiers define the number of occurrences of a specific element in the regex pattern. In the email regex pattern, we use the + and {2,} quantifiers:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{2,}$/;

The + quantifier matches one or more occurrences of the preceding element.
The {2,} quantifier matches two or more occurrences of the preceding element.
In this case, we use the + quantifier to match one or more characters in the username part of the email address. The {2,} quantifier is used to ensure that the top-level domain (TLD) has at least two characters.

### OR Operator

The OR operator allows us to match either one pattern or another. In the email regex pattern, we use the | operator:

const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{2,}$/;

In this regex pattern, we use the | operator to match either a dot (.) or a hyphen (-) in the domain part of the email address.

### Character Classes

Character classes are used to specify a set of characters that can match at a specific position. In the email regex pattern, we use character classes like [a-zA-Z0-9._%+-] and [a-zA-Z]:

const emailRegex = /^[a

### Flags

Flags in regular expressions are additional parameters that modify the behavior of the regex. Common flags include i for case-insensitive matching, g for global matching (find all matches, not just the first one), and m for multiline matching.

### Grouping and Capturing

Grouping in regular expressions allows you to treat multiple characters as a single unit. It enables you to apply quantifiers, capture specific parts of the pattern, or create logical sections within the regex.

In the context of matching an email address, grouping can be utilized to isolate the username, domain, and top-level domain (TLD) sections for further analysis or validation.

Let's consider the following regex pattern for email matching:

const emailRegex = /^([a-zA-Z0-9._%+-]+)@([a-zA-Z0-9.-]+).([a-zA-Z]{2,})$/;

In this pattern, we have three groups defined by parentheses ( ):

The first group ([a-zA-Z0-9._%+-]+) represents the username part of the email address. It allows alphanumeric characters, dots, underscores, percent signs, plus signs, and hyphens.
The second group ([a-zA-Z0-9.-]+) represents the domain part of the email address. It allows alphanumeric characters, dots, and hyphens.
The third group ([a-zA-Z]{2,}) represents the TLD part of the email address. It allows alphabetical characters with a minimum length of 2. By grouping these sections, we can access and extract them individually for further processing.

### Bracket Expressions

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
Matches any character in the square brackets. For example [nN] [oO] matches no, nO, No, and NO. gr[ae]y matches both spellings of the word 'grey'; that is, gray and grey.

### Greedy and Lazy Match

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
A greedy match tries to match an element as many times as possible. Whereas, a lazy match tries to match an element as few times as possible. In our example we have ? which signifies lazy quantifier. This is referred to a lazy quantifier because it causes the regular expression engine to match as few occurances as possible. We can simply turn this lazy match into a greedy one by adding a ?.

### Boundaries

Boundaries are positions between characters where assertions such as the start of a line (^) and the end of a line ($) can be applied. In the given regex, ^ asserts the start of the line, and $ asserts the end of the line. Together, they ensure that the entire string adheres to the specified pattern.

### Back-references

Back-references allow referencing previously matched groups within the regex. For example, if you capture a group with parentheses, you can reference it later in the regex. The provided regex doesn't include explicit back-references.

### Look-ahead and Look-behind

Look-ahead ((?=...)) and look-behind ((?<=...)) are assertions that check for patterns ahead or behind the current position in the string without including them in the match. They are used for creating more complex conditions without consuming characters in the process. The provided regex doesn't employ look-ahead or look-behind assertions.

## Author

This tutorial was created by [Nicholas Holder](ngholder@hotmail.com).

[GitHub](https://github.com/nickholder6425/Regex-Tutorial-Challenge-17)