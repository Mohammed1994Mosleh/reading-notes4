# Spring:

## How to complete Spring?

![Spring flow](https://lh3.googleusercontent.com/proxy/8Txk4qeUGGMsHeLzguBTwD8-4Si0FCwoKHek8jatTWG5PB4UcZYqNcdBtS4q19lwpzPHMLPlhV9UA6LvQSZBPbJvqs-5wi6ArYgcY4rH_sjqnITenCg8uW6CkyPOJSZG6gIAetOlog)
1. Starting with Spring Initializr.
2. Create a Web Controller.
    * HTTP requests are handled by a controller

3. Spring Boot Devtools
   -Its handy moduls used to handle coding a change.
   -This tool have these characteristics:
      1. Enables hot swapping.
      2. Switches template engines to disable caching.
      3. Enables LiveReload to automatically refresh the browser.
      4. Other reasonable defaults based on development instead of production.

4. Run the Application:

    - @SpringBootApplication is a convenience annotation that adds all of the following:
      1. onfiguration
      2. EnableAutoConfiguration
      3. ComponentScan
      
    - SpringApplication.run() this method use in main to launch application.

5. Build an executable JAR:
   - To run application contains all the necessary dependencies, classes, and resources.

6. Test the Application:
   - make test by changing the query in request and you should notice the difference.

7. Add a Home Page :
   - Its the final step.


## pring MVC and Thymeleaf:

  - Their are many ways to adding model attributes to a view in Spring MVC.
     1. addAttribute method.
     2. return ModelAndView.
     3. Expose common attributes via methods in (ModelAttribute).

  - As messages attribute is added to the model ,so i can access through Thymeleaf views.
  
  -The attribute is accessed through ${attributeName}.

- Request parameters:
   e.g https://example.com/query?q=Thymeleaf+Is+Great!

    - Access reuest by : 
      1. param. prefix
      2. by using the special #request

  - Session attributes:
      
      * Access session attributes through session.prefix.
      * or direct access to the javax.servlet.http.HttpSession.

 - ServletContext attributes:
    * by using #servletContext. prefix may access to ervletContext attributes.

- Spring beans:
   - access registerd beans through @beanName syntax e.g("@urlService")