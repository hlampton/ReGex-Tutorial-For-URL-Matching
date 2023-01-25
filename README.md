# Regex Tutorial for URL Matching
Regular expressions (regex) are a powerful tool for matching patterns in strings. In this tutorial, we will learn how to use regex to match URLs.

## Table of Contents:

- [Basic Syntax](#Basic Syntax)
- [Matching URLs](#Matching URLs)
- [Here is a basic regex pattern for matching URLs](#Here is a basic regex pattern for matching URLs)
- [Using the Regex](#Using the Regex)
- [Conclusion](#Conclusion)
- [Author](#Author)
- [User Story](#User-Story)
- [Acceptance Criteria](#Acceptance-Criteria)

## Basic Syntax
The basic syntax for a regex is as follows:

```regexp
/pattern/modifiers
```
The pattern is the regular expression that you want to match, and the modifiers are optional flags that modify how the pattern is matched.

## Matching URLs
A URL typically has the following format:

```regexp
http(s)://www.example.com(/path)?(?querystring)
```

## Here is a basic regex pattern for matching URLs:

```regexp
/(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/
```

**This pattern matches URLs that start with 'http' or 'https', followed by an optional 'www.' subdomain. Then it matches any combination of letters, numbers, and special characters, followed by a domain extension. It also matches any optional path and querystring.**

## Using the Regex

You can use the regex pattern in a variety of programming languages and libraries to match URLs in strings. Here is an example of how to use the regex pattern in JavaScript:

```regexp
let pattern = /(https?:\/\/)?(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/;
let string = "Visit our website at http://www.example.com for more information.";
let match = pattern.exec(string);
console.log(match[0]); // Outputs "http://www.example.com"
```

## Conclusion
Regular expressions are a powerful tool for matching patterns in strings. In this tutorial, we learned how to use regex to match URLs in a string. This is a basic example and can be extended to match specific URL formats or make the regex more restrictive.

Please note that this is a basic regex pattern and might not match all the possible URL formats, you can use various regex testers such as Regex101 to test your regex before using it in your code.

## Author

Hunter Lampton is currently a Student of KU's Coding BootCamp.

## User Story

```text
AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines
```
## Acceptance Criteria

```text
GIVEN a regex tutorial

WHEN I open the tutorial.
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, 
a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile.

WHEN I click on the links in the table of contents.
THEN I am taken to the corresponding sections of the tutorial.

WHEN I read through each section of the tutorial.
THEN I find a detailed explanation of what a specific component of the regex does.

WHEN I reach the end of the tutorial.
THEN I find a section about the author and a link to the author’s GitHub profile.
```
