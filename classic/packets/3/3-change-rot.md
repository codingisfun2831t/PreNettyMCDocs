# Change Rotation

Protocol version 3 (c0.0.16a), S2C

Sent from the server to update rotation.

Check [Player Position](../../POSITION.md) for more info.

| Field     | Type    | Description                                                                                                                          |
| --------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Player ID | `sbyte` | Player ID. Positive values mean another player (meaning a max of 128 players), and negative means the client this packet is sent to. |
| Yaw       | `byte`  | Yaw rotation.                                                                                                                        |
| Pitch     | `byte`  | Pitch rotation.                                                                                                                      |
