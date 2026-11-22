# Server Set Block
Protocol version 1 (Classic MpTest1, c0.0.15a), S2C

Sent whenever the server changes a block.

| Field | Type | Description|
|-|-|-|
| X | `short` | X position to set. |
| Y | `short` | Y position to set. |
| Z | `short` | Z position to set. |
| Block Type | `byte` | [Block Type.](../../BLOCKS.md) |