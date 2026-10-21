# bongocat-assets

Sprite assets for the BigBongo keyboard visualizer.

- `MODEL/<Cat>.pack` — zlib of the 4 frames (Left, LeftPunch, Right, RightPunch)
  concatenated. The ESP32 downloads one pack per cat (one request), inflates it
  on-device (ROM miniz) to the exact original 480x320x4 ARGB bytes — lossless.
- `ACCESSORIES/<name>.argb.zz` — zlib of one accessory frame.

Served via jsDelivr, e.g.
    https://cdn.jsdelivr.net/gh/bbthegod/bongocat-assets@main/MODEL/Black.pack
