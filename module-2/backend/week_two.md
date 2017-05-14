## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
```
AR is an SQL tool used to access data stored in a database. It does Object Relational Mapping to allow the user to access data.
```
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
```
Team.all
Team.count
Team.find(1)
Team.find_by(name: "George")

We have access to these methods because they are defined in ActiveRecord and are available for our use through that tool.
```

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

```ruby
Team.find(4)
Owner.find(Team.find(4).owner_id).name
```

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

```
Team.owner.name
```

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

```
many to many

students:
id
f_name
l_name

teachers:
id
f_name
l_name
subject

student_teachers:
student_id
teacher_id
```

6. Define foreign key, primary key, and schema.
```
foreign key: the id of a table elsewhere in the database that references an object in that table.
primary key: the id of each object in a table in a database.
schema: the layout of your database. it shows how objects are connected and which tables relate to which and how.
```

7. Describe the relationship between a foreign key on one table and a primary key on another table.
```
the foreign key on one table is the primary key on another table. the foreign key is used to give access to the full content of an object on another table.
```

8. What are the parts of an HTTP response?
```
I had to look this up to have any idea how to answer it...
The response is made up of the:
Status line: 
Status code & reason: the protocol version followed by a numeric status code and its associated textual phrase
    And I think this bit is fascinating:
      - 1xx: Informational - Request received, continuing process
      - 2xx: Success - The action was successfully received,
        understood, and accepted
      - 3xx: Redirection - Further action must be taken in order to
        complete the request
      - 4xx: Client Error - The request contains bad syntax or cannot
        be fulfilled
      - 5xx: Server Error - The server failed to fulfill an apparently
        valid request
Response Header Fields: allow the server to pass additional information about the response which cannot be placed in the Status- Line
```



### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
```
.find: quick way to look up something when you have its ID
.find_by: when you don't have an id, but need to find something
.where: limits the returns you have so you can retrieve a list of objects that meet your specifications
.select: similar to where, it allows you to limit returns
.create: add a new object to the table
```

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
```
rake db:create - create a new database
rake db:migrate - go through existing migrations and make any changes written to the database
rake db:create_migration NAME=create_new_table - make a new migration
```

3. What two columns does `t.timestamps null: false` create in our database?
```
created_on
last_changed
```

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
```
most likely, one-to-many. The school will have many teachers, but the teacher will all work at one school.
```

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
```
in the migration for schools, have a column for teacher_id
in the migration for teachers, have a column for school_id
in the model for Teacher, include belongs_to :schools at the top
in the model for School, include has_many :teachers at the top
```

6. Give an example of when you might want to store information besides ids on a join table.
```
Movies shown in many movie theatres still need to be able to list their showtimes.
```

7. Describe and diagram the relationship between patients and doctors.
```
many to many. 
make a join table where patients can have several doctors and doctors can have many patients.
on the join table, there might be a column for type of practice.
```

8. Describe and diagram the relationship between museums and original_paintings.
```
one to many
museums would have many original paintings.
original paintings would belong to one museum.
```

9. What could you see in your code that would make you think you might want to create a partial?


