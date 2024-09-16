# IDE Style Guide

**__NB:__** Before checking your IDE - Webstorm, VSC, etc. - please, do check the root folder of
the developer's repository of the project you're going to work on for settings and configurations, 
and do not change those unless you know what you are doing.

## _Integrated Development Environment (IDE) guidelines for React-based projects_

This style guide offers recommendations for configuring your IDE to optimize your React-based project development. 

A properly configured editor can significantly improve code readability and decrease the writing process. 
It can even help you catch bugs as you write them.

> The provided rules are general and may vary depending on the IDE you're using (Visual Studio Code, WebStorm, etc.). 
> Refer to the specific guidelines of your chosen IDE for more detailed information.

### 1. Editor Configuration
Ensure that your IDE is configured to follow standard coding conventions, including:
- Use 2 spaces for indentation (please make sure tabs are converted into spaces).
- Nested indentation should be incremental, for instance: a once nested pair of 
curly braces should be indented with 4 spaces, and so on.
- Remove trailing whitespaces automatically.

### 2. JSX and JavaScript Syntax Highlighting
- Enable JSX and JavaScript syntax highlighting in your IDE for better code readability and identification of syntax errors.

### 3. ES6/ES7 Syntax Support
- Ensure that your IDE supports ES6/ES7 syntax features such as arrow functions, destructuring, spread/rest operators, and async/await.

### 4. Linting
- Integrate ESLint or a similar linting tool into your IDE to enforce coding standards, catch errors, and maintain code quality.
- Your current project may already have linting configuration, please use them in your IDE.

### 5. Debugging Support
- Utilize the debugging capabilities of your IDE to set breakpoints and step through code for efficient debugging of React applications.

### 6. React-specific Tools
- Install React-specific extensions or plugins for your IDE to access features like component snippets, JSX/HTML tag autocompletion, and React-specific syntax highlighting.

### 7. IDE specific problems
- Some IDEs may be unaware of things like JSX, regexp and the like - they may not support highlighting of the
corresponding syntax or files with an extension; in such a case, refer to the documentation of the given
IDE or check its community sites for help.

## Links
- [JetBrains WebStorm React Documentation](https://www.jetbrains.com/help/webstorm/react.html)
- [Visual Studio Code React Tutorial](https://code.visualstudio.com/docs/nodejs/reactjs-tutorial)
- [React Official Editor Setup Guide](https://react.dev/learn/editor-setup)