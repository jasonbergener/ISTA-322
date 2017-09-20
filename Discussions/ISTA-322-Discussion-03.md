#### MSSA Cohort 3
#### Course: ISTA-322
#### Lesson Plan: 03
#### Name: Jason Bergener
#### Date: September 19, 2017

1. What is a view?  
**The view is effectively your application's ambassador to the user. The view is responsible for providing the user interface (UI) to the user. After the controller has executed the appropriate logic for the requested URL, it delegates the display to the view. Unlike file-based web frameworks, such as ASP.NET Web Forms and PHP, views are not themselves directly accessible. You can't point your browser to a view and have it render. Instead, a view is always rendered by a controller, which provides the data the view will render.**
1. What is the similarity between view names and controller names? What is the difference between the two?  
**View names correspond to the method names in a controller, and are stored in a folder that shares the base name of the controller. The root view for each controller is usually the index.cshtml. Controller base names are a theme, like home or store, and they are always combined with the word "Controller". Using the same examples, the controller names would be HomeController and StoreController.**
1. Where in the directory structure of an ASP.NET MVC application do
views live?  
**Views can be found in the Views folder. Each view is further organized into subfolders based on their controller.**
1. What is a ViewBag object? What does it do?  
**All data is passed from the controllers to the views via a ViewDataDictionary (a specialized dictionary class) called ViewData. The ViewBag leverages the dynamic keyword to create a dynamic wrapper around ViewData. ViewBag is just syntactic sugar that some people prefer over the dictionary syntax. It just looks nicer.**
1. What does the at symbol (@) do? Can you escape it? If so, how?  
**The key transition character in Razor is the “at” sign (@). This single character is used to transition from markup to code and sometimes also to transition back. The two basic types of transitions are code expressions and code blocks. Expressions are evaluated and written to the response. You can escape it by using it twice consecutively like @@. You can also use the HTML coding for @ (&#64;) instead.**
1. What are view conventions and how do they work?  
**Each controller folder contains a view file for each action method, and the file is named the same as the action method. This provides the basis for how views are associated to an action method.
The view selection logic looks for a view with the same name as the action within the /Views/ControllerName directory (the controller name without the Controller suffix in this case). The view selected in this case would be /Views/Home/Index.cshtml.
As with most things in ASP.NET MVC, you can override this convention.**
1. What is an ActionResult object? How do these objects interact with views?  
**An ActionResult object is an instance of the ActionResult class. They contain the information that the view converts into HTML to send to the browser.**
1. What are strongly typed views?  
**Strongly typed views allow you to set a model type for a view. This allows you to pass a model object from the controller to the view that's strongly typed on both ends, so you get the benefit of IntelliSense, compiler checking, and so on. Strongly typed views return an object of a specific type that the view knows how to handle.**
1. How does Razor combine HTML and C# code?  
**Razor allows you to insert C# code into HTML using the @ sign. It effectively converts the code to HTML before it is passed to the browser.**
1. Where do layouts live in the directory structure of an ASP.NET MVC  application?  
**Layouts can be found in the Shared subfolder of the Views folder.**
1. What are the differences between a partial view and a "full view?"  
**The partial view itself looks much like a normal view, except it doesn't specify a layout; if the layout is specified by a _ViewStart.cshtml page (and not directly within the view), the layout is not rendered.**