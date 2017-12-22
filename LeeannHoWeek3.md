### Javascript Course Assessment

## Week 3 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Here is a list of pros and cons to using the React library to build your application -- but some of them are false. Remove the false statements from the list:

- React is a modern, efficient answer to complex UI applications

- React is a flexible library that plays the role of V in an MVC framework


 #### 2. What are "smart" and "dumb" components? Explain the difference and also add why we bother to make the distinction between them.


 //Your Answer
 Smart components hold the logic parts of your code, and dumb components are static. We make the distinction between them because our smart components take care of state and can change what happens to our application, but the smart components are just templates for information.

 //Googled Answer
 Dumb components are also called 'presentational' components because their only responsibility is to present something to the DOM. Once that is done, the component is done with it. Smart components (or container components) on the other hand have a different responsibility. Because they have the burden of being smart, they are the ones that keep track of state and care about how the app works.  

#### 3. Write a simple component that simply prints "I am a dumb component" to the screen. Be sure to include all necessary imports, exports, etc...
import React, {Component} from 'react'

class Dumb extends Component {
    render() {
        return (
            <div>
                <p>I am a dumb component</p>
            </div>
        )
    }


export default dumb

#### 4. When we use "yarn add ..." in the terminal - what is yarn doing? And what file will always be automatically updated after we add a package with yarn?


 //Your Answer
 When we use yarn add, we are adding a dependency to a project. The package.json file will always be automatically updated after we add a package with yarn to include the dependencies that we added.  

 //Googled Answer
 In general, a package is simply a folder with code and a package.json file that describes the contents. When you want to use another package, you first need to add it to your dependencies.This means running yarn add [package-name] to install it into your project. This will also update your package.json and your yarn.lock so that other developers working on the project will get the same dependencies as you when they run yarn or yarn install.

#### 5. There are three mistakes in this code that would cause it to break our application. Find the mistakes and fix them:

    import React, { Component } from 'react';

    class Recipes extends Component {
      constructor(props){
        super(props)
        this.state = {
          recipes: [
            {name: 'Meatballs'},
            {name: 'Mac & Cheese'}
          ]
        }
      }

      render() {
          let recipes = this.state.recipes.map(function(recipe){
            return(
              <li key={recipe.name}>{recipe.name}</li>
            )
          })
        return (
            <div>
                <ul>
                    {recipes}
                </ul>
            </div>

        );
      }
    }

    export default Recipes;

#### 6. Name three input types. (NOTE: text is the default type - so it doesn't count in this case)

 //Your Answer
Button, submit, radio

 //Googled Answer
checkbox, file, email, password, etc.

 #### 7. How would you explain state to a friend who doesn't know code?

 //Your Answer
I would tell them that state is the condition and information that a site or app is currently displaying. You can send new information, and perform an action on a webpage, but it won't update until the state is updated.

 //Googled Answer
Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.

 #### 8. What is the difference between component state and props? Your answer should include a short explanation of both.
Props are set by the parent, and are connected to the state in the parent component. State is used for data that is going to change, and usually we use state in the parent component, because it is the smart component.

 #### 9. Name three benefits of testing and TDD:


 //Your Answer
 Testing and TDD are beneficial to development because it forces the developers to write better code because the code you write needs to pass a specific test, rather than just writing code to do something you want it to do. It also helps with finding bugs sooner, rather than later. You have to stop and check if your tests are passing. Setting up tests also makes it a lot easier to pinpoint bugs later on when you're project is finished. The more tests you set up, the easier it will be to see where your code is breaking.

 //Googled Answer
When writing some new code, you usually have a list of features that are required, or acceptance criteria that need to be met. You can use either of these as a means to know what you need to test and then, once you've got that list in the form of test code, you can rest safely in the knowledge that you haven't missed any work.

Because you're writing a test for a single piece of functionality, writing a test first means you have to think about the public interface that other code in your application needs to integrate with.

Once you've got a test passing, it's then safe to refactor it, secure in the knowledge that the test cases will have your back.

#### 10. List two helpful testing matchers and two helpful enzyme simulators that we can use when writing our tests:


 //Your Answer
 .toEqual(), .toContain()
.simulate('click') .simulate('change')


 //Googled Answer
 .toBeNull() .toBeUndefined() .toBeDefined()
 .simulate('click') .simulate('change')
