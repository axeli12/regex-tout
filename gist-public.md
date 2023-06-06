# Regex Tutorial: Html Tag 

Regular Expressions are a string of characteres that can be used to create a search pattern. This will help you locate HTML tags in a string.

 ## Summary 

The regex we will be looking at is :
`/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/`

The start of the expression is it will be looking for an opening tag that is `^` and the closing tag `$`. Then followed by any lowercase letter from a-z. This will find any HTML tag such as a p,a,div,script.

As the expression is ending there is a closing tag before the `$` this will look for any closed tags of the HTML tags ex: `</div>`


## Table of Contents

* [Anchors](*anchors)
* [Quantifiers](#quantifiers)
* [OR Operator](#or-operator)
* [Character Classes](#character-classes)
* [Flags](#flags)
* [Grouping and Capturing](#grouping-and-capturing)
* [Bracket Expressions](#bracket-expressions)
* [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Componets
 
 ### Anchors

 The two characters that are anchors are `^` and `$`. These two are to match the beginning and the end of the string.

 `^` This anchor is used to start the string, in our example it is followed by `<` an open string this means it will match only one string.

`$` This is a closing anchor. This anchor matches the end of the string.

 ### Quantifiers

 There are two quantifiers in this regex and they are `+` and `*`

 The `+` quantifier is to match 1 or more of grouping 

 the `*` quantifier is to check the 0 more instances of that capture group

 
 ### OR Operators

 There is one or operator in this regex `|`

 What this operator is doing it will match one or the other one on each side of the operator `?:>(.*)<\/\1>|\s+\/>)$ `, this is represented as having the posibilities of having a closing or self closing tag.


 ### Character Classes

 Character classes are indicated by the `[]` and it tells our expression what letter we want it to match.

 * `[a-z]` This will match any lowercase letter from 'a' all through 'z'
 * `[^<]` This will match any character that is not '<' due to it being used in the beginning with out anchor

 ### Flags

 There are no flags in this expression.

 Some examples of flags are 
 * `g` Makes the expression match all occurrences
 * `i` Makes the expression case sensitive
 * `m` Makes the expression search on multiple lines

 ### Grouping and Capturing

 Groups are formed with the parentheses, what they are used for is to capture parts of a match. 
 The two examples of groupings in this expression are
  * `([a-z]+)` 
  * `([^<]+)*` 


 ### Bracket Expressions

 The bracket expression `[a-z]` will match any lowercase a-z
 and the other expression is `[^<]` this will match any character that is not <

 ### Greedy and Lazy Match

 There is no lazy match in this regex but there is but the quantifiers that were used are greedy by deault so, `+` and `*` meaning that they will match as many characters that they can possibly match. 

### Author

This regex tutorial was made by: https://github.com/axeli12