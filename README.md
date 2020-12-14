# A CSS Tutorial for the #vetswhocode non-profit

### [Part 1: Intro to CSS](#intro-to-css)
### [Part 2: Linking HTML to CSS Stylesheet](#linking-html-to-css-stylesheet)
### [Part 3: CSS Selectors](#css-selectors)
### [Part 4: CSS Properties](#css-properties)
### [Part 5: CSS Box Model](#css-box-model)
### [Part 6: CSS Units](#css-units)
### [Part 7: Flexbox](#flexbox)
### [Part 8: CSS Grid](#css-grid)
### [Part 9: CSS Display Property](#css-display-property)


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


# Flexbox

Modern web design can be challenging because your website has to look good on viewports ranging in size from an iPhone to a 27" desktop. The Flexbox system of design is a set of CSS properties that allow you to build responsive design layouts that will shrink and expand, orient elements, and define spacing between components as the viewport width increases and decreases.

This tutorial will show you how to get started with flexbox and teach you about the various flexbox properties and their function.

## Prerequisites

A basic understanding of HTML
A basic understanding of CSS selectors and properties

## Getting Started With Flexbox

Flexbox requires a container, or parent, element. Elements nested inside of that container, often referred to as children or child elements, are then under the influence of that container's flexbox rules. In the example below, you'll see the HTML for how this is often constructed:

my-first-flex-project/index.html
```html
<!DOCTYPE html>
    <html lang="en">
        <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <link rel="stylesheet" href="stylesheet.css" />
          <title>My Flexbox Practice</title>
        </head>
    
        <body>
            <div class="flex-container">
                <div class="flex-item">
                    <h2>Box 1</h2>
                </div>
                <div class="flex-item">
                    <h2>Box 2</h2>
                </div>
                <div class="flex-item">
                    <h2>Box 3</h2>    
                </div>
            </div>
        </body>
    </html>
```

In the above example, we have a parent container with three children nested inside. Each child element has the same class name of flex-item, but they each have a unique name that will render on the browser.

*Hint: Your parent container does not have to be labeled as "flex-container" for flexbox to work. And neither do your child elements have to be named "flex-item." They are simply labeled that way to help you learn.*

In order to get this HTML code to render as a flexbox, you need to reference the flex-container class name in the linked stylesheet.css file using the class selector notation. Change the display to flexbox as shown in the code below:

```css
my-first-flex-project/stylesheet.css
.flex-container {
    display: flex;
}
```

Based on the code above, the flex-container rules now apply to the flex-container and flex-item classes. Remember, that the parent container's rules apply to the child elements. This has important implications for how the child elements render and behave in varying viewport widths.


## Understanding Flexbox Properties

Within the flex-container selector, you can now use a group of properties and property values that only work when the display is set as flex. These properties are listed and described below. The property is followed by each value associated with it, separated by the | symbol. The meaning of each value is then described.

### **flex-direction: row | row-reverse | column | column-reverse**
**row (default)**: flex-items render as a row, Box one start on the left when the writing-direction property is set at the default ltr (left to right)
**row-reverse**: flex-items render as a row, Box 3 is on the left when the writing-direction property is set at the default ltr (left to right)
**column**: flex-items render as a column, Box 1 is at the top
**column-reverse**: flex-items render as a column, Box 3 is at the top

### **flex-wrap: nowrap | wrap | wrap-reverse**
**nowrap (default)**: flex-items will remain on the same line regardless of viewport width
**wrap**: flex-container height will increase and flex-items will wrap, or split, into additional rows as needed. flex-items will be in order from top left to bottom right. The last flex-item is the first to drop down to a new row created beneath the original row.
**wrap-reverse**: flex-container height will increase and flex-items will wrap, or split, into additional rows as needed. flex-items will be in order initially, but as the viewport width decreases, the last items will move to a newly created top row.


### **flex-flow: flex-direction property value and flex-wrap property value**
This is a shorthand notation that allows the input of flex-direction and flex-wrap in a single line.
The default declaration is flex-flow: row nowrap

### **justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right**
**flex-start (default)**: flex-items begin at the start of their given flex-direction
**flex-end**: flex-items are positioned at the end of their given flex-direction
**center**: flex-items are centered
**space-between**: space between items is evenly distributed, excepting for the first and last items which touch the furthest boundaries of the flex-container
**space-around**: all items have an equal space on both sides. The outermost borders of the first and last items will appear half as wide because they only have one allocation of space, whereas there are two allocations of space between two flex-items
**space-evenly**: all items appear equally spaced. This includes the first and last flex-items
**start**: items begin at the start as declared by the writing-direction property 
**end**: items begin at the start as declared by the writing-direction property 
**left**: flex-items begin at the left boundary of the flex-container
**right**: flex-items are positioned at the right boundary of the flex-container

### **align-items: stretch | flex-start | flex-end | center | baseline**
**stretch (default)**: flex-items stretch to fill the flex-container. Width and height minimums and maximums are still respected 
**flex-start**: flex-items are positioned at the top of the flex-container
**flex-end**: flex-items are positioned at the bottom of the flex-container
**center**: flex-items are center vertically along the flex container
**baseline**: text within flex-items are aligned

### **align-content: normal (default) | flex-start | flex-end | center | space-between | space-around | space-evenly | stretch**

*Hint: This property only takes effect when there is more than one row or column of flex-items.*

