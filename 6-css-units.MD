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

## Conclusion
There are endless debates on what units and unit strategies work best for responsive web design. This tutorial introduced you to some basic units used in responsive web design. To learn more, you'll benefit from reading code. This can often be done directly in Chrome for any website using Chrome dev tools inspect tooling.
