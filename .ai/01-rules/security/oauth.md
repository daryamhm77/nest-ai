# OAuth2 / OIDC

- Use Authorization Code + PKCE for first-party and SPA clients.
- Validate `state` (CSRF) and `nonce` (replay) on callback.
- Verify ID token signature, issuer, audience, expiry.
- Store provider tokens encrypted; never log them.
- Map external identities to internal accounts explicitly; handle account linking.
