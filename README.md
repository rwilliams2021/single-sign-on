# single-sign-on
implement SSO – Single Sign On – using Spring Security OAuth and Spring Boot, using Keycloak as the Authorization Server.

We’ll use 4 separate applications:

An Authorization Server – which is the central authentication mechanism
A Resource Server – the provider of Foos
Two Client Applications – the applications using SSO
Very simply put, when a user tries to access a resource via one Client app, they’ll be redirected to authenticate first, through the Authorization Server. Keycloak will sign the user in, and while still being logged in the first app, if the second Client app is accessed using the same browser, the user will not need to enter their credentials again.

We’re going to use the Authorization Code grant type out of OAuth2 to drive the delegation of authentication.

We’ll use the OAuth stack in Spring Security 5.