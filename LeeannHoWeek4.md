### Javascript Course Assessment

## Week 4 Assessment

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

#### 1. SQL stands for Structured Query Language. In your own words (no need to write a googled answer), what role does SQL play in a full-stack web application? How does this relate to MVC organization?
    SQL is part of the Model in MVC organization. With SQL, we can utilize a database and store and retrieve information for our application.


#### 2. Here is a basic SQL query. What are the various parts of this statement doing? (Comment the code to explain each piece)

     SELECT //selecting certain table columns
      name,
      breed,
      vaccinations,
      age * 15 AS equivalent_human_age, //renaming age to equivalent_human_age
    FROM // naming the table we are selecting from
      mydogs
    WHERE //only selecting instances where equivalent_human_age is greater than 20
      equivalent_human_age > 20
    ORDER BY //ordering our results by the equivalent_human_age descending order
      equivalent_human_age DESC



#### 3. What is a foreign key?

// Your Answer
    A foreign key is the key that shows the relationship between a table and the table it belongs to.

// Googled Answer
A FOREIGN KEY is a field (or collection of fields) in one table that refers to the PRIMARY KEY in another table.

The table containing the foreign key is called the child table, and the table containing the candidate key is called the referenced or parent table.

#### 4. What is this Sequelize code doing? Comment the code to explain each peice.

    ComicBook
      .all({limit: 2}) //grabbing 2 instances of ComicBook
      .then(function(comics){
      let mapped = comics.map(function(cb){
         return cb.get() //mapping through the comicBooks that we grabbed, and return each one so that we can use them individually
      })
      console.log(mapped)
    })

#### 5. Try to explain the role of an ORM in a full-stack application. Include at least two benefits of implementing an ORM.

//Your Answer
 Object relation mapper allows us to treat the tables in our database as classes in our code, and the rows as instances in our classes. This makes it a lot easier for us to work with the database in our code without having to type out regular SQL queries.

 //Googled Answer
 Object-Relational Mapping (ORM) is a technique that lets you query and manipulate data from a database using an object-oriented paradigm. When talking about ORM, most people are referring to a library that implements the Object-Relational Mapping technique, hence the phrase "an ORM".

 An ORM library is a completely ordinary library written in your language of choice that encapsulates the code needed to manipulate the data, so you don't use SQL anymore; you interact directly with an object in the same language you're using.
 Pros:
 DRY: You write your data model in only one place, and it's easier to update, maintain, and reuse the code.
 A lot of stuff is done automatically, from database handling to I18N.

#### 6. Write a command to alter the TABLE water_monsters in the monster DATABASE to name it "sea_monsters" instead.(assume we are using a postgres databse)

 //Your Answer
 ALTER TABLE water_monsters
  RENAME TO sea_monsters;

 //Googled Answer
 ALTER TABLE water_monsters
  RENAME TO sea_monsters;


#### 7. What does CRUD stand for? And what do we use CRUD actions for?

 //Your Answer
 Create, read, update, destroy. We use CRUD actions for database information.

 //Googled Answer
 When we are building APIs, we want our models to provide four basic types of functionality. The model must be able to Create, Read, Update, and Delete resources. Computer scientists often refer to these functions by the acronym CRUD. A model should have the ability to perform at most these four functions in order to be complete. If an action cannot be described by one of these four operations, then it should potentially be a model of its own.

#### 8. When working with Sequelize, how do we make changes on a table or database level? Give a code example along with your answer.
    Well, we can do Model.create to create a new instance of the model, or we can update the information in an instance.

 Model.findAll
  .then(function(model){
    model.name = "New name"  //update value
    return model.save() // a promise
  })
  .catch(function(error){
  })


#### 9. During the review we came across the idea of primitives types in Javascript but didn't really get to go into detail about them, other than the fact that they sometimes behave differently than objects and arrays. Do 5 min of research about primitives and record your findings here:

 //Googled Answer
 Javascript has five primitive data types:
    1. Number
    2. String
    3. Boolean
    4. Undefined
    5. Null

Each of these five different primitive data types has a corresponding object constructor.

#### 10. Friday's lesson was difficult because Sequelize updated its syntax. What did you think about this problem, and how might you deal with breaking updates like this in the future?

 //Your Answer
 I think this is not a bad problem to have. As long as you read the documentation and understand the new syntax, you can easily fix the issues. Honestly, in the future, I may just make sure to add the previous version in my yarn add. 
