> **Archived academic project — UMass Lowell, Spring 2018.**
> Kept for the record, not maintained. Written during my MS in Computer Science;
> it reflects what I was learning then, not how I write code today.
> Current work: [k8s-slo-lab](https://github.com/navaneeth-c/k8s-slo-lab)

# Avenger Cube — WebGL / three.js

Final project for **Computer Graphics I**, UMass Lowell, Spring 2018.

An interactive 3D cube rendered with [three.js](https://threejs.org/), using
environment mapping to texture each face with a different hero image, plus
camera and lighting controls. The cube is driven from the keyboard via
`THREEx.KeyboardState()`, which makes it playable as a board-game-style piece
depending on the floor texture used.

Full write-up: [CG_Final_report.pdf](CG_Final_report.pdf).
Original submission notes: [readMe.txt](readMe.txt).

## Running it

Open `avengerCube.html` in a browser. Everything is client-side — no build step
and no server. Some browsers block `file://` texture loads for security reasons;
if the faces render blank, serve the directory over HTTP instead:

```bash
python3 -m http.server 8000   # then open http://localhost:8000/avengerCube.html
```

## Layout

| Path | Contents |
|---|---|
| `avengerCube.html` | Entry point — scene setup and render loop |
| `js/` | three.js and the keyboard-state helper |
| `css/` | Page styling |
| `images/` | Face textures and the environment map |
