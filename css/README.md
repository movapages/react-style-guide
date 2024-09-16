# CSS Style Guide

## _Cascading Style Sheets best practices_

This style guide presents best practices for creating CSS code that is clean and easily to maintain.

> Keep in mind that the rules mentioned are fundamental guidelines, and they can be expanded or in some cases overridden by ESLint plugins within specific project needs.

### 1. Organization and usage
- Group related styles together.
- Prefer class selectors over ID selectors and selectors built on top of HTML tags for styling.
- Maintain a consistent order for property declarations (e.g. logical grouping).

### 2. Naming Conventions
- Use meaningful, descriptive names for classes and IDs.
- Use lowercase letters and hyphens to separate words in class names (i.e., `my-class`).
```css
.header-container {
    background-color: #000;
}
```

### 3. Syntax and Formatting
- Each declaration should appear on its own line for improved readability.
- Always end a declaration with a semicolon `;`.
- Use a single space after the colon : in each declaration.
- Include one space before the opening brace of declaration blocks for readability.
- Use lowercase for all selectors, properties, and property values.
- Separate each rule by a blank line for clarity.
- Use 3 character hexadecimal notation where possible.

```css
.header {
  color: #fff;
  background-color: #000;
}

.footer {
    color: #000;
    background-color: #fff;
}
```

- Avoid specifying units for zero values.
- Separate selectors and declarations by new lines.

```css
.footer,
.header {
    background-color: #fff;
    margin: 0;
}
```

### 4. Properties
- Use shorthand properties when possible while ensuring the code remains clear and readable (e.g. `padding`, `margin`).
```css
.header {
    padding: 0 1em 2em;
}
```
- Avoid unnecessary use of `!important` as it can lead to specificity issues and make debugging difficult.
- Do not use unit marks on `0` values, browser engines ignore those.

### 5. Comments
- Strive to write code that is self-explanatory and does not require comments for basic understanding.
- Reserve comments for explaining complex styles or providing additional context where necessary.

### 6. Use of UI CSS Libraries
- Try hard not to override the existing in libraries classes, create additional instead.
- Keep a separate register of your own or added CSS classes for maintainability’s sake.

### 7. Clean & Neat
- Never ever let remnants of your developer's work clutter the CSS targeted for production or for use by other developers.
- Try to make use of your IDE, which may find duplicate code blocks throughout the whole project.

## Links
- [MDN CSS Writing Style Guide](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS)
- [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
- [DEV Style Guide for HTML/CSS](https://dev.to/theaccordance/a-style-guide-for-html-css-4p6e)