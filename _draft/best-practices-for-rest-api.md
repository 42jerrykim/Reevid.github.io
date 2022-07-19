> I am the one who connects the two sides of a software
> And
> I respond back whenever someone HITS me

Yes, that’s right, I am an API endpoint!

These days APIs are everywhere — from ordering pizza online to paying bills, booking tickets, listening to music, and more, they have become an industry standard for building applications. In short, they keep the world connected.
What is API?

API stands for Application Programming Interface.

It provides communication between provider and client. It is a type of software interface that offers a service to other pieces of software. A document or standard that describes how to build or use such a connection or interface is called an API specification. A computer system that meets this standard is said to implement or expose an API. The term API may refer either to the specification or to the implementation.
What is Rest API?

Unlike SOAP-based web services, there is no “official” standard for RESTful web APIs. This is because REST is an architectural style, while SOAP is a protocol. REST is not a standard in itself, but RESTful implementations make use of standards, such as HTTP, URI, JSON, and XML.

The goal of REST is to increase performance, scalability, simplicity, modifiability, visibility, portability, and reliability. This is achieved through following REST principles such as a client-server architecture, statelessness, cacheability, use of a layered system, support for code on demand, and using a uniform interface.
Best Practices for Rest API

I will highlight best practices for both developers and testers while developing and testing Rest API.

API Endpoint Naming

You should refer to the endpoints’ names by using nouns, and their actions type by the method.

If you use verbs with nouns like ‘CreateUser’, ‘DeleteUser’ and ‘GetUser’, then it will create a lot of endpoints.

Let’s suppose you have the ‘/users’ endpoint, then you should specify like this:

    To create a user — /users with post action
    To fetch user details — /users with get action

It will also help reduce the maintenance of the Documentation for API endpoints.

Exposing Minimum Permissions and Using Correct Methods

You should always give the minimum number of permissions for an endpoint. For example, if there is an API endpoint only to receive or fetch information, do not add any other unnecessary API level PUT or POST methods to think about the future.

Using Proper Versioning in API

    Standard HTTP status codes

As we know, REST API is built on top of the HTTP protocol. It is always better to use a unified standard response status so that all team members will understand.

2. Validation on the API level

We should always validate the endpoints with positive and negative scenarios.

If you have developed an endpoint, always try to hit that endpoint by changing its actions method and its name. Always send the requests without mandatory fields in the body.

3. Proper response messages and error handling

It is all about giving the proper HTTP status code to the users. If the error is on the client-side, then it should always be in the 4xx class. If the error is on the server-side, then it should always be in the 5xx class.

For example, if you send a request URL that does not exist on the server, it should always return a 404 with a proper log message. If you hit an endpoint with an invalid action type, then it should always return a 405 with the correct message in the response body, without exposing the stack trace.

4. Considering security aspects

It is always beneficial to limit the number of requests from a single host to protect the server from DDoS attacks. Always use a secured authorization, authentication mechanism, and HTTPS protocol. If you are using a JWT token in your project, you must make sure it does not contain sensitive client data.

5. Documentation

It is incredibly beneficial to have API documentation for your project. To be an effective engineer, you should ensure everything is being documented in the proper way. As a best practice, Swagger and Slate are generally used for API documentation.

For more great content, check out Chegg Engineering!

References:

    Handle multiple base URI to achieve end-to-end api testing using rest assured

    Representational state transfer

    Web API design best practices — Azure Architecture Center

    API — Wikipedia