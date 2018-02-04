### Javascript Course Assessment

## Week 5 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. Comment this code from an express server to explain what each part is doing.
//this is sending "hello world" to the url path / when a browser requests that address
app.get('/', function (request, response) {
 response.send('Hello World!');
});
//this is listening for requests from port 3000 server, and will be sending information to that server.
app.listen(3000, function () {
 console.log('Example app listening on port 3000!');
});



#### 2. We have now used both EJS and React to render views with dynamic javascript content (If you want a refresher, take a look at the "Full Stack Express" day). Compare and contrast the two approaches, include a pro and con of each. Which one did you prefer?

// Your answer
EJS /pro- simple syntax
    /con- too simple. hard to understand how to save state

React /pro- saving state and separation of components
      /con- confusing at first because of state and props

I think ultimately, I prefer React because once I got the hang of using state and props, I felt a lot more comfortable passing around information to my components, and this makes the whole application more versatile.


#### 3. Sequelize and Express are the Model and Controller portions of our MVC structure. How the two relate and pass information between each other is important to understand but can be hard to follow. Below are some generic events that happen when a browser requests a web page, but they are not in order. Put them in order and also specify whether the task is done by Sequelize or Express. The first step has been given to you as an example:

1. Server is set to "listen" for requests coming in on a port, or range of ports (Express)

----- organize from here down:
5. Incoming requests are handled by the router (Express)

4. If incoming requests require information from the database, the request is parsed into a SQL query (Sequelize)

3. SQL responses are translated into a javascript object (Sequelize)

2. The content required for a view is sent back to the browser, along with any additional information required      (Express)

** Understanding this process will be important to building full stack apps, if you have any questions about this process, write them here and I will answer them with you in the future:


#### 4. We implement back end tests with Jest and Supertest, look back at the "Testing Express" day and do a few minutes of outside research to understand what this code is doing, and what it is testing. Add comments explaining your findings.

** Also comment any piece you don't understand with questions, and I will get back to you.


const request = require('supertest')
const app = require('./App.js')

//expecting the response when requesting for / to be status code 418
describe('Test the root path', ()=>{
  it('Should respond to GET', () => {
    return request(app).get('/').then((response)=>{
      expect(response.statusCode).toBe(418)
    })
  })
//expecting to get 'Relax, and have a cup of tea' when requesting for / page
  it('Should respond with a message of "Relax, and have a cup of tea", ()=>{
    return request(app).get('/').then((response)=>{
      expect(response.body.greeting).toBe('Relax, and have a cup of tea')
    })
  })
})


#### 5. What are cookies and sessions? Try to explain what they are, and any differences between them that you remember.

//Your Answer
A cookie is a part of a request managed by the server that gets passed back to the browser. Sessions work with cookies, and are only stored in the server. It is accessed through a cookie.

 //Googled Answer
 A cookie is a small piece of text stored on a user's computer by their browser. Common uses for cookies are authentication, storing of site preferences, shopping cart items, and server session identification.

 Each time the users' web browser interacts with a web server it will pass the cookie information to the web server. Only the cookies stored by the browser that relate to the domain in the requested URL will be sent to the server. This means that cookies that relate to www.example.com will not be sent to www.exampledomain.com.

 In essence, a cookie is a great way of linking one page to the next for a user's interaction with a web site or web application.

 A session can be defined as a server-side storage of information that is desired to persist throughout the user's interaction with the web site or web application.

 Instead of storing large and constantly changing information via cookies in the user's browser, only a unique identifier is stored on the client side (called a "session id"). This session id is passed to the web server every time the browser makes an HTTP request (ie a page link or AJAX request). The web application pairs this session id with it's internal database and retrieves the stored variables for use by the requested page.

#### 6. Try to explain the process of how information from a user can be persisted to a database using a form, the "post" method, sequelize, and express.  Look back at the "Full Stack Express" day for a refresher.

 //Your Answer
A user enters information into a form, which takes the data and sends the information to the server using the "post" method. On the server side, the post.get method will receive the request with express to post information, and it will handle taking the information to sequelize. Sequelize will take the requested information and actually put it into the model or table, thereby creating or updating an instance of the table.

 //Googled Answer

 That we are sending form data to server using POST method. Basically when you click Submit button, your browser will create a HTTP Request and once it’s authenticated from server, you will receive HTTP Response from the server.

 Technically HTTP Request and Response has two things, HTTP Header and HTTP Body if your method is POST.
#### 7. What is sequelize "seed" data for? Why can it be helpful as you develop a project?

 //Your Answer
Sequelize "seed" data is like sample data that goes into your database to create the first instances of your models. This is helpful when you are developing a project, because you can use that data to test your code. Without any seed data, you wouldn't be able to be sure that your view is rendering the information correctly, because there would be no information to render.

 //Googled Answer
 Seed data is anything that must be loaded for an application to work properly. An application needs its seed data loaded in order to run in development, test, and production. Examples can include: initial accounts for the application administrator and client users.


#### 8. Red, Green, Refactor is the process for TDD - what does this mean to you right now, and what do you think it might look like to do this in a work environment?

Red, means you wrote a test that doesn't pass. Then you write code specifically to make the test pass, or turn green. Refactor is improving your code, or even writing a more specific test.

#### 9. This is an example express application on github: https://github.com/shapeshed/express_example. Take a few minutes to go to the address and look around in the files. List a few things here about the project - what do you notice that is different about their setup? What looks familiar from class? What sticks out to you or gives you questions?

They use express, but they have an index.js file and an app.js file that looks the same as our app.js files. Their view folder contains .jade files, which looks like a form of html, but it isn't html.


#### 10.  Try to explain what an express router does in your own words.

 //Your Answer
An express router will take a browser's request, and match it to a corresponding route or endpoint and HTTP method. Then it will run the callback function associated with it. Usually, the callback will involve pulling information from the database using sequelize.  And then we will send the information to the browser in the form of JSON.
