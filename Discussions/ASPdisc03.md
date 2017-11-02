#### MSSA Cohort 3
#### Course: ISTA-322
#### Chapter: 09
#### Name: Jason Bergener
#### Date: November 8, 2017

1. In a nutshell, what is Chapter 9 about? A one word answer "routing" is not a sufficient answer. Explain what routing is, what it does, and its role in ASP.NET MVC.  
**Chapter nine is about how requests are disassembled by MVC and the pieces are use to process the request.**
1. What is the difference (as described in the book) between traditional web applications and applications built with MVC frameworks?  
**Traditional web applications were invoked when they received a request whereas MVC frameworks are running and the request is handled by a controller that invokes a method.**
1. What two approaches to routing does ASP.NET take? Explain the difference between them.  
**The two approaches to routing are traditional routing and attribute routing.**
1. What are the two locations for the placement of attribute routes?  
**Attribute routes can be placed inside the attributes of the action methods or they can be placed in the attributes of the controller.**
1. Where is the RegisterRoutes method defined? What is its type and parameters? What is its visibility and scope?  
**The RegisterRoutes method is defined in the RouteConfig.cs file inside the the App_Start folder. The type is void, it takes one parameter (route collection), its visibility is public, and its scope is class.**
1. At its core, what is the job of a route?  
**The job of a route is to direct the traffic.**
1. How do you code dynamic behavior into routes? Be specific.  
**You add a route parameter by enclosing them in curly braces.**
1. What are route constraints? Be specific. Give an example of the usage of a constraint and include the program code for the constraint.  
**Route constraints are conditional statements that allow requirements to be specified for routes. For example, to constrain a parameter to a specific type like ensuring that the parameter `{id}` is an integer, you would use a colon and the type like: `{id:int}`.**
1. What are route defaults? Be specific. Give an example of the usage of a constraint and include the program code for the constraint.  
**In `[Route("home/{action=Index}")]` the `{action=Index}` snippet defines a default value for the {action} parameter. This default allows this route to match requests when the action parameter is missing. In other words, this route now matches any URL with one or two segments instead of matching only two-segment URLs.**
1. What are optional route patterns? Be specific. Give an example of the usage of a constraint and include the program code for the constraint.  
**In `[Route("{action=Index}/{id?}")]` the ? makes the id parameter optional.**
1. Where is the central location for placement of traditional routes?  
**Traditional routes are found in the RegisterRoutes method in the RouteConfig.cs file inside the the App_Start folder.**
1. What purpose do literal values serve in specifying routes?  
**Literals have to be matched exactly and are not up to interpretation.**
1. In traditional routing, how do you specify that a route parameter is optional. Be specific - include the name of the variable or method.  
**You call a new constructor and pass it the name of the parameter and invoke.**
1. (Not in the book) Write a regular expression that would recognize all of these dates as a valid route parameter: 2017/10/31, 17/10/31, 2017/OCT/31, 17/Oct/31, and 17/October/31.  
**[0-9]{2,4}/([0-9]{1,2}|{^oct}i)/[0-9]{1,2}.**
1. How do you combine traditional routing and attribute routing?  
**You combine them by stacking them. It is important to put the attribute routing above the traditional routing.**
1. How do you dynamically generate a hyperlink from within a view using named routes?  
**Given the named route:**
    ```aspnet
    routes.MapRoute(
           name: "Test",
           url: "code/p/{action}/{id}",
           defaults: new { controller = "Section", action = "Index", id = "" }
    ```
    **to generate a hyperlink to each route from within a view, you write the following code:**
    ```aspnet
    @Html.RouteLink("to Test", new {controller="section", action="Index", id=123})
    ```
1. How would you create a web application more than two layers deep? Note that the controller/action syntax only permits two layers of the application. Suppose you wanted four layers, such as (for example) Catalog/Books/Technology/Microsoft/id?.  
**Divide your application into areas.**
1. What is the difference between the way that traditional routing and attribute routing handle multiple route parameters in a segment?
**One is greedy and the other is lazy.**