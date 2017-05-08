## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
```
GET - retrieves information from the database
PUT - changes information on the database
POST - adds information to the database
DELETE - removes information from the database
PATCH - updates information on the database
```

2. What is Sinatra?
```
A server we can use to see what our pages look like live.
```

4. What is MVC?
```
Models, Views, Controllers. The files that make up our pages.
Models = classes.
Views = pages.
Controllers = routes between pages.
```
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
```
To make it easier to read? Because that's the way it's required in Rails and that's what we're moving to next?
```

6. What types of variables are accessible in our view templates without explicitly passing them?
```
Instance variables.
```

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  ```ruby
  get '/horses' do
    @count = 1
    erb :index, :locals => {:name => 'Mr. Ed'}
  end
  ```

9. What's the purpose of ERB?
```
It allows you to use ruby functions in your HTML. That way we can update dynamically update the number of horses we have in our stables instead of manually changing the number.
```

10. Why do I need a development AND test database?
```
You don't want to make changes to your development database. You're going to be running your tests several times and you want to be able to clear out the data you're playing with. Additionally, your development database probably contains all the data you will use in production. Rather than loading all of that data whenever you need access to it, you can use smaller sample sets.
```

11. What's responsive design?
```
Design that allows for different screen sizes. If Kanye's picture should be a picture taking up most of the screen on a computer, you might focus in on Kanye's face for the mobile site.
```

12. What is CRUD and why is it important?
```
Create
Read
Update
Delete

It's all the tools you need to manage a database. By coding with CRUD in mind, you can plan your processes better.
```

13. What does HTTP stand for? 
```
HyperText Transfer Protocol
```

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
```
<% RUBY TO BE INTERPOLATED %>     = This method will perform the ruby requested, but doesn't display anything to the page
<%= RUBY TO BE INTERPOLATED %>    = This method will perform the ruby requested, and then displays the result to the page
```

15. What's an ORM?
```
Object Relational Mapping.
Basically, it's working with databases. It's what Active Record does for us.
```

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
```
Active Record
```

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
```
Create + GET    = render the page with the form to make a new restaurant
Create + POST   = take all the info I just gave you in the form and add a new restaurant to our database
Read + GET      = show me all the objects of all restaurants
Read + GET      = show me the details of one particular restaurant
Update + GET    = show me the form to update a restaurant, preferrably showing what's currently living in all the fields
Update + PUT    = take any changes I made to the form and update the restaurant with them
Delete + DELETE = obliviate this restaurant
```

18. What's a migration? 
```
It's how we make a new database and make changes to existing databases. It controls the structure of the database, not the content.
```

19. When you create a migration, does it automatically modify your database?
```
No. You have to run it first. 
```

20. How does a model relate to a database?
```
A model is the object that each item on the database is made up of. So for our horses, they are all instances of horse that are held on our horses table inside our database.
```

21. What's the difference between agile workflow and waterfall method?
```
Agile has you getting tasks done in iterative methods. Rather than complete the project before you test it, for example, you test as you go so you know what you have works.
Waterfall treat projects as chunks. First you design. Then you Create. Then you test. The problem with this method is the later portions of the process don't get to have input on the former when they really should.
```

22. What is the difference between `#new` and `#create`?
```
#new makes a new instance of an object on a table, but it doesn't save it to the database.
#create makes a new instance and saves it at the same time.
```
