## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
```
That I actually really enjoy JS. Mostly, the intermission work was review of stuff we'd done in Mod 3.
```

2. What are some tools to help debug JavaScript code?
```
console.log();
debugger;
using the different tabs in the console
```

3. What are some tools you need in order to unit test your JavaScript?
```
Mocha will help you run your tests
Chai will help you build your tests
```

4. What is the syntax for invoking a function?
```
functionName();
```

5. What is CORS?
```
CORS is a method to share resources between domains, e.g. a call to an API in one domain to get information for another domain.
```

6. How do we enable CORS?
```
... Mostly, I just added the methods I wanted access to in config/application.rb... Umm... Is there a gem? Do you just ask the internet and blindly follow their rules? Surly there's docs somewhere... ;)
```

7. What's `this` in JavaScript?
```
huge.
Also, it's a much bigger version of 'self' in Ruby. Depending on where you call 'this', it could be any of a myriad of different content. 'this' could be the window or it could be a particular line you are clicking on. It's scope changes depending on where you are in your code.
```

8. What is Webpack and why is it useful?
```
Webpack is a way of organizing and utilizing your resources (e.g. all your .scss and .js files) in your app. Instead of individually including each file on each page that requires it, webpack will condense them all down and do the including for you. Nifty.
```

9. When/why do you want to use event delegation?
```
When you have resources that are being dynamically loaded on the page. For example, if you have content that loads after it makes an API call, that content will not be available on $(document).ready. If you need to access that content after the document loads, you need to bind it to another element that is found on $(document).ready and call it from there.
```

10. What is a callback function?
```
A callback function is a function that is passed to another function as a parameter and then is executed inside the original function. Function. Function. Function...
```

11. What's `npm` and what do we use it for?
```
npm = Node Package Manager. It's basically the gem of JS. It allows developers to share packets of code to simplify their coding in the future. 
```

#### Review  
12. What's the MVC design pattern? Describe each part of MVC.
```
Models - access the database, find specific information, do most of the logicing, all your fancy methods are belong to us
Views - render the content they're told to by controllers, do almost no logicing, none of your fancy methods belong in here
Controllers - do minimal logicing, act as the go between for views and models, your fancy methods might be called in here
```

13. What are a few ways to optimize a Rails application?
```
Keep all logic in the Model
Use ActiveRecord as often as possible to manage and access information in your database
```

14. What's a background worker? When would we want to use a background worker?
```
A bit of code that goes off to do thing by itself. Rails processes information in the order it receives it. This means you can come across bits of code that might be monsters at consuming resources. Instead of holding up the application waiting for a long process to complete, we can use a background worker to go complete the process while the app moves on it's merry little way. They're another handy tool for optimizing Rails apps.
```
