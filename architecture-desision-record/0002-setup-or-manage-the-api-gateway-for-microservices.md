# Setup or Manage the API Gateway for Microservices

* Status: Proposed
* Deciders: Binoy
* Date: 2024-10-27

## Context and Problem Statement

In a microservices architecture, an API Gateway is essential for managing client connections to microservices. Acting as a reverse proxy, the API Gateway routes incoming client requests to the appropriate upstream services. It should also handle authorization by interacting with an identity server to validate tokens before forwarding requests to the designated microservices.

## Decision Drivers

* Highly performance: It required highly performance to handle the requests
* Security: Authorise the requests with identity server,  Open ID connection need to support
* Able to monitor the request and trace the logs

## Considered Options

* KONG Api Gateway
* OpenResty Framework
* Spring Boot API Gateway

## Decision Outcome

Chosen option: "OpenResty Framework", because It high performance webframework and this framework build on top of Nginx and Lua language

Choose Kong if you need a high-performance gateway with extensive plugin support and deployment flexibility. Kong API paid version support only Authorization capability. 
Choose Spring Boot API Gateway if you’re fully invested in the Spring ecosystem and need a gateway solution integrated with Spring Cloud.

### Positive Consequences

* NGINX Server: A high-performance web server.
* Reverse Proxy Support: NGINX can act as a reverse proxy, directing requests to appropriate backend services.
* SSL Termination: NGINX supports SSL termination, providing secure HTTPS connections.
* Monitoring Integration: NGINX can be connected to monitoring tools to track performance and health metrics.
* Security Configuration: Allows configuration of security rules, such as rate limiting and IP whitelisting, to control access.
* Lua Language: A high-performance language widely used in game development.
* OpenResty Framework: A web framework built on NGINX with seamless integration for services like OpenID Connect, enhancing interoperability with other systems.

### Negative Consequences

* Experience required LUA language
* Experience required Open Resty
* Deployment and local setup challanes
