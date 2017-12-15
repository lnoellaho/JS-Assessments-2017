### Javascript Course Assessment

## Week 2 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. How do you link a css file to your html page?

 //Your Answer
 <link rel="stylesheet" href="./.css">

 //Googled Answer
 <link rel="stylesheet" type="text/css" href="./.css">


 #### 2. What is a css class? How do you use declare one in html? How do you use it in css?


 //Your Answer
 A class in css is basically a name you give to elements on your page. You can give more than one element the same class. That way, by calling on one class, you can style multiple elements the same way.

 You declare a class in the html page by putting class="className" within the tags of the element. In css, you call the tag by puting a period in front of the class name. For example ".className", followed by your curly brackets.

 //Googled Answer
The .class selector selects elements with a specific class attribute. To select specific elements with a specific class, write a period (.) character, followed by the name of the class.


#### 3. The class "heading-box" exists in our html file - write the css code that would:
##### 1) align this box to the center of its container,
##### 2) give it a black border that is 5px wide,
##### 3) make its text appear in the center of the box


#### 4. What is Bootstrap? Explain a few reasons that you might choose to use it in a project?


 //Your Answer
 .heading-box {
     margin: auto;
     width: 80%
     border: 5px solid black;
     text-align: center;
 }

Bootstrap is a library that you can use in your html to facilitate styling. I may choose to use it in a project because it makes styling an app very easy. It is especially useful when you need your app or webpage to be responsive to screen size changes.

 //Googled Answer
 .heading-box {
     margin: auto;
     width: 50%;
     border 5px solid black;
     text-align: center;
 }

 Bootstrap is a free front-end framework for faster and easier web development. Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels, and many other things. Bootstrap gives you the ability to easily create responsive designs.


#### 5. Name 4 semantic html tags.
<header>
<table>
<footer>
<nav>

#### 6. What is block scope that became available in ES6? Include how it differs from local and global scope, and what variables are block scoped.

 //Your Answer
Block scope that became available in ES6 included the variables let and const. Block scope differs from local and global scope because it is a type of local scope. It assigns things to its variables, and these variables/things assigned to these variables are only available within the curly brackets where they are placed.

 //Googled Answer
 The new ES6 keywords let and const allow developers to scope variables at the block level (the nearest curly brackets).


 #### 7. What is front end development? Can you identify any tools/skills that are uniquely required of front end developers?

 //Your Answer
Front end development is developing the view or user side of an app or website. I think html and css are definitely skills that front end developers need to use. Javascript also seems to be a front-end language.

 //Googled Answer
Front end development is the practice of producing HTML, CSS, and JavaScript for a website or Web Application so that a user can see and interact with them directly.

 #### 8. Choose one of the new ES6 concepts we learned about this week (namely: block scope, classes, and string interpolation) and write example code that demonstrates the concept, with comments to explain what is going on.

 string interpolation
`This is a string to show how you can add ${elements} or ${variables} to a string without using separate strings with plus signs.`

 #### 9. What is the difference between a div and a span?


 //Your Answer
A div is used to section your html into blocks. A span is used inside of sections and html tags to insert something inline.

 //Googled Answer
 The difference between span and div is that a span element is in-line and usually used for a small chunk of HTML inside a line, whereas a div element is block-line and used to group larger chunks of code.

#### 10. How would you explain the idea of "inheritance" in object oriented programming?


 //Your Answer
 Inheritance in object oriented programming is when a child class inherits the attributes of the parent class that it extends. When we make a child class that extends some parent class, we can get every single attribute and method that the parent class contains.

 //Googled Answer
 In object-oriented programming, inheritance is when an object or class is based on another object or class, using the same implementation. Inheritance is a mechanism in which one object acquires allthe properties and behaviors of the parent object.
