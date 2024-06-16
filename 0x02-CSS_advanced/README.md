# CSS Advanced
## some intresting points to note ## 
( since this is CSS, I advise you to open the original md code to read and understand more properly since some of the examples here are overriden by md language ).
- Inline styles take precedence over stylesheets, so a inline style will always prevail over any other.
- **You might be wondering what happens if a browser encounters a CSS selector or declaration it doesn’t recognise?**.

well, If a browser is parsing your rules, and encounters a property or value that it doesn’t understand, it ignores it and moves on to the next declaration. It will do this if you have mistyped/misspelled a property or value, or if the property or value is just too new and the browser doesn’t yet support it. Similarly, if a browser encounters a selector that it doesn’t understand, it will just ignore the whole rule and move on to the next one.
- __what does it mean to validate your CSS?__:

A CSS validator checks your Cascading Style Sheets to make sure that they comply with the CSS standards set by the W3 Consortium. There are a few validators which will also tell you which CSS features are supported by which browsers (since not all browsers are equal in their CSS implementation). You can use the following service for that: [CSS Validator](https://jigsaw.w3.org/css-validator/#validate_by_input).
- A browser’s developer tools can also highlight invalid property names or values, when you see a cross line throughout a property in it, you should know it's cancled.
- Nowadays developers tend to target less IDs in their CSS. The reason behind is that IDs should always be unique on a page. And for a maximum flexibility, the usage of only classes simplify the reusability of parts of the UI.
### Cascading or order ###
1. * { } /* select all elements */
2. section /* select all section tags */
3. .my-class { } /* select all elements with that class */
4. .my-block > .my-title { }
5. .my-block + .my-title { }
6. .my-block ~ .my-title { }
7. #my-div /* select the element with that ID  */
### How to represent colors with examples: ###
1. p { color: red; }
2. p { color: #f00; }
3. p { color: #ff0000; }
4. p { color: rgb(255,0,0); }
5. p { color: rgb(100%, 0%, 0%); }
6. p { color: hsl(0, 100%, 50%); }

### custom properties: ### 
Refer to this to learn more: [custom CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)
Short Code example: ``` :root {
  --main-bg-color: blue;
}
body {
  color: var(--main-bg-color);
} ```

---
### Units and values ###
Multiple CSS units can be used in your CSS. px is the one of the most commonly used, and is also an absolute unit, in contrast with relative length units like rem & Both (absolute and relative) are used in different contexts.
rem: font size, padding, margin em: media queries. Kepp in mind that: REM is relative to the root element: the <html> tag not <body> tag.
- Accessibility tip: Use a minimun of 1.5 for line-height for main paragraph content. It will help people with low vision conditions to easily read your content.
- Positioning in CSS requires to use different CSS properties that allow you to position elements in your HTML webpage.
## Popular CSS property: ##
| Syntax      | Description |
| ----------- | ----------- |
| text-align     | Sets the horizontal alignment of a BLOCK element      |
| text-transform   |  Allow to capitalize a text element.       |
| pseudo-class | keyword you can add to a selector. It specifies a different state of the element. |
| a:visited | when you have already clicked and visited the link |
| a:hover | any link over which the user's pointer is hovering |
| box-sizing: border-box | This is the box-sizing value we usually use to create layouts |
| pseudo-element | a keyword added to a selector that lets you style a specific part of this element. |
| transform CSS properties | allow you to rotate, scale, skew, or translate an element. |
| animation CSS properties |  allow you to animate other property of an element. |

### CSS Reset/Normalize ###
The expression CSS reset came from Eric Meyer who created a reset stylesheet in 2007, to reduce browser inconsistencies. Since then, different solutions came out: Normalize.css, sanitize.css, reboot for Bootstrap… .
### Grid systems ###
Grid systems started to be used to layout books and magazines. They started to be used more recently to also create and define website’s layout. Before flexbox and css grid, grid systems were using floats to organize the content. In addition, Before CSS Grid, developers were already using the word grid to define the responsive grid system used to build websites.

Keep in mind that Animation is a shorthand property. Only animation-duration and animation-name are required, here is an example of its syntax:
```
@keyframes example {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
.box {
  width: 10rem;
  height: 10rem;
  background-color: blue;
  animation-name: example;
  animation-duration: 3s;
}
```
## Refernces: ##
1. [css cheatSheet](https://cssreference.io/)
