# class19 Reading Notes:Using WebSocket to build an interactive web application

![WebSocket](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/using-websocket-to-build-real-time-application-via-asp-net-core/Images/arc.png)

#### What is WebSocket?

 - WebSocket is a thin, lightweight layer above TCP. This makes it suitable for using “subprotocols” to embed messages

### How to make web application an interactive  Using WebSocket to build ?

1. Insatll dependencies for websocket and stomp

* note: to use websocket you should install dependencies and we need to use STOMP protocol is a subprotocol operating on top of the lower-level WebSocket so we need to install dependency for it.

    - implementation 'org.webjars:sockjs-client:1.0.2'
    - implementation 'org.webjars:stomp-websocket:2.3.3'

2. Create a Resource Representation Class

   - after build your project you can create your STOMP message service.
   - The service will accept messages that contain a name in a STOMP message whose body is a JSON object.
   - crete class to make instances of messsage

3. Create a Message-handling Controller

   - In spring to work with stomp you need to route stomp message with controller
   - @MessageMapping annotation this used to check if the message send to its path destination .
   - @SendTo annotation this used to brodcast value to all users.

4. Configure Spring for STOMP messaging
    
  - Create class to configure Spring to enable WebSocket and STOMP messaging.
  - @Configuration to indicate that it is a Spring configuration, @EnableWebSocketMessageBroker enables WebSocket   message handling
  
5. Create a Browser Client

  - Create an index.html
  - This HTML file imports the SockJS and STOMP javascript libraries that will be used to communicate with our server through STOMP over websocket.
  -  connect() function uses SockJS and stomp.js to open a connection with socket
  - When connect is success it will match /topic/greetings destenation and puplish message.
  - sendName() function retrieves the name entered by the user and uses the STOMP client to send it to the /app/hello destination

6. Make the Application Executable

   - @SpringBootApplication Adds the following annotation
     1. @Configuration
     2. @EnableAutoConfiguration
     3. @ComponentScan

7. Build an executable JAR

   - You can build jar file contains all dependencies ,classes an resources and run it.
   - So the application makes it easy to ship ,version ,and deploy an application 
   - to run application you can use ./gradlew bootRun.

8. Test the service

   - Now check your application through  http://localhost:8080