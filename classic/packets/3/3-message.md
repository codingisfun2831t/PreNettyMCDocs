# Message

Protocol version 3 (c0.0.16a), S2C or C2S

Sent from the client/server to send a message to the other side.

| Field     | Type      | Description                                                                                                                          |
| --------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Player ID | `sbyte`   | Player ID. Positive values mean another player (meaning a max of 128 players), and negative means the client this packet is sent to. |
| Message   | `cstring` | Chat message. See [Color Codes](..\..\..\COLOR_CODES.md)                                                                             |
