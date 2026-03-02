# TacoScape

TacoScape is a mesh-based audio visualizer shader. It’s intended for **large surfaces** (dance floors, domes, walls) where vertex motion becomes the show.

## What “good” TacoScape motion looks like

You want a **spatial displacement field**:
- adjacent vertices move differently
- waves propagate across the surface
- different AudioLink bands can drive different layers of motion

You generally do *not* want:
- uniform shrink/grow
- whole-mesh lift/lower

## Mesh requirements

- Higher vertex density = better deformation detail
- Clean UVs help if the shader uses UV-driven waves
- Consistent object scale helps if the shader uses object/world space

If effects vary wildly per mesh:
- add scale compensation (bounds-based)
- normalize displacement by object size
- provide coordinate modes (UV vs object vs world) where possible

## Best practices

- Start with bass-driven large waves
- Layer mid/high bands as detail (with smoothing)
- Keep extremes comfortable for VR
