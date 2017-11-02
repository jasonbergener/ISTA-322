#### MSSA Cohort 3
#### Course: ISTA-322
#### Chapter: 08
#### Name: Jason Bergener
#### Date: October 25, 2017

1. Examine the following code. Then explain what this code does, line by line.
    ```aspnet
    $(function () {
      $("#album-list img").mouseover(function () {
        $(this).animate({ height: '+=25', width: '+=25' }).animate({ height: '-=25', width: '-=25' });
      });
    });
    ```  
    **The `$` is the alias for a jQuery function. The parameter passed to the jQuery function is an anonamous function that takes no parameters. The body of the anonamous function calls a jQuery function and passes it a selector. This specific selector tells jQuery to find all the images inside the element with an id value of album-list. When the selector executes, it returns a wrapped set of zero or more matching elements. Any additional jQuery methods you invoke will operate against all the elements in the wrapped set. For example, the `mouseover` method hooks an event handler to the `onmouseover` event of each image element that matched the selector. In the body of the `mouseover` method, the code animates an element during the mouseover event. The element the code animates is referenced by the this keyword (this points to the element where the event occurred). Notice how the code first passes the element to the jQuery function ($(this)). jQuery sees the argument as a reference to an element and returns a wrapped set with the element inside. After you have the element wrapped inside of jQuery goodness, you can invoke jQuery methods such as animate to manipulate the element. The code in the example makes the image grow a bit (increase the width and height by 25 pixels), and then shrink a bit (decrease the width and height by 25 pixels). The result of the code is as follows: When users move their mouse over an album image, they see a subtle emphasizing effect when the image expands, then contracts.**
1. Write the jQuery code that selects all the hyperlinks in the menu block level element \<div> that are descendants of the menu division. Write the jQuery code that selects all the hyperlinks in the menu block level element \<div> that are children of the menu division. What is the difference between the two?  
**This selects all \<div> elements that are descendants of the element with an id of “menu" : `$("#menu div")`. This selects all \<div> elements that are children of the element with an id of “menu" : `$("#menu > div")`. The difference is that children are one level below; they are the direct descendants. Descendants can be children of children of children and so on.**
1. Describe the Document Object Model (DOM).  
**The document object model is the collection of all the html, css, and scripts on a page once it has finished loading. Unlike traditional static pages that needed to be completely reloaded whenever a change occurred, individual sections of the DOM can be modified and refreshed without having to reload the entire page.**
1. How do you write Unobtrusive JavaScript? Describe the process.  
**Unobtrusive JavaScript is simply keeping your JavaScript separate from your HTML. You do that by packaging all the script code you need into .js files and then referencing those in the markup.**
1. How do you add a script reference to a web application in ASP.NET? How do you add a script bundle to a web application in ASP.NET? What is the difference between the two?  
**Instead of emitting JavaScript code into a view to enable features such as client-side validation, the framework sprinkles metadata into HTML attributes. Using jQuery, the framework can find and interpret the metadata, and then attach behaviors to elements, all using external script files.**
1. I you to write your own custom JavaScript, where in the application directory structure might you place it?  
**You would put it in the Scripts folder.**
1. What is the main purpose of using AJAX in web applications? Explain why you would want to do so.  
**Technically, Ajax stands for asynchronous JavaScript and XML. In practice, Ajax stands for all the techniques you use to build responsive web applications with a great user experience. Being responsive does require some asynchronous communication now and then, but the appearance of responsiveness can also come from subtle animations and color changes. If you can visually encourage your users to make the right choices inside your application, they'll love you and come back for more.**
1. What are data dash attributes? Why do we use them? Do web browsers render them? Why or why not?  
**Data dash attributes are attributes that have a prefix of "data-". The HTML 5 specification reserves data dash attributes for private application state. In other words, a web browser does not try to interpret the content of a data dash attribute, so you are free to put your own data inside and the data does not influence the display or rendering of a page. Data dash attributes even work in browsers released before an HTML 5 specification existed. Internet Explorer 6, for example, ignores any attributes it doesn't understand, so data dash attributes are safe in older versions of IE.**
1. How do you activate client side jQuery validation? How do you activate server side validation with ASP.NET?  
**The jQuery Validation plugin (jquery.validate) exists in the Scripts folder of a new MVC 5 application by default. If you want client-side validation, you'll need a reference to the jqueryval bundle to the applicable views. The model binder in ASP.NET MVC performs server-side validation against properties when it sets their values.**
1. You have an 11 character product model code that consists of four upper case alphabetical characters, four digits, and three upper case alphabetical characters. As example would be ABCD4567XYZ. Write a custom validation method to validate user input as to your model code.  
**[A-Z]{4}[0-9]{3}[A-Z]{3}.**