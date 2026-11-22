# Delta Position and Rotation

Protocol version 3 (c0.0.16a), S2C

Sent from the server to move the position by a delta and update rotation.

Check [Player Position](../../POSITION.md) for more info.

| Field     | Type    | Description                                                                                                                          |
| --------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Player ID | `sbyte` | Player ID. Positive values mean another player (meaning a max of 128 players), and negative means the client this packet is sent to. |
| ChangeX   | `fbyte` | Change in X position.                                                                                                                |
| ChangeY   | `fbyte` | Change in Y position.                                                                                                                |
| ChangeZ   | `fbyte` | Change in Z position.                                                                                                                |
| Yaw       | `byte`  | Yaw rotation.                                                                                                                        |
| Pitch     | `byte`  | Pitch rotation.                                                                                                                      |
