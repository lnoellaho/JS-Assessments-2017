### Javascript Course Assessment

## Week 1 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Name some of the data types in Javascript.

  //Your answer
        Some data types in Javascript are strings, numbers, booleans, arrays, and objects.

  //Googled Answer
        Boolean, null, undefined, number, string, symbol, and object

#### 2. Describe what "if" does in Javascript.

  //Your Answer
        "If" is a conditional statement in Javascript. It determine if a statement is true or false, and can run a block of code based on the condition.

  //Googled Answer
        The if/else statement executes a block of code if a specified condition is true. If the condition is false, another block of code can be executed.

#### 3. Write a function that takes one number as a parameter and decides if that number is divisble by three or not. If it is, print the number and "is divisible by three". If it is not, print that the number "is not divisble by three".
        function divByThree(x) {
            if(x % 3 == 0) {
                console.log(x + " is divisible by three.")
            } else {
                console.log(x + " is not divisible by three.")
            }    
        }

#### 4. What is JSON?

  //Your Answer
        Javascript Object Notation

  //Googled Answer
        JavaScript Object Notation. JSON is a syntax for storing and exchanging data. JSON is text, written with JavaScript object notation.

#### 5. Write about yourself in an object, giving at least three properties of you. Then store your object in a variable with your name.

        var Leeann = {
            mood: "happy",
            weight: "too heavy",
            height: "too short"
        }

#### 6. What is a closure?

  //Your Answer
        A closure is a callback function used to protect the privacy of certain things inside a function, while still making it possible to return and use the results of a function, outside of that function.

  //Googled Answer
        A closure is a function having access to the parent scope, even after the parent function has closed.

#### 7. What's the difference between =, ==, and === in JavaScript?

  //Your Answer
        = sets the value of something. == checks if the value of two things are equal. === checks if the value and type of two things are equal.

  //Googled Answer
        By using = you assign a value to something.
        By using == you check if something is equal to something else. Value-wise.
        By using === you cehck is something is equal to something else, value and type-wise.

#### 8. Create an array with at least 4 items inside it, then access two of the values and console.log() them. Try to access the two values in two different ways.
        var fruits = ["bananas", "oranges", "grapes", "peaches"];
        console.log(fruits[1]);
        var one = fruits.pop();
        console.log(one);

#### 9. Describe the different kinds of loops and why you would use them.

  //Your Answer
        The classic for loop is used when you need to iterate through an array and have a function run through all the items in that array.
        The for in loop is used when you need to run functions for certain items in an array, as opposed to all items. The while loop is used as a conditional. While something is true, you can run your function. The do while loop tells your function to do something, while a certain condition is true.  

  //Googled Answer
        for- loops through a block of code a number of times.
        for/in- loops through the properties of an object.
        while- loops through a block of code while a specified condition is true.
        do/while- also loops through a block of code while a specified condition is true.

#### 10. How would you explain "scope" in javascript?

  //Your Answer
        There are two types of scope: global scope and local scope. It basically describes whether a certain part of your code can see or use another part of your code. For example, if you have a variable in the global scope, any function can use that variable.

  //Googled Answer
        Scope determines the accessibility (visibility) of variables. Javascript has two types of scope: local scope and global scope. Javascript has function scope. Each function creates a new scope. Variables defined inside a function are not accessible (visible) from outside the function.
