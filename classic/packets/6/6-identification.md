# Client/Server identification

Protocol version 6 (c0.0.20a), C2S or S2C

Sent from the client to handshake with the server, and vice versa.

Both packets have the same format but different semantics of the fields.

## C2S

| Field            | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| Protocol Version | `byte`    | Protocol version the client supports. |
| Username         | `cstring` | The name of the client.               |
| Verification Key | `cstring` | Verification key.                     |
| Unused           | `byte`    | Unused in server. |

## S2C

| Field            | Type      | Description                           |
| ---------------- | --------- | ------------------------------------- |
| Protocol Version | `byte`    | Protocol version the server supports. |
| Name             | `cstring` | The name of the server.               |
| MOTD             | `cstring` | MOTD/Description of the server.       |
| OP               | `byte`    | 0x64 if OP (player can break bedrock), 0x00 if not. |

A client shall send this packet with its username and protocol it support to the server. When the server detects this packet, it should check if its protocol version equals the client. If it doesn't, the server should do something about it; maybe activate a compatibility mode, disconnect the client with a message if possible. But if it equals the server should accept the client, send the S2C packet with the info it wants.

Verification key, on the original Minecraft Classic server, is calcuated using a salt the server gives the minecraft.net heartbeat with the player name, i.e. `md5(salt + player.name)`. The server is able to get this salt and therefore get the correct hash for the client to send to the server. Unless you carelessly expose your salt a "cracked" (un-paid) player cant fake it. The verification key might be calcuated different or unneeded on modern servers.


