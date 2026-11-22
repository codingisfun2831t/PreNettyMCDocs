# Types
Below is every type the protocol across versions uses. Minecraft is, of course, Java; so Notch used its built in [`DataOutputStream`](https://docs.oracle.com/javase/8/docs/api/java/io/DataOutputStream.html), so all numbers are big-endian (biggest byte first).

| Name | Size | Description |
|-|-|-|
| byte | 1 byte | A single unsigned byte (0 to 255) |
| sbyte | 1 byte | A single signed byte (-128 to 127) |
| short | 2 bytes | A single signed short (-32,768 to 32,767) |
| ushort | 2 bytes | A single unsigned byte (0 to 65,535) |
| int | 4 bytes | A single signed integer (-2,147,483,648 to 2,147,483,647) |
| uint | 4 bytes | A single unsigned integer (0 to 4,294,967,295) |
| long | 4 bytes | A single signed integer (-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807) |
| ulong | 4 bytes | A single unsigned integer (0 to 18,446,744,073,709,551,615) |
| cstring | 64 bytes | A Classic string. It is a 64 character string padded with spaces. To parse it simply remove all spaces from the right until you hit a character. |
| byte[`size`] | `size` byte | A byte array of size `size`. |
| fbyte | 1 bytes | A fixed float using a byte, 5 bits for decimal (e.g. num / 32) |
| fshort | 2 bytes | A fixed float using a short, 5 bits for decimal (e.g. num / 32) |
| boolean | 1 byte | 0x00 if false, other value than true. |