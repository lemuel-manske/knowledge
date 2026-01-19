> [RFC](https://datatracker.ietf.org/doc/html/rfc6749)

OAuth is an [[Authorization]] framework, not an [[Authentication]] protocol.

OAuth is a protocol about relationships between actors, not about users per se.

> In the traditional client-server authentication model, the client
requests an access-restricted resource (protected resource) on the
server by authenticating with the server using the resource owner's
credentials.  In order to provide third-party applications access to
restricted resources, the resource owner shares its credentials with
the third party. This creates several problems and limitations.

> Instead of using the resource owner's credentials to access protected
resources, the client obtains an access token -- a string denoting a
specific scope, lifetime, and other access attributes.  Access tokens
are issued to third-party clients by an authorization server with the
approval of the resource owner.  The client uses the access token to
access the protected resources hosted by the resource server.

> For example, an end-user (resource owner) can grant a printing
service (client) access to her protected photos stored at a photo-
sharing service (resource server), without sharing her username and
password with the printing service.  Instead, she authenticates
directly with a server trusted by the photo-sharing service
(authorization server), which issues the printing service delegation-
specific credentials (access token).

```mermaid
flowchart LR:
    Client -->|Requests Authorization| ResourceOwner
    ResourceOwner -->|Grants Authorization| Client

    Client -->|Requests Access Token| AuthorizationServer
    AuthorizationServer -->|Issues Access Token| client

    Client -->|Accesses Protected Resource| ResourceServer
    ResourceServer -->|Protected Resource| Client 
```
