# Part 11: CSS Custom Properties

## Introduction

Once you pick a color palette for your website, you can imagine how often you'll write those color values in your stylesheet. You could have the same color listed as a property value in thirty or more places! Now imagine if your client a team all of the sudden you needed to change your site's color palette? This might not be final, but just to see if one color might look better. You'd have to go through the entire document and change each of those 30+ values!

One way to avoid this is to use CSS custom properties, also known as CSS variables. CSS custom properties are variables defined by CSS authors that contain specific values to be reused throughout a document. This tutorial will show you how to create and use CSS variable.

## Prerequisites

A basic understanding of HTML
A basic understanding of CSS selectors and properties

## Understanding CSS Custom Properties

Let's say our client thinks they'd like their website background to be gray. And all borders are black. Font colors should be white, they say. But you've worked with enough people to know that this will change a few times before the finishing your project, so you decide to set up custom properties. You would create custom properties for each of these colors like so:

/ stylesheet.css
```css
:root {
    --background: gray;
    --border: black;
    --font: white;
    }
```

By declaring the CSS custom properties inside of the root psuedo-class, these custom properties are globally available throughout your entire project. Assigning a custom value to a div declaration means that the custom variable would only be available to div types. This is due to a process referred to as scoping, which you'll learn more about as you dive into JavaScript. But for now, let's carry on with our website design stylesheet, inserting these custom properties into your project like so:

/ stylesheet.css
```css
:root {
    --background: gray;
    --border: black;
    --font: white;
    }

div .header {
    background-color: var(--background);
    border: 5px solid var(--border);
    color: var(--font);
    }
    
h1,
h2,
h3,
h4 {
    color: var(--font);
    }
    
body {
    background: var(--background);
    color: var(--font);
    }
```

Now your html is styled with the property values assigned to your custom properties of --background, --border, and --font. As you can see, if you needed to change the color palette of the entire website, all you would need to do is change the property value assigned to your custom property declarations inside of the root pseudo-class.

The benefits of CSS custom properties are not limited to colors and you're really only limited by your imagination.

## Conclusion 

You just learned about CSS custom properties. You now know how to create and use these custom properties throughout your stylesheet.
