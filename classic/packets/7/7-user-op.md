# User OP

Protocol version 6 (c0.0.20a), S2C

Sent from the server to change a client OP status.

| Field            | Type      | Description                                         |
| ---------------- | --------- | --------------------------------------------------- |
| OP               | `byte`    | 0x64 if OP (player can break bedrock), 0x00 if not. |