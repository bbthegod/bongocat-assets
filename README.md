# bongocat-assets

Sprite assets for the BigBongo keyboard visualizer.

- `MODEL/<Cat>.pack` — zlib of the 4 frames (Left, LeftPunch, Right, RightPunch)
  concatenated. The ESP32 downloads one pack per cat (one request), inflates it
  on-device (ROM miniz) to the exact original 480x320x4 ARGB bytes — lossless.
- `ACCESSORIES/<name>.argb.zz` — zlib of one accessory frame.
- `RAW/` — the **original, un-rotated** 256x256 sprites (BGRA, straight alpha), for
  BongoOs 1.16 beta and later, which place and rotate them on the device:
  - `RAW/MODEL/<Cat>.pack` — zlib of the 4 frames (Left, LeftPunch, Right, RightPunch),
    4 x 262144 bytes; a missing frame is transparent.
  - `RAW/ACCESSORIES/<name>.argb.zz` — zlib of one 262144-byte frame.
  Offsets are not stored here (they ship in the device's assets partition), so
  moving an accessory never changes these files.

Served via jsDelivr, e.g.
    https://cdn.jsdelivr.net/gh/bbthegod/bongocat-assets@main/MODEL/Black.pack
