# class13 Reading Notes:

## Working with Relationships in Spring Data REST:

![](https://res.infoq.com/articles/spring-data-intro/en/resources/spring_data_overview_small.jpg)


- In order to make relationship i should have these things:
   1. The Data Model.
   2. The Repositories.
   3.  Creating the Associations:
   4. One-to-Many Relationship.

### One-to-One Relationship:
![](https://www.baeldung.com/wp-content/uploads/2018/12/1-1_FK.png)
   - public interface LibraryRepository extends CrudRepository<Library, Long> {}
1.  The Data Model

2. The Repositories.

3..  Creating the Associations:
    - This is done using the HTTP method PUT.

3.. One-to-Many Relationship.
   - defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.


### One-to-many Relationship:
![](https://www.baeldung.com/wp-content/uploads/2017/02/C-1.png)
   - defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.

1. The Data Model:
 
2. The Repository

3. The Association Resources

###  Many-to-Many Relationship:
![](https://1.bp.blogspot.com/-KSOtp0ncuCE/XUl_W_CgInI/AAAAAAAAGlY/azmqBxYiSFIOhLEF3ZL4amuOnM4Z_SgcACLcBGAs/s1600/many-to-many-ERD.png)
- defined using @ManyToMany annotation, to which we can add @RestResource.

1. The Data Model

2. The Repository.

3. The Association Resources.

   - must first create the resources before we can establish the association.

## Integration Testing in Spring:

## Spring MVC Test Configuration:

### Enable Spring in Tests with JUnit 5:
    - enable this extension by adding the @ExtendWith annotation to our test classes.
  
1. The WebApplicationContext Object:
    - provides a web application configuration. It loads all the application beans and controllers into the context.

2. Mocking Web Context Beans:
   - support for Spring MVC testing. It encapsulates all web application beans and makes them available for testing.

3. Verify Test Configuration

###  Writing Integration Tests

1. Verify View Name
   - http://localhost:8080/spring-mvc-test/

2. Verify Response Body

- MockMvcResultMatchers.status().isOk()) will verify that response HTTP status is Ok (200).this means connection successfully.

3. Send GET Request With Path Variable

   - http://localhost:8080/spring-mvc-test/greetWithPathVariable/John

4. Send GET Request With Query Parameters.
    e.g http://localhost:8080/spring-mvc-test/greetWithQueryVariable?name=John%20Doe

5. Send POST Request:

    - e.g http://localhost:8080/spring-mvc-test/greetWithPost

### MockMvc Limitations:

- The MockMvc class wraps this TestDispatcherServlet internally, so their is no real connection
