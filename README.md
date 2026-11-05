# Beaver Valley

A relaxed, mobile-friendly three.js game: you play a beaver in a procedurally
generated valley. Chew trees for logs, build dams anywhere, watch ponds fill,
build a lodge, and wildlife moves in as the wetland grows. There is no fail state.

**▶ [Play it in your browser](https://jmorrisseyd.github.io/Beaver-Builder/)**

## Controls

| | Desktop |
|---|---|
| Move | `WASD` |
| Act (chew / build / enter) | `Space` |
| Build dam | `B` |
| Splash | `Q` |

Touch controls are built in, so it plays on a phone as-is.

## Running it locally

The whole game is one self-contained `index.html` — HTML, CSS and a single
ES module. three.js r160 loads from a CDN via an import map; there are no other
assets, because every texture is painted onto a canvas at load time and all
sound is synthesised with WebAudio.

Serve the folder with any static server and open it:

```bash
python3 -m http.server
```

Then visit <http://localhost:8000>. Use the browser's phone emulation to test
the touch controls.

## Saves

Progress autosaves to `localStorage`. The journal can also produce a portable
save code (prefixed `BV1-`) that you can paste on another device.

## Development notes

See [CLAUDE.md](CLAUDE.md) for the code map: the script's `// ====` sections,
the water simulation, the save format and the performance constraints.
