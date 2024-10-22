## http response status code

- HTTP response status codes indicate whether a specific HTTP request has been successfully completed.


 We have five groups of HTTP response status code which are summarized below;

 # Informational responses
 description

 ### <ins> Types of infomation responses</ins>

 <h2 style="color:yellowgreen">100 Continue</h2> 

 - It shouws that the client should continue the request or ignore the response if the request is already finished.

  <h2 style="color:yellowgreen">101 Switching Protocols</h2>

  -  Indicates the protocol that a server has switched to. 
 
  <h2 style="color:yellowgreen">102 Processing Deprecated</h2>

  - Indicates to client that a full request has been received and the server is working on it. This status code is only sent if the server expects the request to take significant time.

   <h2 style="color:yellowgreen">103 Early Hints</h2>

   - May be sent by a server while it is still preparing a response, with hints about the sites and resources that the server expects the final response will link to.
   

 # Successful responses

Its confirmation used by Distributed Search to indicate that a message has been received and processed successfully.

 ### <ins> Types of Successful  responses</ins>


 <h2 style="color:yellowgreen">200 OK</h2>

- Response has a different meaning and format depending on the HTTP request method. Here's how they vary for different methods:

  - GET: A resource was retrieved by the server and included in the response body.

  - POST: An action succeeded; the response has a message body describing the result.
  
  - HEAD: Identical to GET, except there is no message body.
  - TRACE: The response has a message body containing the request as received by the server.

  <h2 style="color:yellowgreen">201 Created</h2>

- Indicates that the HTTP request has led to the creation of a resource.

 <h2 style="color:yellowgreen">202 Accepted</h2>

 - Indicates that a request has been accepted for processing, but processing has not been completed or may not have started.

<h2 style="color:yellowgreen">203 Non-Authoritative Information</h2>

- Indicates that the request was successful, but a transforming proxy has modified the headers or enclosed content from the origin server's 200 (OK) response.


<h2 style="color:yellowgreen">204 No Content</h2>

- Indicates that a request has succeeded, but the client doesn't need to navigate away from its current page.

 - A 204 No Content in response to these request methods has the following meaning and results:

     - DELETE: The action was successful, and no further information needs to be supplied.

     - PUT: The action was successful, and the ETag value contains the entity tag for the new representation of that target resource.

     <h2 style="color:yellowgreen">205 Reset Content</h2>

-Indicates that the request has been successfully processed and the client should reset the document view.


  <h2 style="color:yellowgreen">206 Partial Content</h2>

  -  It is sent in response to a range request. The response body contains the requested ranges of data as specified in the Range header of the request.

<h2 style="color:yellowgreen">207 Multi-Status (WebDAV)</h2>

- Indicates a mixture of responses. This response is used exclusively in the context of Web Distributed Authoring and Versioning (WebDAV).


<h2 style="color:yellowgreen">208 Already Reported (WebDAV)</h2>

- It  is used in a 207 Multi-Status response to save space and avoid conflicts. This response is used exclusively in the context of Web Distributed Authoring and Versioning

<h2 style="color:yellowgreen">226 IM Used (HTTP Delta encoding)</h2>

- Indicates that the server is returning a delta in response to a GET request. It is used in the context of HTTP delta encodings.

# Redirection messages

These codes indicate that further action must be taken by the client to complete the request.

 ### <ins> Types of Redirection messages</ins>

<h2 style="color:yellowgreen">300 Multiple Choices</h2>

- In agent-driven content negotiation, the request has more than one possible response and the user agent or user should choose one of them. There is no standardized way for clients to automatically choose one of the responses, so this is rarely used.

<h2 style="color:yellowgreen">301 Moved Permanently</h2>

- Indicates that the requested resource has been permanently moved to the URL in the Location header.


<h2 style="color:yellowgreen">302 Found</h2>

- Indicates that the requested resource has been temporarily moved to the URL in the Location header.

<h2 style="color:yellowgreen">303 See Other</h2>

- ndicates that the browser should redirect to the URL in the Location header instead of rendering the requested resource.

- This response code is often sent back as a result of PUT or POST methods so the client may retrieve a confirmation, or view a representation of a real-world object.

<h2 style="color:yellowgreen">304 Not Modified</h2>

- Indicates that there is no need to retransmit the requested resources.

<h2 style="color:yellowgreen">305 Use Proxy Deprecated</h2>

- indicate that a requested response must be accessed by a proxy. It has been deprecated due to security concerns regarding in-band configuration of a proxy.

 <h2 style="color:yellowgreen">306 unused</h2>

 - This response code is no longer used; but is reserved. It was used in a previous version of the HTTP/1.1 specification.

 
 <h2 style="color:yellowgreen">307 Temporary Redirect</h2> 
 
 - Response to direct the client to get the requested resource at another URI with the same method that was used in the prior request.

- This has the same semantics as the 302 Found response code, with the exception that the user agent must not change the HTTP method used: if a POST was used in the first request, a POST must be used in the redirected request.


 <h2 style="color:yellowgreen"></h2> 
 
