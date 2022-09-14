---
title: "[REST] REST API 모범 사례"
category: REST
tag:
- REST
- API
- Endpoint
- Music
- Ticket
---

API는 모든곳에서 사용한다. 온라인에서 피자를 주문하고 요금을 걸재 하는것 부터, 음악을 듣고, 드라마를 보는것처럼, 세계를 연결된 상태로 유지 시키고 있다.

> 본 글은 다음의 글을 번역한 글이다. [Best Practices for rest api](https://medium.com/chegg/best-practices-for-rest-api-df7417ea07e5)

> Q. 나는 소프트웨어의 양 끝을 이어주는 역활을 한다. 또한 누군가 나를 건드리면 반응하는 역활도 수행한다.
> A. 그래, 나는 API Endpoint이다. 

최근에는 API는 모든 곳에서 사용한다. 온라인에서 피자를 주문하고 요금을 지불하는것 부더, 티켓을 예매하고, 음악을 듣고, 더 나아가 애플리케이션을 만들때 산업 표준으로 자리잡아가고 있다. 간단히 말해서, 세계를 연결된 상태로 유지 시키고 있다.

# API란 무엇인가?

API는 Application Programming Interface의 축약어이다.

API는 제공자(Provider)와 클라이언트(Client) 사이의 통신(Communication)을 제공한다. 다른 소프트웨어에 서비스를 제공하는 인터페이스의 한 종류이다. API을 어떻게 만든는지 또는 연결이나 인터페이스를 어떻에 사용하는지 설명하는 문서(Document)나 규격(Standard)을 API 표준(API Specification)이라고 한다. 이러한 규격을 만족하는 컴퓨터 시스템을 API를 구현하거나 노출시킨다고 얘기한다. API 용어는 표준(Specification)이나 구현(Implimentation)을 참조(Refer) 한다고 말 할 수 있다.

# Rest API란 무었인가?

SOAP 기반의 웹 서비스와는 다르게 RESTful API에는 공식적인 표준이 없다. REST는 아키텍처 스타일이고, SOAP는 프로토콜이기 때문이다. REST 자체로는 표준이 아니고, RESTful은 HTTP, URI, JSON, and XML와 같은 표준을 사용하는것을 구현한다.

REST는 performance, scalability, simplicity, modifiability, visibility, portability, and reliability를 향상 시키는데 목표를 두고 있다. client-server architecture, statelessness, cacheability, use of a layered system, support for code on demand, and using a uniform interface와 같은 REST 원칙을 따랏을때 이것들을 달성 할 수 있다. 

# Rest API 모범 사례

앞으로의 내용은 개발자와 테스터가 REST API를 개발하거나 테스트 할 때 좋은 사례이다.

# API Endpoint Naming

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