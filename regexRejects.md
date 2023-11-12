# regexRejects: a Regular Expression Tutorial

This tutorial will breakdown and describe, in detail, each componenent of a Regular Expression.<br>
A Regular Expression (`regex`) is a sequence of characters that defines a specific search pattern. When coded or utilized within a specific algorithm-search, `regex` may hyper-focus on certain patterns of characters within a string, or locate & replace a character or sequence-of-characters within a string. As well as validation of certain or specific input. 

## Summary
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This assignment tasks us with dissecting and describing the `regex` components, of the above expression.

The specific regex code that I've chosen to breakdown for this assignment, is used in the validation of hexadecimal-color-codes formatted: #xxx or #xxxxxx. Enabling developers to utlize 3 & 6 digit color codes, which may or may NOT contain the prefix `#`.

`^` - This symbol denotes the beginning of a line. Indicating that the matching, should start from the beginning of the string.

`#?` - The question mark `?`, placed right after the `#` symbol, represents it being optional. Meaning the `#` character can appear zero or one time in the string.

`([a-f0-9]{6}|[a-f0-9]{3})` - This is a group, denoted by the parentheses `()`. Which captures either a group of six hexadecimal characters, or a group of three hexadecimal characters.

`[a-f0-9]{6}` - This character class `[a-f0-9]` matches any lowercase letter from `a` to `f`, or any digit from `0` to `9`.<br> The `{6}` specifies that there should be exactly six consecutive characters that match this.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors
There are two anchors being used in this regular expression the `^` and `$`.<br> The `^` anchor tells us that the pattern should match at the beginning of the input string.<br> The `$` anchor lets us know that the pattern should match at the end of the input string.  When they are used together `^` & `$` ensure that entire input string matches the pattern defined within our expression.<br>
`^` - Matches the start of a line.<br>
`$` - Matches the end of a line.

### Quantifiers
Quantifiers allow us to set limits of the string, that our regular expression matches.<br> Here we have three quantifiers in our expression `?`, `{6}` & `{3}`.<br> The `?` is the quantifier which follows the `#`.<br> This decribes that the string, can contain `0` to `1` occurrence of the `#` character.<br> Next is the `{}` quantifier, which tells us that we are looking for an exact number or occurrences in the input string.<br> `{6}` is displayed, looking for exactly six occurrences of a valid hexadecimal code, while the `{3}` is looking for exactly three occurrences.<br>
`?` - Matches the preceding character or group zero or one time.<br>
`{6}` - Matches the preceding character or group exactly six times.<br>
`{3}` - Matches the preceding character or group exactly three times.

### Grouping Constructs
Grouping constructs `()` are used to delineate the subexpressions of a regular expression, and capture the substrings of an input string.<br> 
The `(` and `)` in our expression, is a grouping construct or sub-expression.<br> 
In our regular expression they group two hexadecimal strings that are valid color codes. Either 3 or 6 digits codes.<br>
`()` - Defines a group. Allows capturing and grouping parts of the expression together.

### Bracket Expressions
`[]` - Defines a character class or a bracket expression. Matches any character inside the brackets.<br>
`[a-f0-9]` - This bracket expression defines a character class that matches any lowercase letter from `a` to `f`, or any digit from `0` to `9`. It represents the valid characters for the hexadecimal color codes.<br>
`[a-f0-9]{6}` - This bracket expression is followed by the quantifier `{6}`, which specifies that the preceding character class should be repeated exactly six times. It matches a group of six hexadecimal characters representing the full color code.<br>
`[a-f0-9]{3}` - Similarly, this bracket expression followed by the quantifier `{3}`, matches a group of three hexadecimal characters that represent a shortened version of the color code.


### Character Classes
Character classes are represented by `[]`, and specify a set of characters that my be matched at a particular position in the input string.<br>
The `[a-f0-9]` characer class tells us that the input string can include any lowercase letters from `a` to `f`, and any digit `0`-`9`.<br>
`[a-f]` - Matches any lowercase letter from `a` to `f`.<br>
`[0-9]` - Matches any digit from `0` to `9`.

### The OR Operator
`|` - Acts as the OR operator. Matches the expression before or after it.<br> In regular expressions the `|` serves as an OR operator. This allows the patterns, on either side of it, to be matched.<br> Which means a valid match can occur, if either of the patterns is found.<br> In our expression valid matches can be either 6 characters, OR 3 characters. The OR operator provides flexibility in pattern matching, allowing you to define more comprehensive validation rules for your data.

## Author
## Author
A link to my Github Profile: [BrianJohnMaher](https://github.com/BrianJohnMaher)<br>
A link to the Repository: [[regexRejects](https://brianjohnmaher.github.io/regexRejects/)]<br>
A link to the Github Gist: [[regexRejectsGist](https://gist.github.com/BrianJohnMaher/97057d22b747818601abcb921f3f54bf)]
