#### MSSA Cohort 3
#### Course: ISTA-322
#### Lesson Plan: 05
#### Name: Jason Bergener
#### Date: September 25, 2017

1. What elements does an HTML form contain?  
**An HTML form contains input elements like buttons, checkboxes, text inputs, and more.**
1. What attributes does the HTML form element take?  
**HTML form elements take an action attribute that tells the browser where to send the information to and a method attribute that tells the browser how to send the information.**
1. What does HTTP GET do? When is it used?  
**When a user submits a form using an HTTP GET request, the browser takes the input names and values inside the form and puts them in the query string. The default method value is “get,” so by default a form sends an HTTP GET request. GET represents an idempotent, read-only operation. You can send a GET request to a server repeatedly with no ill effects, because a GET does not (or should not) change state on the server.**
1. What does HTTP POST do? When is it used?  
**When a user submits a form using an HTTP POST request, the browser does not place the input values into the query string, but places them inside the body of the HTTP request instead. Although you can successfully send a POST request to a search engine and see the search results, an HTTP GET is preferable. Unlike the POST request, you can bookmark the GET request because all the parameters are in the URL. You can use the URLs as hyperlinks in an e-mail or a web page and preserve all the form input values. A POST, on the other hand, is the type of request you use to submit a credit card transaction, add an album to a shopping cart, or change a password. A POST request generally modifies state on the server, and repeating the request might produce undesirable effects (such as double billing). Many browsers help a user avoid repeating a POST request.**
1. How does an ASP.NET action method know what the query parameters are? How does it know what the parameter values are?  
**The MVC framework automatically finds this value in the query string, when the name of the parameter is present, and also finds the value in posted form values if you made your search form issue a POST instead of a GET.**
1. How does the dynamic calculation of the route path work in the HTML helper BeginForm?  
**The BeginForm HTML helper asks the routing engine how to reach the Search action of the HomeController. Behind the scenes it uses the method named GetVirtualPath on the Routes property exposed by RouteTable— that's where your web application registered all its routes in global.asax.**
1. What is HTML encoding? How does it work? Why is it necessary?  
**All the helpers that output model values will HTML encode the values before rendering. It works by converting your code into HTML. Encoding by default helps you to avoid cross-site scripting attacks (XSS).**
1. What is URL encoding? How does it work? Why is it necessary?  
**URL encoding replaces reserved characters in the URL with other characters (" " with %20, for example). This is necessary to prevent users from injecting malicious code.**
1. What is JavaScript encoding? How does it work? Why is it necessary?  
**JavaScript encoding encodes the JavaScript on the page to prevent malicious attacks.**
1. (Not in book) What is the JavaScript library jQuery? What does it contain, and why do we use it?  
**jQuery is a cross-platform JavaScript library designed to simplify the client-side scripting of HTML. It is free, open-source software using the permissive MIT License. Web analysis indicates that it is the most widely deployed JavaScript library by a large margin. jQuery's syntax is designed to make it easier to navigate a document, select DOM elements, create animations, handle events, and develop Ajax applications. jQuery also provides capabilities for developers to create plug-ins on top of the JavaScript library. This enables developers to create abstractions for low-level interaction and animation, advanced effects and high-level, themeable widgets. The modular approach to the jQuery library allows the creation of powerful dynamic web pages and Web applications.**
1. (Not in book) What is the JavaScript library jQueryUI ? What does it contain, and why do we use it?  
**jQuery UI is a collection of GUI widgets, animated visual effects, and themes implemented with jQuery (a JavaScript library), Cascading Style Sheets, and HTML. According to JavaScript analytics service, Libscore, jQuery UI is used on over 197,000 of the top one million websites, making it the second most popular JavaScript library. Notable users include Pinterest, PayPal, IMDb, The Huffington Post, and Netflix.**
1. (Not in book) What is the JavaScript library AngularJS ? What does it contain, and why do we use it?  
**AngularJS (commonly referred to as "Angular.js" or "AngularJS 1.X") is a JavaScript-based open-source front-end web application framework mainly maintained by Google and by a community of individuals and corporations to address many of the challenges encountered in developing single-page applications. The JavaScript components complement Apache Cordova, the framework used for developing cross-platform mobile apps. It aims to simplify both the development and the testing of such applications by providing a framework for client-side model–view–controller (MVC) and model–view–viewmodel (MVVM) architectures, along with components commonly used in rich Internet applications. The AngularJS framework works by first reading the HTML page, which has additional custom tag attributes embedded into it. Angular interprets those attributes as directives to bind input or output parts of the page to a model that is represented by standard JavaScript variables. The values of those JavaScript variables can be manually set within the code, or retrieved from static or dynamic JSON resources.**
<br/>

The information for the last three answers was obtained from en.wikipedia.org.