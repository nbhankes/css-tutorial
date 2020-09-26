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

## Conclusion
You just learned of different ways to select an HTML element from within your style sheet file. Continue to the next tutorial to learn about CSS Properties and how these can alter the ways in which the selected HTML elements render within the browser. 
