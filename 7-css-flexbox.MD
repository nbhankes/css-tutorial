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


## Conclusion
You just learned about CSS flexbox properties and property values. This is a powerful CSS style system that is essential for responsive web design.
