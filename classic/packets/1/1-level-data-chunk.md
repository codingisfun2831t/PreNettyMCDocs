# Level data chunk

Protocol version 1 (Classic MpTest1, c0.0.15a), S2C

Before anything else, lets describe how the level is sent. The level data increments X fastest, followed by Z, and then Y: `idx(x, y, z, width, depth) = (y * depth + z) * width + x`. Each block is stored as one byte. Before the block data, there is a `int` (big endian!) before with the length of the blocks. That data is then gzipped and split into 1024 byte chunks, and each of those chunks is sent over this packet.

| Field    | Type         | Description                                                                                                |
| -------- | ------------ | ---------------------------------------------------------------------------------------------------------- |
| Length   | `ushort`     | Length of the data chunk. Most chunks will have 1024, but the last chunk may have a value lower than this. |
| Data     | `byte[1024]` | Always 1024 bytes, if the data is smaller this is padded with zeroes.                                      |
| Progress | `byte`       | 0-100, describes percent done with the level.                                                              |

A server will send any amount of these chunks between Initailize and [Finish](1-level-finish.md) packets, and a client should read them as they come in, store the GZipped data, and update the progress display. At the end the client should collect the data, unzip it, and then store that data.