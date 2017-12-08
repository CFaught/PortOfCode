+++
author = "Caleb Faught"
categories = ["Programming"]
date = "2017-10-19"
description = "Programming may sound intimidating, but with determination and the right resources, I think anyone can learn how to code."

linktitle = ""
title = "How to Learn Programming as a Beginner"
type = "post"
draft=false
+++

# Anyone Can Learn to Code

I believe that a lot of people approach the idea of programming with a bias built up from hearing about guys from MIT and Harvard starting revolutionary projects causing people to think that programmers need to be mathematicians or computer science majors to become competent at developing applications. And while it's true that there are a lot of super smart people in the community who have pioneered the technology, there are also just as many average Joe's out there with good ideas that are able to pick up programming and build great things.

There are a couple of factors that allow for this:

* Abstraction - Programmers stand on the shoulders of those that went before them and developed the tools that abstract away the things that programmers do on a regular basis. This hides the nitty-gritty of things like machine code, compiling, and garbage collection. More on this later.

* Great resources - There are tons of great resources (like this site hopefully, but also [this list](/blog/resources)) online now that help beginners understand the fundamentals and guide them towards the right topics to accomplish specific tasks. [Stack Overflow](https://stackoverflow.com/) is a great Q/A forum for programming, and will probably have the answers for most of the questions you will ever have the trick is learning the terminology to search for.

## Where to Start?

Start with a basic web-based project and build the whole thing from start to finish. This exercise will make you run into problems that you will need to solve. I will try to provide the fundamentals here at Port of Code, but inevitably, all developers end up spending a fair amount of time Googling things and debugging (aka figuring out why something doesn't work the way you thought it would).

> Most aspiring developers get hung up on all the different acronyms and tools and lose the forest for the trees. I suggest focusing on one thing at a time.

Websites all use the same basic technologies, HTML, CSS, and Javascript.

* HTML - or Hyper Text Markup Language is not a programming language per-say but a language for describing how a web page should look. Much like a skeletal system, it provides the structure.

* CSS - or Cascading Style Sheets is the styling of the webpage.

* Javascript - or JS or ECMAScript or ES6 (confusing, I know) is the logic that makes the site interactive; this is where things get interesting with webpages. Javascript can also be used to interact with a server behind the scenes (this is known as AJAX). There are a bunch of different frameworks written in Javascript to make building complex applications easier, but I suggest you start with learning plain old Javascript (also referred to as Vanilla Javascript) first, and then pick one framework and stick with it for a while.

> In the stone-age of the internet, websites were static documents that did not really do anything. Now, as Javascript has evolved over the years, we have full blown applications that *run in the browser*.

That running in the browser is part is key; Javascript code is read by and *interpreted* by the runtime environment within the browser which tells the computer what needs to happen. This is an example of *abstraction* that I was talking about earlier; the browser translates a more human readable code to something the computer knows what to do with.

## Front-ends, Backends, and Databases Oh My!

Web or cloud-based applications can be broken down into two main areas, front-end and back-end. The front-end covers the HTML/CSS/JS that runs within the client's browser, and the back-end is the server based application. Back-end is a lot more open-ended and can be written in a variety of different languages. For beginners I suggest either PHP, Ruby, or Python; all of which are easy to read and understand and have great tools to build web apps with the appropriate documentation and community support. These tools for building web apps are usually referred to as frameworks. The biggest one within Ruby is Rails (aka. Ruby-on-Rails). Rails is written in Ruby and provides a whole bunch of tools for generating code to save time, interacting with the database, and generating the front-end (Ruby will write out the HTML based on a template you create.). Python has a similar tool called Django, and PHP has Laravel.

One of the key functions for an app is persisting, or saving, data in a database. Databases require a connection to the app with a 'user' to make changes to the tables. You can kind of think of a database as a collection of Excel sheets, which in this case are called tables, with many columns per table. These columns represent each piece of data. Tables can be linked together with 'joins'. SQL is the language to know for database querying, and we'll talk more about that later.

These frameworks try and follow a structure that is common in web app development called MVC or Model, View, Controller.

> I have heard a good explanation of MVC as the view being the food that has been prepared by the cook (model) and served back to the customer by the waiter (controller) in a restaurant.

* Model - Models represent the different types of data in your application. This is also where the bulk of the logic in the application lies. If you have a login you'll most likely have a User object; this object will have some properties associated with it like name, email, and password. The User object may have some methods associated as well, methods are like functions the object can perform like updating the Users email or adding friends. The model should only interact with the Controller. This is also a very basic intro to Object Oriented Programming or OOP!

* View - This is what the user sees in their browser. Similar to a the things associated with a table in a restaurant. The view renders the templates that we talked about earlier. They do not have much logic to them at all because their main purpose is to display the data sent from the controller.

* Controller - The controller is charged with taking requests from the customer, relaying it to the kitchen (the model), retrieving the prepared order, and serving it to the customer's table. In essence, the controller manages data-flow in the application, and does the communicating between the view and the model. Controllers should be light, with little application logic within them.

> These abstract concepts are what trip up a lot of new developers, but the more you think about what is going on in an application the more it makes sense. Especially when you are building something and run into issues when your controllers have too much logic within them for example.

## Next steps

After you have built a simple application, find a something a little harder and go build that. Try building something different like a mobile application in [Expo.io](http://snack.expo.io) (which uses Javascript and the React framework.), try out a JS framework, or write a Ruby Gem. In all these steps, try and solve problems that you face yourself, because you will find that you're more willing to put in the effort and you stay interested longer.

## Resources

I will be posting a list of resources [here](/blog/resources).

Good luck and welcome to the world of programming!
