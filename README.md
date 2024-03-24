# Brock's Regex Tutorial

Searching for specific text patterns in a large document can be a daunting task. It can work, but it is not efficient. Using Regular Expressions (RegEX) can help you search for specific text patterns, and variations of those patterns, in a more efficient manner. RegEX uses a sequence of characters to assist in pattern matching. This tutorial will help you understand the basics of RegEX and how to use it to search for specific text patterns.

## Summary

In this example, we will be using the following RegEx to search for a text pattern that matches a specific email address (example@acme.com):
```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

## Table of Contents

- [Brock's Regex Tutorial](#brocks-regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors (```^``` and ```$```)](#anchors--and-)
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
  - [Author](#author)

## Regex Components

### Anchors (```^``` and ```$```)
An anchor component is used to match a position in the text. The \^ and \$ characters are both anchor components. The \^ character is used to match the beginning of the text, and the \$ character is used to match the end of the text. In the example RegEx, the \^ character is used to match the beginning of the email address, and the \$ character is used to match the end of the email address.

In our example RegEx, we have defined that the beginning of the email address should start with a sequence of characters that include lowercase letters, numbers, underscores, periods, and hyphens ```/^([a-z0-9_\.-]+)```. The email address should also include the @ symbol, followed by a sequence of characters that include numbers, lowercase letters, periods, and hyphens ```@([\da-z\.-]+)```. The email address should end with a period, followed by a sequence of characters that include lowercase letters and periods ```\.([a-z\.]{2,6})$/```.

### Quantifiers
Quantifiers can be represented by a single character or a range of characters. The most common quantifier is the asterisk (*) character, which is used to match zero or more occurrences of a character. Other quantifiers include the plus (+) character, which is used to match one or more occurrences of a character, and the question mark (?) character, which is used to match zero or one occurrence of a character.

In our example RegEx, we have used the plus (+) character to match one or more occurrences of the sequence of characters that include lowercase letters, numbers, underscores, periods, and hyphens ```([a-z0-9_\.-]+)```, and the sequence of characters that include numbers, lowercase letters, periods, and hyphens ```([\da-z\.-]+)```. If you did not have the plus (+) character, the RegEx would only match one occurrence of the sequence of characters in the email address meaning it would only return the first character in the email address.

### OR Operator
The OR operator is represented by the pipe (|) character and is used to match one of two or more patterns. In our example RegEx, we have not used the OR operator.

In other examples, the OR operator can be used to match different variations of a pattern. For example, the RegEx ```/cat|dog/``` will match either the word "cat" or the word "dog".

### Character Classes
A character class defines a set of characters that can be matched in a text. In our example RegEx, we have used the character classes [a-z], [0-9], [_.], [\d], and [a-z\.]. The [a-z] character class is used to match any lowercase letter, the [0-9] character class is used to match any number, the [_.] character class is used to match an underscore or a period, the [\d] character class is used to match any digit, and the [a-z\.] character class is used to match any lowercase letter or period. The [\w] character class is used to match any word character, which includes lowercase letters, uppercase letters, numbers, and underscores.

### Flags
Flags are used to modify the behavior of a RegEx pattern. In our example RegEx, we have not used any flags.

In other examples, flags can be used to make a RegEx pattern case-insensitive, global, or multiline. For example, the RegEx ```/cat/i``` will match the word "cat" in a case-insensitive manner.

An example of a global flag is the RegEx ```/cat/g```, which will match all occurrences of the word "cat" in a text.

Finally, an example of a multiline flag is the RegEx ```/cat/m```, which will match the word "cat" across multiple lines in a text. What makes a multiline flag different from a global flag is that it will match the word "cat" at the beginning of each line in a text.

### Grouping and Capturing
Grouping and capturing are used to group multiple characters together and capture the matched text. Grouping is defined with rounded brackets (()), and capturing is defined with backslashes (\). In our example RegEx, we have used grouping and capturing to match the sequence of characters that include lowercase letters, numbers, underscores, periods, and hyphens ```([a-z0-9_\.-]+)```, the sequence of characters that include numbers, lowercase letters, periods, and hyphens ```([\da-z\.-]+)```, and the sequence of characters that include lowercase letters and periods ```([a-z\.]{2,6})```.

### Bracket Expressions
In bracket expressions, you can define a set of characters that can be matched in a text. In our example RegEx, we have used bracket expressions to match the sequence of characters that include lowercase letters, numbers, underscores, periods, and hyphens ```[a-z0-9_\.-]```, the sequence of characters that include numbers, lowercase letters, periods, and hyphens ```[\da-z\.-]```, and the sequence of characters that include lowercase letters and periods ```[a-z\.]```.

When you use a hyphen in a bracket expression, it is used to define a range of characters. For example, the bracket expression [a-z] will match any lowercase letter from a to z. Likewise with defining a range of numbers, the bracket expression [0-9] will match any number from 0 to 9.

### Greedy and Lazy Match
A greedy match will match as many characters as possible in a text, while a lazy match will match as few characters as possible. In our example RegEx, we have not used a greedy or lazy match.

In other examples, a greedy match can be defined with the asterisk (\*) character, and a lazy match can be defined with the asterisk followed by a question mark (*?) meaning it will match as few characters as possible.

Curly brackets can also add extra functionality to a greedy or lazy match. For example, the RegEx ```/a{2,4}/``` will match the letter "a" two to four times in a text.

### Boundaries
Boundaries are used to match a position in a text. In our example RegEx, we have not used boundaries.

A boundary is a special character that is used to match a position in a text. For example, the \b boundary is used to match a word boundary, the \B boundary is used to match a non-word boundary, the ^ boundary is used to match the beginning of a text, and the $ boundary is used to match the end of a text.

In other examples, the \b boundary is used to match a word boundary, the \B boundary is used to match a non-word boundary, the ^ boundary is used to match the beginning of a text, and the $ boundary is used to match the end of a text.

### Back-references
Back-references are used to match a previously captured group in a text. In our example RegEx, we have not used back-references.

In other examples, back-references can be used to match a previously captured group in a text. For example, the RegEx ```/(\d)\1/``` will match any digit that is repeated in a text.

### Look-ahead and Look-behind
Look-ahead and look-behind are used to match a position in a text without including the matched text in the result. In our example RegEx, we have not used look-ahead or look-behind.

In other examples, look-ahead and look-behind can be used to match a position in a text without including the matched text in the result. For example, the RegEx ```/cat(?=dog)/``` will match the word "cat" only if it is followed by the word "dog".

## Author

My name is Brock Lockhart-Doyle. I am a Junior Full-Stack Developer with a passion for learning new technologies and programming languages. I am currently enrolled in the University of Toronto's Full-Stack Web Development Bootcamp. I am excited to continue learning and growing as a developer. You can find me on [GitHub](https://github.com/blockdoyle) and on [LinkedIn](https://linkedin.com/in/blockdoyle).
