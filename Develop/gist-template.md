# Learning About Code

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines

## Summary

    Some examples can be explained by the following regex but this doesn't contain all examples. The parenthesis are capturing groups that match in that group. Between the capturing groups they seek to match the @ sign and a period. The first capture group can match any character a-z any number range 0-9, "_", "-" or ".". The first capture group has it's items to be matched in a character set that has a quantifier instructing to match one or more of the tokens in that group. The second capture group uses \d to match any digit character any letter a "." or "-" and also includes a character set that has a quantifier instructing to match one or more of the tokens in that group. The third capturing group includes a character set in the brackets which is a-z and a "." and outside of the character set there is a quantifier that indicates that between 2 and 6 of the tokens in that character set should be matched. 

    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
-Matching Fixed Strings

-Matching Special Characters

-Matching Character Sets - a character set would be the letters or numbers inside the brackets can also include a range of characters

-Specifying Groups and Fields -

-Evaluating Occurrences

-Specifying Location

-Specifying Alternatives

-Matching Information from a Table

-Capturing Multiple Lines

-Managing the Scope of Analysis
### Anchors
^ - start
$ -end 
^\d+$ digits
\s+$ white space 
^abc$	start / end of the string - carrot is the beginning while dollar sign is the end. 
    - for example "/^J/" would find something that STARTS with J.
\b\B - word, not-word boundary
### Quantifiers
{x , y}- curly brackets offer a range of number of items to get {2,3} is wanting to match between 2 and three items in the set
{ x} - curly bracket with just one value in it indicates the number of characters you are trying to match
{y,} - match at least the number of y times 
* - match zero or more - greedy matching
+ - match one or more times - greedy matching
? - match zero or one time - lazy matching

### OR Operator
(a|b|c):(x|y|z) - | is the or operator, selects which token to match, matches for example the character (a) (b) or (c) OR then going to the other parenthesis x y or z.
### Character Classes
d/ - matches to one character that character is a digit
w/ - matches 
s/ - selects for whitespace 
/W/D/S - opposite, not word digit whitespace
[a-p] - range of characters a thru p for example
[abc] - lets u take any of this a b OR c
[^abc] - NOT a b or c

### Flags
i - case-insensitive search 
g - returns all matches the default without this flag is to return the first one
m - multiline mode of anchors eg. ^$m - enable m affects ^ and $ so that you can pick out items from different places on the line instead of just the beginning of the line
s - dot-all mode - . now matches to new line character 
u - unicode support enabler. processes surrogate pairs - sometimes a character is 4 bytes and the length of that string is marked incorrectly because the 4 byte character is counted as two separate characters
y - sticky flag - finds the character at the exact position in the text.

### Grouping and Capturing
- (abc) "()"- capture group. Groups multiple tokens so that the group can later be used as    back-reference or can have a substring extracted from it;

- \1 - back-reference group 1 for example - this is useful so you don't have to repeat the character sequence you want to include. (remember DRY);

- (?:abc) "(?:)" - non capturing group - you want to use parenthesis in your expression but you don't want to capture the group;

- (?=abc) "(?=)"- positive lookahead - returns the instances that do include the elements. It will look out for abc for example but also abcd abdc but not zabc

-a(?!b) "(?!)" - negative lookahead -you want to select all of something that does not include the element. It would return the instances that don't have b in them. will match to all not followed by b.
### Bracket Expressions
[a-z\.] - character set that can contain matches, other elements can be added like "i" that would make sure an expression like [A-Z] would match a lowercase a whereas the character set normally would not match
{2-6} - this is a quantifier and as shown in the example, could come after a character set and specify that the character set could match between 2 and 6 tokens. the quantifier specifies the number of matches. 
### Greedy and Lazy Match
* + ? {}
? is lazy
{n} - the number of times the "token" has to be matched. Quantifiers are greedy, they match as many as possible 
+ - matches to one or more of the item/token that goes in front of it.
* - matches to zero or more of the previous item/token, greedy 
### Boundaries
\b - word boundary allows you to search whole words 
\w - non word character
### Back-references
- \1 - back-reference group 1 for example - this is useful so you don't have to repeat the character sequence you want to include. (remember DRY);
### Look-ahead and Look-behind
negative lookahead - a(?!b) - first letter (a) should not be followed by the second letter (b) - this regex searches for that situation
positive lookahead -  a(?=b) -first letter (a) should be followed by the second letter (b) - this regex searches for that situation

negative lookbehind - (?<!a)b - we are looking fo a letter (b) that doesn't have the preceding letter (a) in front of it
positive look behind - (?<=a)b - we are looking fo a letter (b) that does have the preceding letter (a) in front of it
## Author

Kaylin Boyle is in a UCB Full Stack Web Development program student who is learning about regex expressions and hopes to one day work as a front end developer. Her github is listed below.

[Github Profile](https://github.com/kaynboyle)
