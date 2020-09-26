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

Margin is the spacing between the your content's border and any adjacent HTML elements. The property declarations are the same as padding.

## Conclusion
You just learned about the CSS Box model, the border property, the padding property, the margin property, and gained some familiarity with the ways in which they can change how HTML elements render in the browser. Continue to the next tutorial to learn about CSS units.
