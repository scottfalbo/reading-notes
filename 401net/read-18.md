# 401 .NET Read 18: Identity
[Microsoft docs: Intro to Identity](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity?view=aspnetcore-2.1&tabs=visual-studio)<br>
[Auth Demystified](https://digitalmccullough.com/posts/aspnetcore-auth-system-demystified.html)<br>

Identity is a membership system that adds login functionality to apps.  It allows for users to login in with a username that is stored in a database, or via facebook, google, twitter, or microsoft account.
Identity uses a database to store usernames, passwords, and user data.

Like all of the services we use in ASP.NET CORE we have to bring in the service in the `ConfigureServices` method is the `startup.cs`.

Components and behavior:
+ **Identity** - Identity is represented by three classes
  + *Claim* - contains a single piece of user data.
  + *ClaimsIdentity* - a way to prove who you are with multiple pieces of information.  The digital equivalent of a license.
  + *ClaimsPrinciple* - represents the actually user and can have many claimIdentities, like a license, ssn card, etc.
+ **Verbs** - Commands or behaviors
  + *Authenticate* - gets user if info it exists. 
  + *Challenge* - requests auth by user.
  + *SignIn* - Persists the user information somewhere.
  + *SignOut* - removes the persisted information.
  + *Forbid* - denies access to a resource.
+ **Auth Handlers** - are the components that implement the above behaviors.
+ **Middleware** - a layer between client and database that calls the handler.

[Back to the main page](../README.md) 