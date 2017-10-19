#### MSSA Cohort 3
#### Course: ISTA-322
#### Chapter: 07
#### Name: Jason Bergener
#### Date: October 18, 2017

1. What is the difference between authentication and authorization?  
**Authentication is identity verification. Authorization is user privileges. We authenticate a user by verifying their credentials. Once they have been authenticated, they are only able to access resources they have been authorized for.**
1. What three conditions does the OnAuthorization method check?  
**The OnAuthorization method is defined by the programmer and can check whatever you want it to. The book example shows the code checking to see if a user is authenticated, if the user exists in the list of authorized users, and if the user is assigned a role.**
1. How do you register the AuthorizeAttribute as a global filter?  
**To register the AuthorizeAttribute as a global filter, add it to the global filters collection in the RegisterGlobalFilters method, located in \App_Start\FilterConfig.cs.**
1. How do you activate the authorization filter in ASP.NET MVC 5?  
**.**
1. What is the difference between OAUTH and OPENID? Explain.  
**Sites that use an OAuth provider (Facebook, Twitter, and Microsoft) require you to register your site as an application. When you do, you'll be provided a client id and a secret. Your site uses these to authenticate with the OAuth provider. Sites that implement OpenID (such as Google and Yahoo!) do not require you to register an application, and you won't need a client id or secret.**
1. How are authorization providers configured?  
**The example code to implement Google provider support is already included in Startup.Auth.cs, so just uncomment it. Although the code involved in configuring an OAuth provider is very similar to the OpenID case, the process of registering your site as an application varies by provider. The MVC 5 project template (when using Individual Account for authentication) includes support for three specific OAuth providers (Microsoft, Facebook, and Twitter) as well as a generic OAuth implementation.**
1. How do you prevent user log in information from being intercepted during log in?  
**You use `[RequireHttps]` to enforce HTTPS on the callback.**
1. How do you carry out an attack by XSS?  
**XSS can be carried out in one of two ways: by a user entering nasty script commands into a website that accepts unsanitized user input or by user input being directly displayed on a page. The first example is called passive injection—whereby a user enters nastiness into a textbox, for example, and that script gets saved into a database and redisplayed later. The second is called active injection and involves a user entering nastiness into an input, which is immediately displayed onscreen.**
1. How do you carry out an attack by XSRF?  
**In a nutshell, you convince a user to log into a legitimate site like their bank, and then exploit the session cookie by running a XSS script that redirects to their bank's site with them as an authenticated user.**
1. How do you carry out an attack by cookie stealing?  
**You use XSS to run a script on the victim's browser that sends their cookies to a remote server. You then use the stolen cookies to impersonate them on the web and have their authorization.**
1. How do you carry out an attack by over posting?  
**Over posting takes advantage of model binding by adding values to properties that were not intended to be submitted on the form.**
1. How do you carry out an attack by open redirection?  
**You append a legitimate URL with a `ReturnUrl=` that redirects to a cloned site. Once at the cloned site, you trick the user into re-entering their credentials, which you save for later, and then redirect them back to the legitimate site that gives them access because they logged in successfully the first time..**