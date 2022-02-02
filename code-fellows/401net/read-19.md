# 401 .NET Read 19: Claims and JWT Tokens

## Claims
A claim is a key value pair that represents what a user is.  It's like a name or birth date on a license.  In order to gain access to certain things you much prove that you are who you are.  The thing authenticating you must be a trusted source as well.  

Claim checks are set up in the `ConfigureSerives` method in `Startup.cs`.  Each one is a policy and the required claim to gain access to content.
```
services.AddAuthorization(options =>
{
    options.AddPolicy("SecretArea", policy => policy.RequireClaim("PassCode"));
});
```
use the policy to decorate classes and methods that require the policy and claim.
```
[Authorize(Policy = "SecretArea")]
public class HiddenStuff(){}
```

+ **Authentication** - defines you are.
+ **Authorisation** - defines what you can do.


## JWT, Json Web Token

Producer - The one who gives the service, the API provider.
Consumer - The client, who will need to provide a valid JWT.

In server to server auth both producer and consumer need to share the same contract.
1. Share the secret
2. Prepare the payload
3. Get the token
4. Identify the consumer

[Back to Mainpage](../code-fellows.md)<br>