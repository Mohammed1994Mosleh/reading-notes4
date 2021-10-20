# class08 Reading Notes:


## Review: High-level HTTP:
![http structure](https://miro.medium.com/max/1838/1*i2tUjWy44-dYT9qsaWbvig.png)
1. Local Processing:
browser will generate scheme .
<protocol>://<host><:optional port>/<path/to/resource><?query>
and then browser find ip adrees by search on cache of recently requested urls

2. Resolve an IP:

- if cache fail to find ip then we can have ip by dns request,this process have many sequence.
- as request arrive dns server it will send response ,if not find one it will pass this request to another dns
- then the response will arrives ,it also have piece of information .

3. Establish a TCP Connection:
client have ip so can send http request over TCP 


4. Send an HTTP Request:
the request contains 
- request line
-  request header
-  request body

* The only mandatory field in an HTTP request is HOST, which contains the domain and port that the request is being sent to.

- Once the HTTP request is sent  using TCPs magic sequence number powers.

- As server receives the request,  find the resource being requested, it generates an HTTP response.

- send response at TCP layer and client receives the first packet data

4. Tearing Down and Cleaning Up:

- As response arrives client sends Fin packet through Tcp ,and server responed by ack.
-At this point, your browser begins processing what it has received. If it is an image, data, or other media file 

## Java HTTP Request example:
### 0HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries.

- this method is more  cumbersome than http libraries.

##### Creating a Request:

- openConnection() method of the URL class .

##### Adding Request Parameters:
- we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream .

##### Setting Request Headers:
- y using the setRequestProperty() method.

##### Configuring Timeouts:

- These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.

##### Handling Cookies:
- e.g CookieManager and HttpCookie

##### Handling Redirects:
- using the setInstanceFollowRedirects() method

##### Reading the Response:
- by using getResponseCode(), connect(), getInputStream() or getOutputStream() methods.


##### Reading the Response on Failed Requests:
-  by HttpUrlConnection.getErrorStream().

##### Building the Full Response:
- using the HttpUrlConnection instance.

