## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
```
Node is a JS environment that allows for asynchronous processing of tasks.
```

2. What is Express? Why is Express similar to in the Ruby world?
```
Express:JavaScript::Rails:Ruby
It is a framework to help you organize your application. Except, without all the support that Rails provides. Which means you get to make up your own rules.
```

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
```
const app = require('express')()

app.get('/', () => {
})
```

4. What do we use Knex for?
```
Knex is used to make database calls. E.G.

const knex = require('knex')
knex.raw('SELECT * FROM kitties') // side note: this would be the best day ever... ALL THE KITTIES!
```

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
```
Use server.js to be your routes file.
Create a model for every table in your DB. Move any DB calls and logic into the model.
Create a controller for each model to communicate between server.js and the model.
```

6. How do you execute raw SQL in node?
```
const knex = require('knex')
knex.raw('SELECT * FROM kitties') // BEST. DAY. EVER. All the softness and the paws!!!
```

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
```
Advantages: taking SRP to the next level. Each application has one job to do, i.e. deliver a front end or deliver a back end.
Disadvantages: getting the applications to talk to each other. Rather than just doing a database call from within a single app, you have to call to another app to get the info for you.
```


#### Review  

8. Describe DNS.
```
Domain Name Service. When you go to a web site, the DNS server will convert the text to an IP address and do a lookup for that address. If it doesn't find it locally, e.g. in your browser, it escalates the request to the next highest DNS, maybe your router. If it doesn't find it there, it continues to move the request up the chain until it finds the information it's looking for.
```

9. What does writing clean code mean to you?
```
Primarily, it's easy to read. Someone who didn't write the code should be able to come in and look at it and know what's going on.
Secondarily, there isn't any repetition. If there is, pull it out into it's own function. Or find another way of writing your code to automate the process.
Thirdarily, it uses the most efficient tools available. Rather than using EACH, you maybe use other array prototypes.
```

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?
```
Building: The state of the building, it's address, phone, breakfast?, on site amenities(e.g. pool?, recreation room?...)
Room: sq ft, #beds, size of bathroom, various amenities (e.g. hair dryer, cable...)
Staff: position, work hours, duties, pay, name, 
```
