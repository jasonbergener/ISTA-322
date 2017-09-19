#### MSSA Cohort 3
#### Course: ISTA-322
#### Lesson Plan: 02
#### Name: Jason Bergener
#### Date: September 18, 2017

1. What is a controller? What does it do?  
**Controllers within the MVC pattern are responsible for responding to user input, often making changes to the model in response to user input. In this way, controllers in the MVC pattern are concerned with the flow of the application, working with data coming in, and providing data going out to the relevant view.**
1. Explain the relationship between URLs and controller methods.  
**Rather than having a direct relationship between the URL and a file living on the web server's hard drive, a relationship exists between the URL and a method on a controller class. The URL tells the routing mechanism which controller class to instantiate and which action method to call, and supplies the required arguments to that method. The controller's method then decides which view to use, and that view then renders the HTML.**
1. What does it mean to say that, "The web is stateless?"  
**With the Web, the state of the app for the user essentially vanishes and then is restored with every click.**
1. Where in the directory structure of an ASP.NET MVC application do controllers live?  
**The controllers can be found in the Controllers folder of the project.**
1. What programming constructs do controllers contain?  
**Controllers follow the basic class architecture and include methods also know as controller actions.**
1. Where are action methods? What do they do?  
**Action methods are the methods inside a controller. An action method's job is to respond to URL requests, perform the appropriate actions, and return a response back to the browser or user that invoked the URL.**
1. What are query parameters?  
**Query parameters are parameters passed via the URL.**
1. How do action methods receive HTTP query parameters?  
**The HTTP query parameters are passed in the URL as values assigned to named parameters. For example: if a method took a parameter of string type named "name" `public string Fun(string name)` then the URL that would pass the name would look like: `website/Fun?Name=Jason`.**