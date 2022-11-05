# Regex Tutorial

What is Regex? First of all, "Regex" or "regular expression" is a sequence of characters that defines a unique and specific search matching process in a data string.

## Summary

In this Regex Summary, I will be describing not only the various componets of Regex but also describing how it is used in Hex (Hexadecimal) Values.

What is a Hex Value? 
It's a positional numeral system that uses 16 distinc symbols.
The symbols are "`0`"-"`9`" and "`A`"-"`F`" or "`a`"-"`f`".
The "`0`"-"`9`" symbols represent values 0 to 9.
The "`A`"-"`F`" or "`a`"-"`f`" symbols represent values 10 to 15.

Below is an example of a Hex Value and the value that I will be using going forward:
`(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`



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
In Regex, even though Anchors themselves do not match any current characters in the data string, they state the current position and location of the characters within the given data string.

In the Hex value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, the "`^`" and "`$`" are examples of Anchors.

 

### Quantifiers
Quantifiers are greedy by default, which means that they try to match as many data patterns within the data string as possible. They let Regex know how many characters (character length) need to be matched within the data string. 

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, the "`{6}`", and "`{3}`" are examples of Quantifiers
    -The "`{6}`" indicates that the previous array "`[a-f0-9]`" needs to have 6 characters 
    -The "`{3}`" indicates that the previous array "`[a-f0-9]`" needs to have 3 characters

### OR Operator
OR Operators or "or" can be best described as seperators between groups of data. The seperation allows Regex to not only search for but also match however many groups are present.

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, the "`|`" in between "`(/^#?([a-f0-9]{6}`" and "`[a-f0-9]{3})$/)`" is an example of an OR Operator.

### Character Classes
Character Classes define a set of characters in Regex and are defined as whatever data and information is present in between "`[]`" brackets.

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, "`a-f0-9`" and "`a-f0-9`" are examples of Character classes. 

### Flags
Flags are located at the end of a Regex data and they not only define additional functionality, but also limits for the Regex. They are found after the second slash in the dataset.

There are 6 flags that can be used in Regex `(g, i, m, u, s, y)`
`g - Global`
`i - Ignore Casing`
`m - Multiline`
`u - Unicode`
`s - DotAll`
`y - Sticky `

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, there is no Flag because there is nothing after the second slash in the Regex data.

### Grouping and Capturing
Grouping or Group in Regex is any information found inside the parentheses. Capturing a group in Regex is a way to treat multiple characters as one single unit.

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, everything within the parentheses "`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`" is considered grouped and captured, in this example there is one capture, but it is seperated by an OR Operator "`|`".

### Bracket Expressions
Bracket Expressions can be used to match any character within the square brackets inside the data string "`[]`".

### Greedy and Lazy Match
A Greedy Match or quantifier will consume as much information as possible, trying to match with as many elements within the Regex as possible.

A Lazy Match will do the opposite, it will try to match with an element within the Regex as few times as possible.

Greedy and Lazy matches are common in Regex data strings and often characterized by their location within the data.

A Greedy and Lazy match is similiar but the main difference is the addition of the `?` which simbolizes a lazy match.

In the Hex Value `(/^#?([a-f0-9]{6}|[a-f0-9]{3})$/)`, the `?` is considered a Lazy match.


### Boundaries
`Boundaries`, or "`Boundary Markers`", or "`Word Boundaries`", often characterized by "`\b`" allow the user to anchor the Regex pattern either to the beginning and or to the end of the data string.

There are `THREE` different rules that a Bondary must follow for it to be considered a `Boundary`
1. It's considered a Boundary if it is before the first character in the data string.
2. It's considered a Boundary if it is after the last character in the data string.
3. It's considered a Boundary if it's in between two characters in the data string.

### Back-references
A Back-reference looks for the same text or value again within the Regex data.

### Look-ahead and Look-behind
Both Look-ahead and Look-behind are also known as and called "Lookaround", they both match with characters within the Regex, then then they give up the match, returning the result regardless if one was found.

## Author
Hello! I'm Kevin Korza, a Trilogy Full-Stack Coding Bootcamp student! This was a walkthrough and toutorial of Regex.

Please visit my Github profile for more coding fun!

https://github.com/KevinGKorza
