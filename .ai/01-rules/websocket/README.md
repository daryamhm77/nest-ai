# WebSocket Rules
- Authenticate on connection (JWT in handshake); reject unauthenticated sockets.
- Authorize each subscription/room join server-side.
- Use rooms/namespaces per tenant; never broadcast across tenants.
- Validate every inbound message with DTOs.
- Scale with the Redis adapter for multi-instance fan-out.
