# 401 .NET Read 27: Cookies

## Claims
A claim is a key value pair that represents what a user is.  It's like a name or birth date on a license.  In order to gain access to certain things you much prove that you are who you are.  The thing authenticating you must be a trusted source as well.  

Claim checks are set up in the `ConfigureSerives` method in `Startup.cs`.  Each one is a policy and the required claim to gain access to content.
```
services.AddAuthorization(options =>
{
    options.AddPolicy("SecretArea", policy =>
      policy.RequireClaim("PassCode"));
});
```
use the policy to decorate classes and methods that require the policy and claim.
```
[Authorize(Policy = "SecretArea")]
public class HiddenStuff(){}
```

+ **Authentication** - defines you are.
+ **Authorisation** - defines what you can do.

A `principal` can have multiple identities, and identities can have multiple claims.  The `ClaimsPrincipal` inherits all of the `claims` of its `identity`.

---
JWT authentication has two parties, the server (producer), and the client (consumer).
  + Producer - The producer is the server, the ones that gives the service.  It provides the access token.
  + The consumer is the client which uses the token to consume the API.



[Back to Mainpage](../code-fellows.md)<br>