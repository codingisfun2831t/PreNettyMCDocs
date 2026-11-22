# Client Set Block
Protocol version 1 (Classic MpTest1, c0.0.15a), C2S

Sent whenever the client places/breaks a block. Note: The `Block Type` field is always the currently selected block on the original client, even when the `Created` flag is `false`. The server should set the block to air (`0`) when its `false`!

| Field | Type | Description|
|-|-|-|
| X | `short` | X position to set. |
| Y | `short` | Y position to set. |
| Z | `short` | Z position to set. |
| Created | `boolean` | True when the block is placed, not destroyed. |
| Block Type | `byte` | [Block Type.](../../BLOCKS.md) |