# Nara Cards · 奈良めぐりカード

A full-screen 3D card deck about Nara, built with three.js in a single HTML file.
Swipe through seven cards, flip them over, hold one up close to look into the picture, or send the whole deck into a 3D ring.

**Live:** https://sinastoler.github.io/nara-cards/

## Controls

| Action | Mouse / touch | Keyboard |
|---|---|---|
| Next / previous card | Drag left / right, or flick | ← → or the mouse wheel |
| Flip a card | Tap the top card | Space |
| Look closer | Press and hold the top card, then move | |
| 3D Flow mode | The "3D Flow" button | F (Esc to return) |
| Pick a card in Flow | Tap it | |

## What's inside

- **One continuous state.** The deck is a single number (2.4 = between the 3rd and 4th card) driven by a critically damped spring. Every card's position, rotation, bend and fade is a function of that number, so dragging, releasing, springing back and pulling a card back are all continuous.
- **Cards in WebGL.** Each card is a curved plane with its own shader: rounded corners, two faces, a bow while it moves, a glossy highlight and a holographic sheen on the picture.
- **Depth inside the pictures.** The illustrations are painted in layers; their silhouettes become a depth map, and the shader shifts near layers against far ones as the card tilts.
- **3D Flow.** The cards leave the stack one by one, swoop past the camera and settle on a ring over a reflective floor.
- **Procedural art.** Every picture (deer, Todai-ji, the five-storey pagoda, Kasuga lanterns, Mt. Wakakusa, Naramachi) is drawn in code; no image files.

`demo.html` holds two kinetic-type experiments: karaoke-filled words on 3D planes, and letters riding a 3D orbit.

## Run locally

The pages load three.js and fonts from CDNs, so serve the folder over HTTP (opening the file directly will not work):

```sh
python -m http.server 8000
```

Then open http://localhost:8000/.
