# Classic player position

A player is described by five values, XYZ in floats and Yaw and Pitch in bytes.

XYZ is simply in floats, transmitted over the wire as `fshorts`. However Y is actually the eye position, about `1.59375` blocks above the feet (fixed point: 51), so if you want to stand on a block at Y level 50, the client sends `51.59375` to the server.

But yaw and pitch are different. A yaw of zero means the player is facing towards negative Z/north, increasing in clockwise. (64 means east, 128 means south, 192 means west, and 255 is right before north.) Pitch of zero means level and increases downward, so a pitch of 64 is down and 192 is up. (Note that theres no check on the client for values 65-191 so you can weirdly rotate players heads!)