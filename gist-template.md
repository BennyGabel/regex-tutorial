# Title
<h1> regex-tutorial </h1>


## Summary
A **regular expression** also known as **regex**, is a string used to define a search pattern which can then be applied to text. 
This code search is used to look for certain patterns in strings, documents, etc; as well as to perform user's-input validation, like the one will be used in this project to validate an email entry

### **FROM README.md.... will not be used**
### ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$              
---
### **<ins>NOTE</ins>: I HAVE INSERTED A-Z in ALL 3 groups - to include upper case**
### ^([a-zA-Z0-9_\.-]+)@([\da-zA-Z\.-]+)\.([a-zA-Z\.]{2,6})$        
---



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#Author)
- [Regex deeper](#regex-deeper)





## Regex Components

### [Anchors]
^ Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. 
$ Matches the end of the string, or the end of a line if the multiline flag (m) is enabled.
This two anchors determine the beginning and ending of the pattern to-be-searched



### [Quantifiers]
Specify the number of length a string must have minimum (also optional) up-to how many characters.
On the current *regex*,  {2,6} indicates, after xxx@xxx.   should contain between 2 and 6 characters



### Character Classes
*Character class* is also called *character set*,

^([a-zA-Z0-9_\.-]+)@([\da-zA-Z\.-]+)\.([a-zA-Z\.]{2,6})$

Each group is surrounded by []
a-z    represent any character between a to z **lower case**
A-Z    represent any character between a to z **upper case**
_      matches **_**
0-9    represent any digits    from    0 to 9

\d     any digit
-      matches **-**
\.     matches the character **.**.  "\" is used as a scape character




### Flags
\.     matches the character ".".  **\** is used as a escape character, since "." has a specific function in regex



### Grouping and Capturing
()
Parenthesis ae used to group parts of expressions together.
For instance, in the current scenarion, we are evaluating the existence of 3 groups; where 
1. After the first group , there is a **@**
2. After the second group, there is a **.**
3. The third group must be 2 to 6 character long



### Bracket Expressions
[] is used to match a specific character in a range. i.e. [a-z] any character between a to z lowercase



### Greedy and Lazy Match
Greedy Match, looks for the appearance in the entire text. For every position in the string. 1. Try to match the pattern at that position.. 2. If there’s no match, go to the next position.
Lazy Match, means, it repeat minimum number of time
The email regex, will use **greedy match**, will try to match as much as possib



## Author
Name: Benny Gabel
Email: bennygabel@gmail.com
Github Repository: https://github.com/BennyGabel/regex-tutorial







## Regex deeper
On a regular expression, we can search for: 
1. Litteral characters: full string; or 
2. Meta characters: a character that doesn't indicate a single literal character, but that indicates some type of more generalized pattern. 
   Examples
   * ?       Any 1 character
   * \d      Any digit 0 to 9
   * \d\d\d  Any 3 consecutive digits   
   * \d{3}   Any 3 consecutive digits
   * e       Will look for a the letter  **e**
   * ea      Will look for a the letters **ea**
   * e?a     Will look for a the letters **e** and possibly (not necessarily) followed by **a**
   * .ea     Any character followed by **ea**
   * \.      Will look for **.**.  Note there is a scape before ., since 
   * \w      Will look for a word
   * \w {4}  Will look for a word with a length of 4 characters
   * \w {4,5}  Will look for a word with a length between 4 to 5 characters
   * [fc]at  Will look for a word that f or c followed\ending by\with **at**

Other Options in Regex

### OR Operator
There is no or Operator for this *regex*

### Boundaries
The \b is an anchor. it matches a string within the word boundaries
On this email-regex, am not using it.

### Lookahead and Lookbehind   
If you want to match something not followed by something else

