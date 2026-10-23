# @Home

A browser remake of **@Home**, made at Global Game Jam 2019 (theme: "What home means to you") at the IAC – Israeli Animation College jam site.

Home is safe, but it shrinks while you're in it. Go outside to make it grow again, and the further out you go, the faster it grows. Ghosts chase you outside, and one touch disqualifies you. Furniture blocks their view, so you can duck behind it to lose them. Collect the points out in the open: an arrow shows the way, and each one grows your home.

## Controls

| Key | Action |
|---|---|
| WASD / arrows | Move |
| Space | Start / pause |
| R | Restart |
| + / − | Circle change speed |
| [ / ] | Number of ghosts |

Circle speed and ghost count are remembered between games.

## Run it

- `prototype/index.html` is the development version. It loads Three.js 0.160.0 from the jsDelivr CDN.
- `dist/` is the self-contained build with Three.js bundled. It's what goes to itch.io.

Both use an import map, so serve the folder over HTTP rather than opening the file directly:

```bash
python3 -m http.server 8417 --directory prototype
```

To build the itch.io upload zip:

```bash
cd dist && zip -X ../athome-itch.zip index.html three.module.js
```
