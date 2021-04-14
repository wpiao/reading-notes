# Read: 08 - APIs - 4/13/2021   

## HTTP methods   
  - `GET` retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.   
  - `POST` creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.   
  - `PUT` either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.    
  - `PATCH` performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.    
  - `DELETE` removes the resource at the specified URI.   

## Representational State Transfer (REST)   
  - REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.   
  - A resource has an identifier, which is a URI that uniquely identifies that resource.    
  - Clients interact with a service by exchanging representations of resources. Many web APIs use JSON as the exchange format.    
  - REST APIs use a uniform interface, which helps to decouple the client and service implementations.    

## References   
[Web API design](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)   