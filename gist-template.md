# Regex Tutorial

This is a simple tutorial of what Regex is and how it can be used as a tool for developers.

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
  - [Regex Components](#regex-components)
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
  - [Author](#author)

## Summary  
This is a tutorial that explains how a specific regular expression, or Regex, functions by breaking down each part of the expression and describing what it does. Because an email is a string, you can use Regex to validate email. The Regex function that will be broke down is:   
 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
 This function or pattern is common in web development. It ensures that a user input conforms to the structure of a valid email address. 

## Regex Components
- The 4 key parts of an email address that need to be considered when we validate an email adress:  
  1. Username  
  2. @ symbol  
  3. Domain name (the '.com' aspect)  
  4. Service provider (gmail, yahoo)  
### Anchors  
|  | Braking it down|
|---|--------------------------------|
| ^ | Asserts the beginning of a line|
| [] | Match any one of the characters inside the brackets|
| A-Za-z | Match any uppercase and lowercase letters|  
| 0-9 | Match any digits 0-9|  
| _!#$%&'*+ | Match any one of the literal characters in the list|  
| \/ | Match the / character|  
| =?`{\|}~^.-  | Many any one of the literal characters in the list|  
| + | Matches the previous token (in this case the group between the brackets) between one and unlimited times|  
| @ | Matches the "@" character|   
| [A-Za-z0-9.-]+ | Matches any uppercase or lowercase letters, any digits 0 9, the literal characters . and - (and matches that grouping as many times as necessary|  
| $ | Asserts the end of a line|  
| / | Indicates that the Regex is ending|   
|gm | Modifiers that indicate that the search should be performed "globally" (meaning don't return after you find the first match), and "multi-line" (meaning, search multiple lines.)|

### Quantifiers  
Quantifiers in this Regex includes the + operator, which will connect the users email name + email service + .com. Another quantifier for this Regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.]

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

As an energetic and results-driven full-stack web developer, I hold a Web Development Certificate from The University of Minnesota. With my skills, I am able to build and maintain websites from conception to production. I am also capable of working effectively in a diverse team environment and developing solutions that exceed expectations.

My work experience includes 15 years in retail, 4 years in manufacturing, and 4 years with a small website development company.   
([Sheila's GitHub](https://github.com/Sheila-Ha))
