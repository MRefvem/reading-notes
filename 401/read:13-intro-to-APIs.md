# Read:13 - Intro to APIs

## YouTube - Microsoft: Intro to APIs

How to build Web APIs in .NET Core

Install .NET Core 2.0 and Visual Studio

What is a Web API?
- An HTTP service
- Logic or data accessible 

HTTP refresher
- Application layer protocol
- Used to access resources identified by a URI
- Access resources using standardized methods/verbs
- Stateless request-reply protocol
- Headers and response bodies - formats
- Status codes indicate the type of response

Status codes:
- 200 level: a good request
- 400 client side problem
- 500 internal service error

Handling HTTP requests with ASP.NET Core
- The server (kestrel) listens for requests
- The middleware pipeline is invoked for each request
- Use MVC to route requests to a controller and action
- Responses flows back down the middleware pipeline

To create a Web API
- Create an ASP.NET Core project
- Setup MVC
- Create a class that derives from ControllerBase
- Implement your Action Methods

Route templates
- Extract route values (ex "api/orders/{id}")
- Use route tokens (ex "api/[controller]")
- Optional route values: {id?}
- Default route values

Model binding and validation
- Bind request data to action parameters
- Bind form data, route values and query string parameters by default
- Use [FromBody] to bind the reqeust body using formatters
User [FromRoute/Query/Form/Header] to restrict model binding to a particular source
- Use data annotations and check ModelState.IsValid