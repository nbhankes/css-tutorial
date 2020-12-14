# Part 2: Linking HTML to CSS Stylesheet

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
  
## Conclusion
You just learned how to link a style sheet to an HTML file. Continue on to learn how to add styling to your HTML file.
