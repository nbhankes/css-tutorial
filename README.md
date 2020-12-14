# A CSS Tutorial for the #vetswhocode non-profit

### [Part 1: Intro to CSS](#intro-to-css)
### [Part 2: Linking HTML to CSS Stylesheet](#linking-html-to-css-stylesheet)
### [Part 3: CSS Selectors](#css-selectors)
### [Part 4: CSS Properties](#css-properties)
### [Part 5: CSS Box Model](#css-box-model)
### [Part 6: CSS Units](#css-units)


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


# CSS Properties

## Introduction
This tutorial provides the definition of the CSS property and provides various examples and resources to find out more.

## Prerequisites
A basic understanding of HTML

##Understanding CSS Properties
CSS properties define a design or functionality aspect that will apply to the HTML element defined by a CSS selector. Every CSS property has a list of predefined CSS property values that apply to it. In the following CSS syntax, the selector is used to define an HTML element to which the { property: property value } pair, or declaration, applies.  

```css
selector {
  property: property value;
}
```
In the below example, we have placed div in the selector position, meaning the { property: property value } pair, or declaration, that follow applies to all div elements within the linked HTML file. The CSS property here is "background," and its property value of "red" will change the design aspect of background to the color red. 

```css
div {
 background: red
}
```

In the above example, we've assigned a background color of red to all div elements within the linked HTML file. 

## Harnessing the Power of CSS Properties
CSS properties can change almost every design aspect you can imagine. You are only limited by your knowledge of what's possible, so it is important to familiarize yourself with the CSS properties available for your use.

These properties allow to change the HTML design in the following ways:
- Coloration
- Shape and size
- Font manipulation
- Orientation (left, centered, right, custom)
- Movement
- Spacing between HTML elements
- Opacity
- And countless other ways.

## Exploring CSS Properties

