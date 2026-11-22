# Client/Server identification

Protocol version 3 (c0.0.16a), C2S or S2C

Sent from the client to handshake with the server, and vice versa.

Both packets have the same format but different semantics of the fields.

## C2S

| Field            | Type      | Description                                     |
| ---------------- | --------- | ----------------------------------------------- |
| Protocol Version | `byte`    | Protocol version the client supports.           |
| Username         | `cstring` | The name of the client.                         |
| Unused           | `cstring` | Unused by the server when sent from the client. |

## S2C

| Field            | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| Protocol Version | `byte`    | Protocol version the server supports. |
| Name             | `cstring` | The name of the server.               |
| MOTD             | `cstring` | MOTD/Description of the server.       |

A client shall send this packet with its username and protocol it support to the server. When the server detects this packet, it should check if its protocol version equals the client. If it doesn't, the server should do something about it; maybe activate a compatibility mode, disconnect the client with a message if possible. But if it equals the server should accept the client, send the S2C packet with the info it wants.