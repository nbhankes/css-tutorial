# A CSS Tutorial for the #vetswhocode non-profit

### [Part 1: Intro to CSS](#intro-to-css)
### [Part 2: Linking HTML to CSS Stylesheet](#linking-html-to-css-stylesheet)
### [Part 3: CSS Selectors](#css-selectors)
### [Part 4: CSS Properties](#css-properties)


# Intro to CSS

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



# Linking HTML to CSS Stylesheet

## Introduction
This page will show you how to link a CSS style sheet with an HTML file. By linking these files, the style sheet will be able to access the content within the linked HTML document. This access allows web developers to use CSS selectors to begin altering the ways in which the layout of the linked HTML document renders on the browser.

## Prerequisites
Code editor (VS Code)
A Basic Understanding of HTML

## Setting Up The Project
Create a new project folder on your computer. Name it something like "CSS Practice." Open the empty folder in your code editor and create an index.html file and a stylesheet.css file. Your folder should be arranged like so:
 <br/>
 📂CSS Practice
 <br/>   ┗ 📜index.html
 <br/>   ┗ 📜stylesheet.css
Great. Now insert the following code into the index.html file:

```html

  <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
    </head>
    
    <body>
  
    </body>
  </html>
  ```
  
The above code is a basic beginning skeleton of an HTML project. In order for your index.html file to link to the stylesheet.css file, you must supply a link tag to the HTML head tag. The following link will be inserted between the HTML link tags:
    ```html
    <link rel="stylesheet" href="stylesheet.css" />
    ```
The link tag element establishes the file relationship "rel" as "stylesheet," ensuring the browser knows what the link is for. And the "href" attribute gives the stylesheet.css location in relationship to the index.html document. This tells the browser where to find the style sheet. In this example, the stylesheet.css and index.html files are in the same folder, so only the file name is required.

Your HTML code should now look like this:
```html
  <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <link rel="stylesheet" href="stylesheet.css" />
      <title>Document</title>
    </head>
    
    <body>
  
    </body>
  </html>
  
```
  
  
# CSS Selectors

## Introduction
This tutorial provides a definition of the CSS selector and lists the various ways to select an HTML element from within the CSS style sheet.

## Prerequisites
A basic understanding of HTML

## Understanding CSS Selectors
CSS selectors define the HTML elements to which CSS properties apply.  In the following CSS syntax, the selector is used to define an HTML element to which the { property: property value } pair, or declaration, applies.  
```css
selector {
  property: property value;
}
```
In the below example, we have placed div in the selector position, meaning the { property: property value } pair that follow applies to all div elements within the linked HTML file.
```css
div {
 background: red
}
```
In the above example, we've assigned a background color of red to all div elements within the linked HTML file.

## Selecting HTML Elements
There are multiple ways to select an HTML element from with the style sheet. Each method has it's own unique syntax.

- **Universal Selector**
  - The asterisk (*) selector applies to the entire document
- **Type Selector**
  - The div selector will apply to all <div> tags
- **Class Selector**
  - The .myClassName selector will apply to all HTML elements with an attribute of class="myClassName"
- **ID Selector**
  - The #myIdName selector will apply to all HTML elements with an attribute of id="myIdName"
- **Attribute Selector**
  - The [attribute] selector will apply to all elements with that attribute.

There are ways to select HTML elements more specifically by combining more than one selector. These methods will be covered in the CSS Scope tutorial.

## Understanding Inheritance

HTML elements can inherit CSS { property: property values } pairs, known as declarations, even if they are not specifically selected in the style sheet. For example, if the index.html file had this:
```html
<div>
    <p>Welcome to #Vetswhocode</p>
<div>
```

And the linked stylesheet.css file had the following code:
```css
* {
    font-family: sans-serif;
}

div {
    font-size: 24px;
}
```

Since the * selector applies to the entire document, the { font-family: sans-serif } declaration will apply to the paragraph tag. 
Additionally. since the paragraph tag is nested within the div tag, the  { font-size: 24px }  declaration applies to this paragraph element.



