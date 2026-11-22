# Version 1 Classic MPTest1

First multiplayer protocol from [Classic MpTest1, version 0.0.15a.

* 0x00: [Identification](../packets/1/1-identification.md)
* 0x01: Keep alive packet (No fields)
* 0x02: Level Initialize packet, used to notice the client of a level (No fields)
* 0x03: [Level Data Chunk](../packets/1/1-level-data-chunk.md)
* 0x04: [Level Finish](../packets/1/1-level-finish.md)
* 0x05: [Client Set Block](../packets/1/1-client-set-block.md)
* 0x06: [Server Set Block](../packets/1/1-server-set-block.md)
* 0x07: [Spawn Player](../packets/1/1-spawn-player.md)
* 0x08: [Set Player Position](../packets/1/1-set-player-position.md)
* 0x09: [Despawn Player](../packets/1/1-despawn-player.md)