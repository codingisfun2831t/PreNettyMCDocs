# Version 7 Classic 0.28 to 0.30

Multiplayer protocol from Classic 0.28 to 0.30.

Version 7 extended the blocks to ID 49 and allowed the server to change user OP on command.

- 0x00: [Identification](../packets/6/6-identification.md)
- 0x01: Keep alive packet (No fields)
- 0x02: Level Initialize packet, used to notice the client of a level (No fields)
- 0x03: [Level Data Chunk](../packets/1/1-level-data-chunk.md)
- 0x04: [Level Finish](../packets/1/1-level-finish.md)
- 0x05: [Client Set Block](../packets/1/1-client-set-block.md)
- 0x06: [Server Set Block](../packets/1/1-server-set-block.md)
- 0x07: [Spawn Player](../packets/1/1-spawn-player.md)
- 0x08: [Set Player Position](../packets/1/1-set-player-position.md)
- 0x09: [Delta Position and Rotation](../packets/3/3-delta-posrot.md)
- 0x0a: [Delta Position](../packets/3/3-delta-pos.md)
- 0x0b: [Change Rotation](../packets/3/3-change-rot.md)
- 0x0c: [Despawn Player](../packets/1/1-despawn-player.md)
- 0x0d: [Message](../packets/3/3-message.md)
- 0x0e: [Disconnect](../packets/3/3-disconnect.md)
- 0x0f: [Change User OP](../packets/7/7-user-op.md)