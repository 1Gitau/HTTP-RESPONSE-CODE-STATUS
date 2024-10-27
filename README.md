## http response status code

- HTTP response status codes indicate whether a specific HTTP request has been successfully completed.


 We have five groups of HTTP response status code which are summarized below;

 # Informational responses

 This interim response indicates that the client should continue the request or ignore the response if the request is already finished.
 

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


 <h2 style="color:yellowgreen">308 Permanent Redirect</h2> 
 

 - This means that the resource is now permanently located at another URI, specified by the Location response header


# Client error responses



 ### <ins> Types of Client error responses</ins>

 <h2 style="color:yellowgreen">400 Bad Request</h2> 

 - Indicates that the server would not process the request due to something the server considered to be a client error. The reason for a 400 response is typically due to malformed request syntax, invalid request message framing, or deceptive request routing.

 <h2 style="color:yellowgreen">401 Unauthorized</h2> 

 - Indicates that a request was not successful because it lacks valid authentication credentials for the requested resource.

 <h2 style="color:yellowgreen">402 Payment Required</h2>

 -  is a nonstandard response status code reserved for future use. 

  <h2 style="color:yellowgreen">403 Forbidden</h2>

  - Indicates that the server understood the request but refused to process it.

  
  <h2 style="color:yellowgreen">404 Not Found</h2>

  - The code indicates that the server cannot find the requested resource.


<h2 style="color:yellowgreen">405 Method Not Allowed</h2>



- The code indicates that the server knows the request method, but the target resource doesn't support this method.

<h2 style="color:yellowgreen">406 Not Acceptable</h2>

- Indicates that the server could not produce a response matching the list of acceptable values defined in the request's proactive content negotiation headers and that the server was unwilling to supply a default representation.

<h2 style="color:yellowgreen">407 Proxy Authentication Required</h2>

- Indicates that the request did not succeed because it lacks valid authentication credentials for the proxy server that sits between the client and the server with access to the requested resource.

<h2 style="color:yellowgreen">408 Request Timeout</h2>

- The code indicates that the server would like to shut down this unused connection.

<h2 style="color:yellowgreen">409 Conflict</h2>

- Indicates a request conflict with the current state of the target resource.

<h2 style="color:yellowgreen"> 410 Gone</h2>

- Indicates that the target resource is no longer available at the origin server and that this condition is likely to be permanent.

<h2 style="color:yellowgreen">411 Length Required</h2>

- The status code indicates that the server refused to accept the request without a defined Content-Length header.

<h2 style="color:yellowgreen">412 Precondition Failed</h2>

- Indicates that access to the target resource was denied

<h2 style="color:yellowgreen">413 Content Too Large</h2>

- Indicates that the request entity was larger than limits defined by server. 

<h2 style="color:yellowgreen">414 URI Too Long</h2>

- Indicates that a URI requested by the client was longer than the server is willing to interpret.

<h2 style="color:yellowgreen">415 Unsupported Media Type</h2>

- The code indicates that the server refused to accept the request because the message content format is not supported.

<h2 style="color:yellowgreen">416 Range Not Satisfiable</h2>

- The ndicates that a server could not serve the requested ranges

<h2 style="color:yellowgreen">417 Expectation Failed</h2>

- The  status code indicates that the expectation given in the request's Expect header could not be met.

<h2 style="color:yellowgreen">418 I'm a teapot</h2>

- Indicates that the server refuses to brew coffee because it is, permanently, a teapot.

<h2 style="color:yellowgreen">421 Misdirected Request</h2>

- Indicates that the request was directed to a server that is not able to produce a response.

<h2 style="color:yellowgreen">422 Unprocessable Content</h2>

- Indicates that the server understood the content type of the request content, and the syntax of the request content was correct, but it was unable to process the contained instructions

<h2 style="color:yellowgreen">423 Locked</h2>

- Indicates that a resource is locked, meaning it can't be accessed. 


<h2 style="color:yellowgreen">424 Failed Dependency</h2>

- Indicates that the method could not be performed on the resource because the requested action depended on another action, and that action failed.

<h2 style="color:yellowgreen">425 Too Early</h2>

- Indicates that the server was unwilling to risk processing a request that might be replayed to avoid potential replay attacks.

<h2 style="color:yellowgreen">426 Upgrade Required</h2>

- The code indicates that the server refused to perform the request using the current protocol but might be willing to do so after the client upgrades to a different protocol.


<h2 style="color:yellowgreen">428 Precondition Required</h2>

- Indicates that the server requires the request to be conditional.

<h2 style="color:yellowgreen">429 Too Many Requests</h2>

- Indicates the client has sent too many requests in a given amount of time.


<h2 style="color:yellowgreen">431 Request Header Fields Too Large</h2>

- The code indicates that the server refuses to process the request because the request's HTTP headers are too long.

<h2 style="color:yellowgreen">451 Unavailable For Legal Reasons</h2>

- The code indicates that the user requested a resource that is not available due to legal reasons, such as a web page for which a legal action has been issued.


# Server error responses

They  indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.



 ### <ins> Types of Server error responses</ins>

 <h2 style="color:yellowgreen">500 Internal Server Error
</h2>

- indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.

 <h2 style="color:yellowgreen">501 Not Implemented
</h2>

- The code means that the server does not support the functionality required to fulfill the request.


 <h2 style="color:yellowgreen">502 Bad Gateway
</h2>

- The code indicates that a server was acting as a gateway or proxy and that it received an invalid response from the upstream server.

<h2 style="color:yellowgreen">503 Service Unavailable
</h2>

- The status code indicates that the server is not ready to handle the request.

<h2 style="color:yellowgreen">504 Gateway Timeout
</h2>

- Indicates that the server, while acting as a gateway or proxy, did not get a response in time from the upstream server in order to complete the request.

<h2 style="color:yellowgreen">505 HTTP Version Not Supported
</h2>

- The status code indicates that the HTTP version used in the request is not supported by the server.

<h2 style="color:yellowgreen">506 Variant Also Negotiates
</h2>

- The ode is returned during content negotiation when there is recursive loop in the process of selecting a resource.


<h2 style="color:yellowgreen">507 Insufficient Storage
</h2>


- The status code indicates that an action could not be performed because the server does not have enough available storage to successfully complete the request.

<h2 style="color:yellowgreen">508 Loop Detected
</h2>

- status code indicates that the entire operation failed because it encountered an infinite loop while processing a request with Depth: infinity.


<h2 style="color:yellowgreen">510 Not Extended
</h2>

- status code is sent when the client request declares an HTTP Extension (RFC 2774) that should be used to process the request, but the extension is not supported.

<h2 style="color:yellowgreen">511 Network Authentication Required
</h2>

- The code indicates that the client needs to authenticate to gain network access.