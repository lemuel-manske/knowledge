Opaque means not transparent. An opaque token is meant to have a format that is not intended to be read, like a random string.

This contrasts with self-contained tokens (like {{JsonWebTokens}}), which embed claims and can be validated without calling the issuer. Such introspection may be implemented via introspection endpoints, shared token stores, or caches.

Such tokens deliberately trade client-side convenience for stronger server-side control and security guarantees. Hence, the authorization server remains the source of truth.

- You can revoke a token instantly
- You can change permissions without reissuing tokens
- You can invalidate tokens globally (incident response, user logout, compromise)
- You can apply real-time, context-aware authorization decisions during token evaluation

In {{OAuth}}, opaque tokens can be used as `access_tokens` or `refresh_tokens`:

> Tokens in a proprietary format that typically contain some identifier to information in a server’s persistent storage. To validate an opaque token, the recipient of the token needs to call the server that issued the token.

This model introduces a runtime dependency on the authorization infrastructure, which must be highly available and scalable.
