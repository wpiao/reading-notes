# Read: 07 - REST - 4/10/2021   

## REST - REpresentational State Transfer   
REST is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. RESTful systems are characterized by how they are stateless and seperate the concerns of client and server.    


## Seperation of Client and Server    
In the REST archetectural style, the implementation of the client and the implementation of the server can be done independently without each knowing about the other. So code on the client side can be changed at any time without affecting the operation of the server, and vise versa. By using a REST interface, different clients hit the same REST endpoints, perform the same actions, and receive the same responses.   

## Statelessness    
Systems that follow the REST paradigm are stateless, meaning that the server does not need to know anything about what state the client is in and vice versa.   

## Making Requests    
  - an HTTP verb, which defines what kind of operation to perform   
  - a header, which allows the client to pass along information about the request   
  - a path to a resource    
  - an optional message body containing data    

## HTTP Verbs   
  - GET - retrieve a specific resource (by id) or a collection resources    
  - POST - create a new resource    
  - PUT - update a specific resource (by id)    
  - DELETE - remove a specific resource by id   
