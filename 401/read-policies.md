# Read: Policies

## Microsoft Docs: Policy-based authorization in ASP.NET Core

Underneath the covers, role-based authorization and claims-based authorization use a requirement, a requirement handler, and a pre-configured policy. These building blocks support the expression of authorization evaluations in code. The result is a richer, reusable, testable authorization structure.

An authorization policy consists of one or more requirements. It's registered as part of the authorization service configuration, in the Startup.ConfigureServices method.

The primary service that determines if authorization is successful is IAuthorizationService.

If an authorization policy contains multiple authorization requirements, all requirements must pass in order for the policy evaluation to succeed.

An authorization handler is responsible for the evaluation of a requirement's properties. The authorization handler evaluates the requirements against a provided AuthorizationHandlerContext to determine if access is allowed.

A requirement can have multiple headers. A handler may inherit Authorization/handler<TRequirement>, where TRequirement is the requirement to be handled. Alternatively, a handler may implement IAuthorizationHandler to handle more than one type of requirement.

The code must traverse PendingRequirements - a property containing requirements not marked as successful.

Handlers are registered in the services collection during configuration.

Since the handler method returns no value, the status of either a success or failure is indicated:
- A handler indicates success by calling context.Succeed(IAuthorizationRequirement requirement), passing the requirement that has been successfully validated.
- A handler doesn't need to handle failures, as other handlers for the same requirement may succeed.