The following [link](https://www.w3schools.com/cssref/) leads to a list of CSS properties with brief descriptions. It's important to familiarize yourself with this list so you know what's available to you.



# CSS Box Model

## Introduction
It's often useful to think of individual HTML elements as boxes within your larger page layout, or, in the case of a parent container with nested children, as a box-shaped container holding multiple HTML element boxes. As a designer, you have the power to adjust how these boxes appear and interact with one another.

The box model is a conceptual framework that visualizes the ways in which you can do this.

## Prerequisites
A basic understanding of HTML.

## Understanding the CSS Box Model
In the image below, the white box represents your HTML element. Let's imagine it's an HTML image tag that renders a jpeg file within the browser. 
![Box Model](https://upload.wikimedia.org/wikipedia/commons/7/7a/Boxmodell-detail.png)


This jpeg image is the content of your box model, so the image is represented by the white box above. Padding, border, and margin are the CSS properties that you can now apply to a selector associated with this image. You can adjust these to meet your design needs.You now have three properties that can apply to this image:

```css
img {
    padding: 0px 0px;
    border: none;
    margin: 0px 0px;
    }
```

## Understanding Border
Border is the perimeter around your image, essentially its edge or outline.The CSS border declaration has a specific syntax that allows you to define its style efficiently. It looks like this:
border: width & border-style (required) & color
In practice, it looks like this:
```css
img {
    border: 5px solid black;
}
```
In the above border declaration, we've given the image a solid black border that's 5 pixels wide. For more details on the types of property values associated with the border property, visit MDN CSS: border

## Understanding Padding
Padding is the space between your content and the border. Padding can be adjusted multiple ways
```css
img {
    padding-top: 5px;
    padding-bottom: 10px;
    padding-left: 20px;
    padding-right: 0px;
    }
```
The above padding declarations assign padding widths and heights to their respective sides individually. A shorthand method for this is:

```css
img {
    padding: 5px 10px;
    }
```
In the above code:
5px applies to the top and bottom padding
10px applies to the left and right padding

## Understanding Margin
Margin is the spacing between the your content's border and any adjacent HTML elements. The property declarations are the same as padding. Using auto for the shorthand method will often center a component. The code would look like this:
```css
.my-component {
    width: 400px;
    height: 400px;
    margin: 20px auto;
}
```
The above code should center the component so that the left and right margins are always equal.

## Understanding Height and Width
In many cases, you may need your component to have a specific height or width. So it's important to understand how padding, margin, and border affect the dimensions of your component. Let's look at the following example:
```css
.my-content {
    width: 400px;
    height: 200px;
    padding: 10px 10px;
    margin: 20px 5px;
    border: 5px solid red;
}
```
In the above example, you might think that your component width would equal 400px. But this is not the case. Padding, margin, and border are added to the width and height. So, remembering that when using shorthand the first value applies to the top and bottom, our height is equal to 200px + 10px + 10px + 20px + 20px + 5px + 5px, or 270px. We add the size of the padding, margin, and border twice because they all apply to the top and bottom. 

There is a CSS property that changes this behavior. The box-sizing property used with the border-box property value includes padding and border in the element's total width and height. See the example below: 
```css
.my-content {
    box-sizing: border-box;
    width: 400px;
    height: 200px;
    padding: 10px 10px;
    margin: 20px 5px;
    border: 5px solid red;
}
```
In the above example, the padding and border are added inside of the declared width and height, meaning the calculated height would amount to 200px + 20px + 20px, or 240px.


# CSS Units

## Introduction
CSS offers many different units for use when declaring property value heights, widths, and sizing, and these units are calculated in various ways. By understanding the various options, you'll be able to achieve the desired look and page layout.


## Prerequisites
A basic understanding of HTML.

## Understanding the Difference Between Absolute and Relative
Absolute length units are units that are not relative to anything, meaning they are generally considered to remain the same size in all situations. Examples include:

- cm (centimeters)
- mm (millimeters)
- Q (Quarter-millimeters)
- in (inches)
- pc (Picas)
- pt (Points)
- px (Pixels)
<br/>
Relative length units are relative to something else. For example, perhaps the font-size is relative to the width of a parent container. Relative sizing allows browsers to render the HTML and CSS differently based on dynamic variables like screen width. Examples include:

- em (Relative to font size or width of a parent container) 
- ex (x-height of the element's font)
- ch (Relative to the width of the symbol "0" of a given element's font)
- rem (Relative to the font size of the root font) 
- lh (Relative to the line height of the element)
- vw (Relative to screen size; 1% of the viewport's width)
- vh (Relative to screen size; 1% of the viewport's height)
- vmin (Relative to screen size; 1% of the viewport's smaller dimension)
- vmax (Relative to screen size; 1% of the viewport's larger dimension)

## Using CSS Length Units on the Web
Relative length units are generally favored in responsive web design. Some of the most popular length units in the industry (as of 2020) are em, rem, vw, and vh units, so this tutorial will go into more depth with these units:

### rem
The rem unit is relative to the root font size. Browser's generally set the root font size at 16 pixels. But as a developer, you can explicitly declare a root font size in one of two ways:
```css
html {
font-size: 12px;
}
* {
font-size: 12px;
}
```

Both of these approaches set the default font size as 12 pixels. So a length unit of 1rem is equal to 12 pixels. A length unit of 1.5rem is equal to 18 pixels. This is calculated as 1.5 times the value of 12. 

You guessed it, a length of 2rem is then equal to 24 pixels, or twice the value of 12 pixels.
em
The em unit is equal to the computed value of the ‘font-size’ property of the element on which it is used. The example below shows how this works:
```css
.my-class-selector {
   font-size: 20px;
   border-radius: 0.5em;
}
```
In the above example, the border-radius is equivalent to 10px, or (20 * 0.5).

If the font-size is not defined, but em is used, the sizing will be based on the parent container's font-size value. The example below shows how this works:
```css
.my-parent-container {
    font-size: 20px;
}

.my-child-element {
    font-size: 1.5em;
}
```

In the above example, the font size of the .my-child-element class is 30px, or (20 * 1.5).

### vw
1vw is equal to 1% of the viewport width. 50vw is equal to 50% of the viewport width. Because you never know what screen size will access your code, this unit allows you to set exactly how much of the screen will be occupied by a given element. 

### vh
1vh is equal to 1% of the viewport height. 50vh is equal to 50% of the viewport height. Because you never know what screen size will access your code, this unit allows you to set exactly how much of the screen will be occupied by a given element.



