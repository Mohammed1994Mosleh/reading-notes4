# class16 Reading Notes:Trees

## Spring Security Architecture:

### Authentication and Access Control

![](https://www.baeldung.com/wp-content/uploads/2019/07/bael-1239-image-simple-1-1024x858.png)

  * authentication (who are you?) 
  * authorization (what are you allowed to do?)

#### authentication :

![](https://docs.spring.io/spring-security/site/docs/5.4.0-RC1/reference/html5/images/servlet/authentication/unpwd/daoauthenticationprovider.png)
     -  strategy interface for authentication is  AuthenticationManager

     public interface AuthenticationManager {

       Authentication authenticate(Authentication authentication)
       throws AuthenticationException;
   }

- Authenticate method returns:
   1. authenticated=true
   2. AuthenticationException
   3. null

- ProviderManager can support multiple different authentication mechanisms.

- A ProviderManager works like consultant if all return null.

- AuthenticationManagerBuilder is The most commonly used as helper

- use @Override of a method in the configurer for only to build a “local” AuthenticationManager


#### Authorization or Access Control:

![](https://docs.spring.io/spring-security/site/docs/5.2.11.RELEASE/reference/html/images/access-decision-voting.png)

- The core strategy  is AccessDecisionManager
- AccessDecisionVoter considers an Authentication (representing a principal) and a secure Object, which has been decorated with ConfigAttributes

#### Web Security:

![](https://www.baeldung.com/wp-content/uploads/2021/05/filters_vs_interceptors.jpg)

* Spring Security in the web tier based on  Servlet Filters

- based on the path of the request URI Container decides which filters and which servlet apply to it.

- FilterChainProxy is concrete type of spring security filter

- security filter is a @Bean is applied te every request

- FilterRegistrationBean.REQUEST_WRAPPER_FILTER_MAX_ORDER: the maximum order that a Spring Boot application expects filters to have if they wrap the request

- FilterChainProxy that contains all the security logic arranged internally as a chain (or chains) of filters 

#### Method Security:

* Spring Security offers support for applying access rules to Java method executions.

#### Working with Threads

- The basic building block is the SecurityContext, which may contain an Authentication.


