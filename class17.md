# class17 Reading Notes:Spring Boot and OAuth2

### Single Sign On With GitHub:

![](https://miro.medium.com/max/902/1*fZJ9clGrT_dX8nmvZAkhXQ.png)

1. Creating a New Project

2. Add a Home Page
   - Create index.html in the src/main/resources/static folder

3. Securing the Application with GitHub and Spring Security
   - For more secure,add Spring Security as a dependency.
   - Configure your app by github as  authentication provider

4. Add a New GitHub App
   - Make New OAuth App
   -  The Authorization callback URL as http://localhost:8080/login/oauth2/code/github
   - {baseUrl}/login/oauth2/code/{registrationId} is The default redirect url.

5. Boot Up the Application

* The above steps make a Client application available using  authorization code gran obtaininng access token from    (the Authorization Server).

6. Add a Welcome Page:

* Adding explicit link to login with GitHub. Instead of being redirected immediately

   - Conditional Content on the Home Page
      -  you have the option of either server-side or client-side rendering ,to render content on conditional       Authorization.

    - The /user Endpoint
       -  It will send back the currently logged-in user.
    
    - Making the Home Page Public
       - WebSecurityConfigurerAdapter used to switch off the security on the home page .

7. Add a Logout Button

   - Client Side Changes
   - Adding a Logout Endpoint
      * /logout built in support endpoint which will do the right thing for us like clear cookie.

   - Adding the CSRF Token in the Client

8. Login with GitHub
   
   - Initial setup :
      Set up a project in the Google API Console to obtain OAuth 2.0 credentials
   - Setting the redirect URI
   - Adding the Client Registration
      Because Spring Security is built with multiple clients in mind ,you need to configure the client to point Google.

   - Adding the Login Link.

9. Add a Local User Database.
  
   - Choose a backend for your database.
   - Implement and expose OAuth2UserService to call the Authorization Server as well as your database.

10. Adding an Error Page for Unauthenticated Users

   - Switching to GitHub
   - Detecting an Authentication Failure in the Client.
   - Adding an Error Message
       when authentication fails configure an AuthenticationFailureHandler

    - Generating a 401 in the Server



