# Manage the Authentication and Authorization Server for Protecting the Microservices

* Status: Proposed
* Deciders: Binoy
* Date: 2024-10-27

## Context and Problem Statement

Our microservices application requires a centralized authentication and authorization server to secure the APIs of each microservice. This server should handle user management, including roles and permissions, and enforce access control using the OAuth2 protocol to authorize requests to the microservices. Additionally, the server must support OpenID Connect for user authentication, enabling the assignment of roles to each user and ensuring that they have appropriate access rights to specific microservices.

## Decision Drivers

* Need to support the OpenID connect
* Able to maange user, roles, and groups
* Able to monitor the service

## Considered Options

* Keycloak authentication server

## Decision Outcome

Chosen option: "Keycloak authentication server", because This open sources authentication and authorization server, it support OpenId connect and provides lot of functionalities such as

* It provides central dashboard where we can managing following functionality in high level
* Multi tenant (Relam)
* User
* Group
* Role
* Scope
* Identity Broker
* Federation
* We can easy integrate with multiple framework
* It provided the Oauth2 protocol for authentication and authorisation

### Positive Consequences

* Keycloak can integrate with Prometheus server for monitoring the metrics
* Prometheus server collect the metrics from Keycloak and can be easily identify the issue if any happen
* For adding the more security, we need to authorise each microservice based on the token
* This helps internal communication between microservices will be protected. This helps to reduce the middle attack / data manipulation

### Negative Consequences

* Tunning required based on our requirements
