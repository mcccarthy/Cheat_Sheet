Here's your **HTTP Status Codes Cheat Sheet** formatted correctly in Markdown, structured similarly to the previous cheatsheets:

```markdown
# HTTP Status Codes Cheat Sheet

## Informational Responses (1xx)

- **100 Continue**: The server has received the request headers, and the client should proceed to send the request body.
- **101 Switching Protocols**: The server is switching protocols as requested by the client.

---

## Successful Responses (2xx)

- **200 OK**: The request has succeeded.
- **201 Created**: The request has been fulfilled, and a new resource has been created.
- **202 Accepted**: The request has been accepted for processing but not yet completed.
- **203 Non-Authoritative Information**: The request was successful, but the returned meta-information is not from the origin server.
- **204 No Content**: The server successfully processed the request and is not returning any content.
- **205 Reset Content**: The server successfully processed the request, and the client should reset the document view.
- **206 Partial Content**: The server is delivering only part of the resource due to a range header sent by the client.

---

## Redirection Messages (3xx)

- **300 Multiple Choices**: The request has more than one possible response.
- **301 Moved Permanently**: The requested resource has been permanently moved to a new URI.
- **302 Found**: The requested resource has been temporarily moved to a different URI.
- **303 See Other**: The response to the request can be found at a different URI using the GET method.
- **304 Not Modified**: The resource has not been modified since the last request.
- **305 Use Proxy**: The requested resource must be accessed through the proxy specified in the response.
- **307 Temporary Redirect**: The requested resource is temporarily located at a different URI.
- **308 Permanent Redirect**: The requested resource has been permanently moved to a new URI, and future requests should use the new URI.

---

## Client Error Responses (4xx)

- **400 Bad Request**: The server could not understand the request due to invalid syntax.
- **401 Unauthorized**: The client must authenticate itself to get the requested response.
- **402 Payment Required**: Reserved for future use, often related to digital payment systems.
- **403 Forbidden**: The client does not have access rights to the content.
- **404 Not Found**: The server can’t find the requested resource.
- **405 Method Not Allowed**: The request method is known by the server but is not supported for the targeted resource.
- **406 Not Acceptable**: The server cannot produce a response matching the list of acceptable values defined in the request's headers.
- **407 Proxy Authentication Required**: The client must first authenticate itself with the proxy.
- **408 Request Timeout**: The server timed out waiting for the request.
- **409 Conflict**: The request could not be completed due to a conflict with the current state of the resource.
- **410 Gone**: The requested resource is no longer available and will not be available again.
- **411 Length Required**: The server refuses to accept the request without a defined Content-Length header.
- **412 Precondition Failed**: The server does not meet one of the preconditions specified by the client.
- **413 Payload Too Large**: The request is larger than the server is willing or able to process.
- **414 URI Too Long**: The URI provided was too long for the server to process.
- **415 Unsupported Media Type**: The media type of the request data is not supported by the server.
- **416 Range Not Satisfiable**: The range specified by the Range header field in the request cannot be fulfilled.
- **417 Expectation Failed**: The server cannot meet the requirements of the Expect request-header field.

---

## Server Error Responses (5xx)

- **500 Internal Server Error**: The server has encountered a situation it doesn’t know how to handle.
- **501 Not Implemented**: The request method is not supported by the server and cannot be handled.
- **502 Bad Gateway**: The server, while acting as a gateway or proxy, received an invalid response from the upstream server.
- **503 Service Unavailable**: The server is not ready to handle the request, often due to maintenance or overload.
- **504 Gateway Timeout**: The server, while acting as a gateway or proxy, did not receive a timely response from the upstream server.
- **505 HTTP Version Not Supported**: The server does not support the HTTP protocol version that was used in the request.

---

This cheat sheet provides a quick reference for all standard HTTP status codes along with their explanations.
```

This format maintains a clean structure and clear headings for easy reference. Let me know if you need any more adjustments!
