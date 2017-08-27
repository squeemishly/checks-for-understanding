## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
```
ES6 has significantly more syntactic sugar than any of the previous ES's. A few syntactic sugars that ES6 adds:
- class syntax
- fat arrow functions
- const & let instead of var
- static functions
```

2. What's the difference between asynchronous and synchronous JavaScript? 
```
synchronous JS runs in the exact order the commands are given
asynchronous allows you to run processes that take longer outside of the order they are entered. It will start the asynchronous process in the order it was entered, but it will complete the process on the side. When it is done with it's process, it will jump back on the stack to allow any promises it has to complete.
```

3. What are the four pillars of Object Oriented programming?
```
Abstraction - move independent concepts into their own methods. this increases readability and reusability.
Encapsulation - make methods that can be hidden from public view (e.g. private methods) hidden. this restricts access to essential components of your code that you don't want the average person to have access to.
Inheritance - reuse as much code as possible. I can use string methods in my "Animal" class without having to write them myself. My code automatically inherits all the methods associated with strings. If I declare a class "Animal" with a method 'walk' and then declare a subclass "Dog", I have access to 'walk' on "Dog". 
Polymorphism - Sometimes, like when our parents are hoarders, we inherit things we don't want. Polymorphism allows us to redefine methods on classes. A classic example of this is the '+' operator. On the Integer class, we combine 2 numbers to come up with another larger number. On the string class, we concatenate 2 strings and end up with a longer sentence.
```

4. What are some tools available in JavaScript to help you write object oriented code?
```
Constructor functions allow you to make new classes.
In ES6, you actually have the ability to declare a 'class'. 
Hashes are by default JS objects and are treated the same way as classes in Ruby.
```

5. What are some key concepts to be aware of when refactoring your JavaScript?
```
If you refactor out a function from a promise chain, don't include the paranthesis on the called function. If you need to pass in variables, declare an anonymous function and call the new function inside it. There you can pass in variables without immediately invoking the function. 
Refactoring allows you to better unit test your code. The more you can pull out into individual functions, the easier it is to test and the easier it is to reuse. 
```

6. What's a callback function and what are some reasons when we use/need callback functions?
```
A callback function is a function that passed into another function as a variable. We might need to use them in promise chains or to tell events handlers what to do when a certain button is clicked.
```

7. What's the scope of variables in Javascript?
```
Global variables are declared outside the context of any function and are accessible to any function in your code. 
Local variables are declared inside a function and are only accessible inside that function. If you need to access them in a dependant function, you must pass them in.
```

8. What's the difference between `==` and `===` in JavaScript?
```
== 'equals': checks to see if 2 objects equal each other on a simple level. E.G. "2" == 2 //true. "I am squee!" == "I am squee!" //true. true == true //true
=== 'strict equals': Means the objects must be the same datatype and be exactly the same.  E.G. "2" == 2 //false. "I am squee!" == "I am squee!" //true. true == true //true
```

9. Why do front end frameworks exist?
```
Because jquery is bulky and slow. Much like Rails exists to take the repetitive load off a developer who might otherwise use Sinatra to write an app, React is there to make it easier to dynamically load and change information on the page. 
```

#### Review  

10. Why do people say "HTTP is stateless"?
```
It doesn't retain information about who you are and what you are doing in any particular app. It continues to occupy the same state before, during, and after your visit to a site. 
```

11. Describe a RESTful API.
```
A RESTful API uses the HTTP verbs in the appropriate ways with the appropriate URLs. It uses a GET request to receive information from the API and the address should look something like /api/v1/thing_i_want. GET should never be used to update, add, or delete information. There are other verbs for that. POST should always be used to make a new item, PUT should be used to update items, and DELETE should be used to remove items. 
```

12. What are some main characteristics of a team following an agile workflow?
```
Agile workflow means that a team isn't just stuck in one section of the development process until it's done. A team using agile will be continuously cycling through designing the app and the user experience, testing the code developed, writing code, and talking to their clients.
```

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
```
Advantages: users don't have to remember their password on your app. apps that require information from the oauth can get it. Most places that you would use OAuth with will have more resources than your startup. Their security is likely to be better.

Disadvantages: it can be a HUGE invasion of privacy. also, it relies on an outside service that may have it's own complications/downtime/attacks/etc to contend with. The service itself might change which could cause havoc in your app.
```
