# Client/Server identification
Protocol version 1 (Classic MpTest1, c0.0.15a), C2S or S2C

Sent from the client to handshake with the server, and vice versa. Just the username for the inital multiplay test.

| Field | Type | Description|
|-|-|-|
| Username | `cstring` | The name of the client. |

A server should receive this message from the client, and then send this same packet back; the string sent from the server is unused.