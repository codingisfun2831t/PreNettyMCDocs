# Spawn Player

Protocol version 1 (Classic MpTest1, c0.0.15a), S2C

Sent from the server to spawn a new player (other client) or to set the client's inital position.

Check [Player Position](../../POSITION.md) for more info,

| Field       | Type      | Description                                                                                                                          |
| ----------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Player ID   | `sbyte`   | Player ID. Positive values mean another player (meaning a max of 128 players), and negative means the client this packet is sent to. |
| Player Name | `cstring` | Name of this player.                                                                                                                 |
| X           | `fshort`  | X position.                                                                                                                          |
| Y           | `fshort`  | Y position.                                                                                                                          |
| Z           | `fshort`  | Z position.                                                                                                                          |
| Yaw         | `byte`    | Yaw rotation.                                                                                                                        |
| Pitch       | `byte`    | Pitch rotation.                                                                                                                      |

NOTE! On protocols before version 4, ID `-1` (the local client), yaw and pitch are flipped; and pitch is opposite (`255 - pitch`.)