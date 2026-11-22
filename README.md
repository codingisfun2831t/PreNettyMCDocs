# PreNettyMC-Docs
This project aims to document every packet and behavior of the Minecraft network protocol, from 1.6.4 and eariler; before Minecraft switched to Netty in 1.7.

HEAVY WORK IN PROGRESS! Help is needed.

# Structure
Before any packet, check out the TYPES.md file. It will describe any type used throughout. There are two main folders, `classic` and `survival`. `classic` has the MC classic packets/versions, protocol versions up to 7, specfically Classic 0.0.15a to 0.30. `survival` is for everything after Alpha, HOWEVER versions 13 and 14 are used in both Alpha (v1.0.15 to v1.0.16) and Beta (1.6-1.7.3). Those alpha versions will be prefixed with `a`, so 13 and 14 becomes a13 and a14.

Now in those two folders, there will be two folders inside them, `packets` and `versions`. `packets` will describe every packet from each protocol version in that section, e.g. there will be a folder `14` in `survival` which describes the changes b1.7 added. In each of those folders, there will be a Markdown file for every packet updated in that version. E.g. `14-block-action.md` for the changes in the Block Action packet for pistons. Note that theres no packet ID! Each version decides what ID gets attached to what packets. For any empty packets, for example the Level Initialize packet in Classic, no packet file will be made and the version list will simply not have a link and say `(No fields)`.

In `versions`, there will be Markdown files with the protocol version (that the packet was introduced/updated in) and the version range, e.g. `14-b1.7-b1.7.3.md` for version 14. These will have every packet in that version as links to files in the packets folder, so you can fully check every packet from a version instead of digging through old versions to find the last change. It will also have a [Minecraft Wiki](https://minecraft.wiki/) page for that version.

Of course, each packet has the packet ID it is assocated with at the start of the packet sent as a byte, before the payload!

With all of that away, enjoy these docs! I've noticed a big gap in documenting these protocol versions, so here they are!

# License
Licensed under CC0 1.0, see [LICENSE.txt](LICENSE.txt)