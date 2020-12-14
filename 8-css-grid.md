# Part 8: CSS Grid

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

## Conclusion

You just learned about CSS grid layout. The above example does not cover the full capabilities of grid layout, so be sure to do your own research once you come across a possible use case.
