Regex Tutorial for URL Matching
Regular expressions (regex) are a powerful tool for matching patterns in strings. In this tutorial, we will learn how to use regex to match URLs.

Basic Syntax
The basic syntax for a regex is as follows:

Copy code
/pattern/modifiers
The pattern is the regular expression that you want to match, and the modifiers are optional flags that modify how the pattern is matched.

Matching URLs
A URL typically has the following format:

Copy code
http(s)://www.example.com(/path)?(?querystring)
Here is a basic regex pattern for matching URLs:

Copy code
/(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/
This pattern matches URLs that start with http or https, followed by an optional www. subdomain. Then it matches any combination of letters, numbers, and special characters, followed by a domain extension. It also matches any optional path and querystring.

Using the Regex
You can use the regex pattern in a variety of programming languages and libraries to match URLs in strings. Here is an example of how to use the regex pattern in JavaScript:

Copy code
let pattern = /(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/;
let string = "Visit our website at http://www.example.com for more information.";
let match = pattern.exec(string);
console.log(match[0]); // Outputs "http://www.example.com"
Conclusion
Regular expressions are a powerful tool for matching patterns in strings. In this tutorial, we learned how to use regex to match URLs in a string. This is a basic example and can be extended to match specific URL formats or make the regex more restrictive.
