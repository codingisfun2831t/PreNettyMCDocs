# Set Player Position

Protocol version 1 (Classic MpTest1, c0.0.15a), S2C or C2S

Sent from the client to move its player, and sent from server to tell a client about the movement of someone.

Check [Player Position](../../POSITION.md) for more info.

| Field     | Type     | Description                                                                                                                                                                            |
| --------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Player ID | `sbyte`  | Player ID. Positive values mean another player (meaning a max of 128 players), and negative means the client this packet is sent to. (Or, if this packet was from a client, always -1) |
| X         | `fshort` | X position.                                                                                                                                                                            |
| Y         | `fshort` | Y position.                                                                                                                                                                            |
| Z         | `fshort` | Z position.                                                                                                                                                                            |
| Yaw       | `byte`   | Yaw rotation.                                                                                                                                                                          |
| Pitch     | `byte`   | Pitch rotation.                                                                                                                                                                        |

This packet, in Classic Version c0.0.18a and under, can not work to teleport the local player (i.e. server sends player id -1 to client).