<img src="./assests/images/banner.png">

# BC17 - Regex Tutorial: Matching an Email

Welcome! In this tutorial we will go over the validation of Matching an Email: A Regex Tutorial. Let's now begin to dissect from left to right and explore each components to understand its role.

## Summary

A regular expression or Regex. Is a character sequence used to define specific search patterns in code or search algorithms. 
It's used to find and change specific character patterns within a string and is also commonly used for input validation.

For instance. The Regex below validates email addresses:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Each component of this regex ensures that user input represents an email address starting with any number of characters before the @ symbol, followed by a valid domain.



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Conclusion](#conclusion)
- [Author](#author)
- [Credits and Resources](#credits-and-Resources)
- [Questions](#questions)
- [License](#license)

## Regex Components

### Anchors
`^ $` These are called anchors. `^` declares the start of the string and `$` declares the end of the string. Regex pattern must match the entire string and not only just a part of it.

***Regex Code Snippet:***
* `^` (Caret): Anchors the pattern to the start of the string.
* `$` (Dollar Sign): Anchors the pattern to the end of the string.
`^` ensures that the matching starts at the beginning of the string and `$` ensures that the matching ends at the end of the string. Meaning the entire string must match the pattern.

***Example:***
Consider the Regex pattern `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`:
* When applied to the string "janedoe@example.com", the `^` ensures that the matching starts at the beginning of the string, and the `$` ensures that it ends at the end of the string, ensuring the entire string must match the pattern.

### Quantifiers
Quantifiers are used to specify how many times certain parts of the email should appear and specify how many times a character or group should be matched.

***Regex Code Snippet:***
* `+` (Plus Sign): Matches one or more occurrences of the preceding character or group.
In the username part `[a-z0-9_\.-]+`, the `+` quantifier ensures that there must be at least one character in the username.

***Example:***
Consider the username part of the Regex pattern `[a-z0-9_\.-]+`:
* With the input "janedoe456," the `+` quantifier ensures that there must be at least one character in the username, matching "janedoe456."
* Without the `+` quantifier, the pattern `[a-z0-9_\.-]` would only match a single character, such as "j."

### OR Operator
The OR operator, represented by the vertical bar `|`, is used to specify multiple alternative patterns within a Regex pattern.  The OR operator is not directly used in `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` but it is implied in the subpatterns. Let's take a closer look:

The `|` symbol acts as an OR operator in regular expressions.
Explanation: It allows you to define alternative patterns and will match the input string if it matches any of the alternatives.
Example: In a regex like `a|b`, it will match either "a" or "b" in the input string.

In the email Regex, we have examples of implied OR operators:

***Example:***
* In `[a-f0-9]{6}|[a-f0-9]{3}`, it matches either a 6-character hexadecimal value or a 3-character hexadecimal value.
* In `[a-z0-9_\.-]+`, it matches one or more lowercase letters, digits, underscores, hyphens or periods.


### Character Classes
Character classes allow you to specify a set of characters to match. They are enclosed in square brackets `[]` and can include individual characters, ranges of characters or predefined character classes. Character Class is also known as the "dot-separated word character class" because it matches any character that can be used to form a word in a domain name, such as a lowercase letter, digit, underscore or hyphen.

***Regex Code Snippet:***
* `[a-z0-9_\.-]+`: Matches the username part of the email address. Matches any lowercase letter, digit, underscore, hyphen, or period.
* `[a-z0-9_\.-]` is a character class that allows lowercase letters, digits `(0-9)`, underscores `(_)`, periods `(.)` and hyphens `(-)`. Matches any digit, lowercase letter, hyphen, or period.

***Example:***
The character class `[a-z0-9_\.-]+` allows valid characters in the username part of an email address:
* "janedoe456" matches because it contains only lowercase letters, digits and underscores.
* "user.name" matches because it contains lowercase letters and periods.
* "invalid-email" doesn't match because it includes a hyphen which is not allowed in the username part.

### Grouping and Capturing
Parentheses `(...)` are used for grouping and capturing parts of a regex pattern.
Capturing groups are enclosed in parentheses and allow you to extract specific parts of the matched string. Capturing groups are useful for extracting specific parts of the matched string, which can be useful for further processing.

***Regex Code Snippet:***
* `(...)` (Parentheses): Groups and captures portions of the pattern.
* `([a-z0-9_\.-]+)`: Captures the username part.
* `([\da-z\.-]+)`: Captures the domain name part.
* `([a-z\.]{2,6})`: Captures the top-level domain (TLD).

### Bracket Expressions
Bracket expressions allow you to specify character ranges within `[...]` square brackets also known as Character Classes.

***Regex Code Snippet:***
* `[\da-z\.-]`: Matches any digit `\d`, lowercase letter `a-z`, period `.` or hyphen `-` within the domain name part.


## Conclusion
In this Regex Tutorial, we've delved into the intricate world of regular expressions and how they can be used to validate email addresses. We've explored the essential components of a Regex pattern. From anchors that define the start and end of a string to quantifiers that dictate how many times certain elements should appear. We've also seen how character classes and grouping can be harnessed to create powerful patterns.

By dissecting a real-world example of an email validation Regex `(/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/)`. We've gained insight into the practical application of these regex concepts.

Regex can be a powerful tool in your programming arsenal. Not only for email validation but also for a wide range of text-processing tasks. As you continue to explore and practice with regular expressions. You'll find that they can simplify complex text matching challenges and streamline your code.

If you're interested in learning more about Regex. There are many resources available online. I encourage you to continue your studies and to apply regular expressions to your own programming projects.

## Author

* Junel B. -  A UC Berkeley Extension Bootcamp Student.

* [Link to Github Profile](https://github.com/junel-balbin)

## Credits and Resources

* Google search & Youtube videos.
* ChatGpt for troubleshooting.
* Starter code EdX and UCB.

## Questions

* Feel free to contact for more information or questions you may have. Happy Coding!

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)