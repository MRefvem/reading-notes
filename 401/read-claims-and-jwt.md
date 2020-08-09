# Read: Claims and JWT

## Microsoft Docs: Claims-based authorization in ASP.NET Core

When an identity is created it may be assigned one or more claims issued by a trusted party. A claim is a name value pair that represents what the subject is, not what the subject can do. Claims based authorization, at its simplest, checks the value of a claim and allows access to a resource based upon that value.

The simplest type of claim poilicy looks for the presence of a claim and checks the value.

The AuthorizeAttribute attribute can be applied to an entire controller, or to a specific method. If you have a controller that's protected by the AuthorizeAttribute attribute, but want to allow anonymous access to particular actions you apply the AllowAnonymousAttribute attribute.

## Andrew Lock: Introduction to Authentication with ASP.NET Core

### The difference between Authentication and Authorization

Authentication is the process of determining who you are while Authorization revolves around what you are allowed to do (i.e. permissions). 

## Rachit Gulati: JWT to authenticate Servers API's

### What is JWT?

JSON Web Token (JWT) is a means of representing claims to be transferred between two parties. The claims in a JWT are enclosed as a JSON object that is digitally signed using JSON Web Signature and/or encrypted using JSON Web Encryption (JWE).

In simple terms, it is just another way of encoding JSON object and use that encoded object as access tokens for authentication from the server.