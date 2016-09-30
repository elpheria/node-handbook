# Code Style Guide

We care about how our code's style is done. Plenty of open and closed-source projects
neglect the fact that they should take care of how their code looks like,
driving away potential contributors and team members from reviewing the code efficiently.

These are some of the things we pay attention to:
* Brace style type
* Indent size
* Quotes
* Semicolons
* Spacings
* Line feeds
* Module import/export
* Naming conventions
* Code linting

## Brace style type

We are using the [Allman Brace Style](https://en.wikipedia.org/wiki/Indent_style#Allman_style)
for all our Node.js projects.  
That way we make sure we write a clear and lucid piece of code. The deviation from the standard Node.js coding style,
which is [K&R](https://en.wikipedia.org/wiki/Indent_style#K.26R_style), was made in order to get a clearer, more structured
code overview, reducing time to get accustomed with the project.

## Indent size

An indent size of 4 whitespaces is used. We avoid using hardtabs, since their behaviour may be unexpected under different environments. An original indent size of 2, a Node.js default, must be avoided, since code clarity decreases. We use async/await nowadays, so there's no real needs for short indentations, since there's not a huge number of indentations. If there is, then your problem might be elsewhere.

## Quotes

We are currently utilizing double-quotes ("foo").

## Semicolons

Semicolons (";") in JavaScript are optional and can be freely omitted. Code without them looks prettier and easier to follow. We use semicolons only where strictly necessary.

## Spacings

Coming soon.

## Line feeds

Never put more than one empty line throughout the entire source code file. It's not pretty, doesn't add up to the structure of code and increases line count for no reason.

## Module import/export

Up to ECMAScript 2015 (ES6) we have used a `require` method. From ECMAScript 2016 (ES7) we have started experimenting with import/export. Please, prefer to use those whenever possible.

## Naming conventions

Function names are named in a camelcase manner. First letter is lowercase, ie. `getAllModules`.  
Class names are also camelcased, but the first letter is uppercase, ie. `AutomobileParts`.  
Variables are snakecased, with all letter in lowercase, ie. `json_message`.

Reason we chose snakecase style for variable naming is purely aesthetics. The code is prettier and much easier to read. It takes you more time to read a camelcased variables. And you have plenty of those, which does not apply to classes and functions.

## Code linting

For code formating we are using `eslint`. Each project has its code automatically beautified once the test, build or install is done.  
You can optionally override our settings using in-line `eslint` comments, but that's not recommended. If there's a change in settings that should be considered, please make a PR.  
You can grab the configuration [here](https://github.com/qaap/dotfiles/blob/master/.eslintrc.json).
