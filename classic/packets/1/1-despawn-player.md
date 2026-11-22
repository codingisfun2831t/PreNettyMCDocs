# DeSpawn Player

Protocol version 1 (Classic MpTest1, c0.0.15a), S2C

Sent from the server to despawn spawn a player (other client).

| Field     | Type    | Description                                                                    |
| --------- | ------- | ------------------------------------------------------------------------------ |
| Player ID | `sbyte` | Player ID. Positive values mean another player (meaning a max of 128 players). |
