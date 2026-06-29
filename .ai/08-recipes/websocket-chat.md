# Recipe: WebSocket Chat
1. Authenticate JWT in the handshake; reject otherwise.
2. Join `tenant:<id>` and `room:<id>` after authorizing membership.
3. Validate each message with a DTO; persist + broadcast to the room.
4. Scale across instances with the Redis adapter. Heartbeats for liveness.
Rules: `01-rules/websocket/README.md`.
