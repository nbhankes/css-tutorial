# Part 1: Intro to CSS

## Introduction

This page will give a high level overview of CSS. This will help bring context to the purpose and potential of CSS in modern web development. By the end of this page, you will understand the concept and basic syntax of CSS.

## Prerequisites

None.

## Defining CSS 

Cascading Style Sheets (CSS) is a language web developers use to describe how HTML and XML elements appear on the screen. Simply put, CSS allows developers to add style (color, form, contrast, shape, movement, responsiveness, etc.) to HTML layouts.
CSS is not a programming language, but rather a style sheet language. Functionally, it works by selecting an HTML element and assigning the selected element CSS properties. 

## Introducing CSS Syntax

CSS syntax follows a simple three-part naming convention. The "selector" selects an html element. The "property" is a pre-defined CSS property. The "property value" is a value assign to the "property."  

```css
selector {
  property: property value;
}
```

The above example is only for teaching purposes so that you can understand the CSS naming conventions. The example below is similar to what you will write in the real world:

```css
div {
 background-color: red;
 width: 50%;
}
```

This code block shows an example of basic CSS syntax where all <div> elements from a linked HTML document are assigned a background color of red and a width equal to 50% of the viewport width.


The selector, in this case "div," is followed by curly braces. The CSS properties (background-color and width) assigned to this selector are placed within the brackets and supplied with CSS properties values (red and 50%). Property and property value pairs are always separated by semi colons.

## Conclusion

You just learned about the definition and purpose of CSS and gained exposure to its most basic syntax.
