# Read: 13 - CRUD - 5/1/2021

## Status code

- 100's = informational status codes
- 200's = success codes
- 300's = redirection codes
- 400's = client error codes
- 500's = server error codes

## CRUD

1. CREATE

- 200 OK
- 201 Created
- 202 Accted
- 303 See Other

2. READ

- 200 OK
- 206 Partial Content
- 300 Multiple Choices
- 308 Perpanent Redirect
- 304 Not Modified
- 307 Temporary Redirect

3. UPDATE  
   An update can be implemented with HTTP `PUT` or `PATCH` method. The difference lies in the amound of data the client has to send to the backend. `PUT` requires the client to send an entire representation of a resource to update it. (Replace the old one with the new one). `PATCH` requires the client only send parts of the representation of the resrouce to update it. (Add, update or delete these parts in the old version)

- 200 OK
- 204 No Content
- 202 Accepted

4. DELETE

- 200 OK
- 204 No Content
- 202 Accepted

5. Errors  
   Wrong URL

- 404 Not Found
- 405 Method Not Allowed
- 501 Not Implemented
- 406 Not Acceptable
- 410 Gone
- 414 Request-URL Too Long
- 308 Permanent Redirect
- 307 Temporary Redirect

No Permissions

- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
