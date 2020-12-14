# Part 10: Specificity

## Introduction

Oftentimes developers will add different styles to the same component. For instance, a stylesheet may have a type selector that states that all HTML div elements have a background color of black. And then elsewhere on the stylesheet a div element is selected by its class name and given a background color of blue. The rules of specificity determine which background color gets rendered by the browser. Understanding CSS specificity will help prevent frustration and give you added confidence when styling a document.

## Prerequisites

A basic understanding of HTML
A basic understanding of CSS selectors and properties

## Understanding the Rules of Specificity

The concept of specificity is closely related to the namesake of Cascading Style Sheets, namely the "cascading" reference. The cascade refers to the series of rules that control which CSS declarations render in the browser in the case of conflicting instructions within the stylesheet.

Let us consider the HTML component below.

```html
<div class="my-class" id="my-id">My HTML Component</div>
```

As developers, we can select this component in our stylesheet in several ways: by type (as div), by class (as .my-class), and by id (as #my-id). In the example below, I'll select this component using all three and discuss the rules of specificity as we consider which selector's property and property value declaration the browser will render.
In the below example, we've styled our component using the class selector. The background of the html component will be red.

```css
.my-class {
    background: red;
}
```

But due to design requirements elsewhere in the project, you now have to style the div type. Our style sheet now look like this:

```css
.my-class {
    background: red;
}

div {
    background: white;
}
```

The rules of specificity now come into play. And since a class selector is more specific than a type selector, the background color of our html component remains red.
The design requirements have changed again, and I need to change the html component to a background of black. The problem is, the .my-class selector applies to multiple components sprinkled throughout the project. And since I only need to change this specific component, I'll use the id selector. See below:

```css
.my-class {
    background: red;
}


div {
    background: white;
}


#my-id{
    background: black;
}
```

Since the id selector is more specific than the class and type selectors, our component now has a background color of black.

In the case that two rules apply that have equal specificity, the declaration that comes last in the CSS stylesheet is the one that will be used.

This tutorial is just an introduction, and there are more rules that will apply to more complex situations. But by understanding the concept of specificity, you'll be able to troubleshoot an issue like this in your code if it arises.

[The Mozilla Development Network: Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) is the de facto authority on these rules and is where you'll want to explore if you run into a problem.

## Understanding Inheritance

Inheritance is when CSS properties, by default, inherit values set on the that element's parent element. Not all CSS properties transfer from parent to child, but when they do, they can produce unintended behavior.

An example of a property that provides inheritance by default is font-family. If you assign a specific font-family to the body tag, this font-family will become the font rendered in every component nested within the body. As a developer, you can assign differing font-family property values to individual components, classes, and id's in order to render a font-family that differs from that assigned the html tag.

As a developer, there are other ways to alter inheritance. Every single CSS property accepts the following property values related to inheritance:

**inherit**: sets the property value to be the same as that of its parent element
<br />
**initial**: sets the property value applied to a selected element to the default value
<br />
**unset**: resets the property to its natural value, which means that if the property is naturally inherited it acts like inherit, otherwise it acts like initial.

*According to the rules of specificity, directly targeted elements will always take precedence over rules which an element inherits from its ancestor.

## Conclusion

You've just learned about CSS specificity and inheritance.
