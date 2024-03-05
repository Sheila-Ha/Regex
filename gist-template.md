# Regex Tutorial

This is a simple tutorial of what Regex is and how it can be used as a tool for developers for Validating Email Addresses.

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
  - [Table of Contents](#table-of-contents)
  - [Summary](#summary)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
    - [Testing](#testing)
  - [Author](#author)

## Summary  
This is a tutorial that explains how a specific regular expression, or Regex, functions by breaking down each part of the expression and describing what it does. Because an email is a string, you can use Regex to validate email. At the heart of this discussion is the following Regex pattern used for email validation.  
` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`  
 This pattern is common and a staple in web development. It ensures that a user input conforms to the structure of a valid email address. By understanding each component, you'll gain the ability to tailor this Regex for different requirements or even craft your own patterns for other validation needs. 

## Regex Components
- The 4 key parts of an email address that need to be considered when we validate an email address:  
  1. Username  
  2. @ symbol  
  3. Domain name (the '.com' aspect)  
  4. Service provider (gmail, yahoo)   
    
|  | Braking it down|  
|---|--------------------------------|
| ` ^ `| Asserts the beginning of a line|
|` [] `| Match any one of the characters inside the brackets|
|` A-Za-z `| Match any uppercase and lowercase letters|  
|` 0-9 `| Match any digits 0-9|  
|` _!#$%&'*+ `| Match any one of the literal characters in the list|  
|` \/ `| Match the / character|  
|``` =?`{\|}~^.- ``` | Many any one of the literal characters in the list|  
|` + `| Matches the previous token (in this case the group between the brackets) between one and unlimited times|  
|` @ `| Matches the "@" character|   
|` [A-Za-z0-9.-]+ `| Matches any uppercase or lowercase letters, any digits 0 9, the literal characters . and - (and matches that grouping as many times as necessary|  
|` $ `| Asserts the end of a line|  
|` / `| Indicates that the Regex is ending|   
|` gm `| Modifiers that indicate that the search should be performed "globally" (meaning don't return after you find the first match), and "multi-line" (meaning, search multiple lines.)|
### Anchors  
The anchors used in this Regex expression for matching an email are `^`, which indicates the beginning of the string and `$` to indicate the ending of the string. `(m)`, or multiline is not enabled, so the Regex and at `$`.

### Quantifiers  
Quantifiers in this Regex includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier for this Regex includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.

### Character Classes  
The character class in this express is `/d`, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "444".

### Flags  
A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

### Grouping and Capturing  
Capturing group first in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. The last capturing group is `([a-z\.]{2,6})` to capture the `.com`.

### Bracket Expressions  
Bracketed expressions for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case sensitive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case sensitive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case sensitive) and the character ".".  
### Greedy and Lazy Match  
This Regex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6}` for the last capture group.  

### Testing  
In this section we will test our Regex pattern against various strings to see if they pass or fail as a valid email address.  

  Passing -  
   1.  'example@email.com' matches because it follows the       
   2.  'username@domain.tld' format with valid characters.   
   3.  'user.name@sub.domain.com' matches, demonstrating that periods and subdomains are allowed.  
   4.  'my-email@domain.co.uk' matches, showing that hyphens and two-part Top Level Domains are acceptable.  
   
The 3 examples above passed because each begins with one or more permitted characters, lowercase letters, numbers, underscores, hyphens, or periods. They contain a single `@` symbol separating the local part from the domain part. The domain part contains permitted characters and at least one period. They conclude with a top-level domain between 2 to 6 letters in length.  

Failing -
  1.  'simpleaddress' does not match because it lacks the @ symbol and domain part.  
  2.  'us@.com' does not match because there is no domain name before the top-level domain.  
  3.  'user@domain.d' does not match because the top-level domain is too short, being only one character.  

The test above fail because they do not conform to the structure defined by the Regex pattern. Essential components such as the `@` symbol, local part, domain, or a valid Top Level Domain are missing or incorrect.

## Author

As an energetic and results-driven full-stack web developer, I am immersing myself in a Full-Stack Web Development Bootcamp from The University of Minnesota. With my skills, I am able to build and maintain websites from conception to production. I am also capable of working effectively in a diverse team environment and developing solutions that exceed expectations.

My work experience includes 15 years in retail, 4 years in manufacturing, and 4 years with a small website development company.   
([Sheila's GitHub](https://github.com/Sheila-Ha))