**normal**: flex-item lines render as they would with now align-content property value
**flex-start**: flex-item lines bunched up toward the upper boundary of flex-container
**flex-end**: flex-items lines bunched up bottom the upper boundary of flex-container
**center**: flex-items lines bunched up in vertical center of flex-container
**space-between**: flex-item lines are equally spaced, with the top line touching upper boundary and lower touching bottom boundary
**space-around**: flex-item lines have equal spacing but have a half-size space on either end
**space-evenly**:  flex-item lines have equal spacing, including the ends
**stretch**: flex-items lines stretch to fill the flex-container space. Width and height minimums and maximums are still respected 


Explore the codepen below to see these different flexbox properties in action:

[Codepen Flexbox Demo](https://codepen.io/vetswhocode/pen/qBaZvJq)

## Flex Properties for flex-items
The above flex properties apply to the flex-container. But there are also flex properties for flex-items. These are described below:

### **order**
The order property allows you to manually assign the order of a flex-item relative to the other flex-items nested in the flex-container

### **flex-shrink**
The flex-shrink property allows you to specify how an individual flex-item will shrink relative to the other flex-items nested in the flex-container

### **flex-grow**
The flex-grow property allows you to specify how an individual flex-item will grow relative to the other flex-items nested in the flex-container

### **flex-basis**
The flex-basis property sets an initial length of a flex-item

### **flex**
The flex property is shorthand property for: flex-grow, flex-shrink, and flex-basis
It sets the flexible length on flex-item

### **align-self: auto (default) | flex-start | flex-end | center | baseline | stretch**
Property value alignments are the same as for the align-items property 
The align-self property allows you to alter the alignment of an individual flex-item
By default, flex-items inherit the align-items declaration from the parent flex-container
Setting an align-self on a flex-items overrides this default behavior


# CSS Grid

## Introduction

CSS grid layout provides developers a set of properties and property values that allow for the design of advanced layout patterns. This tutorial will show you how to get started with grid layout and introduce you to the various grid layout properties and their function.

## Prerequisites

A basic understanding of HTML
A basic understanding of CSS selectors and properties

## Understanding CSS Grid Layout

CSS Grid Layout allows web developers to customize how components arrange on the browser. Take the example layout from the picture below: 

![CSS Grid Example](https://gblobscdn.gitbook.com/assets%2F-MAVvSF3_qSwF8GOq1T4%2F-MK1PxDTR7LwMn_AfW_p%2F-MK1Q0R0_YPfVO0XZekr%2FHeader.png?alt=media&token=1d349d7d-1f72-48fc-9184-dfbaafc094b6)

In the above picture, we have four major design components: Header, Nav, Body, and Footer. We can use CSS grid layout to position our html elements to match this mock up.

You can reference the finished product here:
[Codepen Grid Tutorial Example](https://codepen.io/nbhankes/pen/abZdBPa)

Getting Started With CSS Grid Layout
In a nutshell, we enclose our four major design components in a container with its display property value set to grid. Our container CSS declaration will look like so:

```css
.grid-layout-container {
    display: grid;
}
```

We then assign a grid area name to each of the individual design components. So our style sheet will look something like this:

```css
.header {
    grid-area: header;
}

.nav {
    grid-area: nav;
}

.body {
    grid-area: body;
}

.footer {
    grid-area: footer;
}
```

We have assigned names to our four major design components using the grid-area property. We can now reference and manipulate these grid-areas, by name, inside of the container with the class of "grid-layout-container."

This is where CSS grid layout becomes powerful. Using a set a predefined properties associated with CSS grid layout, we can set the number of columns and rows, their heights and widths, and their position. Here's how we achieve the layout featured in the photo above:

```css
.grid-layout-container {
  display: grid;
  width: 10rem;
  height: 10rem;
  grid-template-columns: 35% 6.5rem;
  grid-template-rows: 1.25fr 5.5em 1fr;
  grid-template-areas:
    "header header"
    "nav body"
    "footer footer";
}
```

In the above code, we see that there are two values assigned to the grid-template-columns property. This tells the browser to render two columns at the assigned width values. These widths can be in any CSS units, including fractions (fr) and auto.

The grid-template-rows property value lists three values, which tells the browser to render three rows.
The browser won't know what to render in those columns and rows until you assign the grid-area names of the individual design components into the grid-template-areas property. We do this using the grid-template-areas property. The property values use the four major design components grid-area property value names to assign these design components positions within the pre-defined grid or rows and columns.

Study and manipulate the Codepen example below to get a feel for how grid layout works.   

CSS grid layout can be used for page layouts, component layouts, form layout, or in any other use case you can imagine.


# CSS Display Property

## Introduction

So far you've learned about the flex and grid display property values. There are several others that are important to understand. This page will introduce some of these.  

## Prerequisites

A basic understanding of HTML
A basic understanding of CSS selectors and properties

## Understanding the Display Property Values

Below is a list of the most common display property values:

**block**: An element takes up its own space, meaning it covers the entire width of the page and neighboring elements are positioned to either side of the element
<br />
**inline**: An element does not generate line breaks before or after itself. In a normal layout, the next element will be on the same line if there is space
<br />
**inline-block**: Similar to inline, except that you're able to assign a height and width
<br />
**table**: An element behaves like the table html tag
<br />
**none**: An element is removed from the DOM without being deleted. Surrounding elements will fill in to the space of the element with the display property value of none. Often paired with Javascript to make element disappear and appear at the click of a button.  

These are just a few of the most common display property values that you will work with. For an exhaustive list, visit [Mozilla Developer Network CSS display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)


