# Getting started

This documentation covers **TacoFX Ultimate**, a VRChat PC shader system built around 4 families:

- **TacoScreenFX**: full-screen effects rendered on a camera-aligned quad
- **TacoMeshShader**: surface + optional vertex effects for props, architecture, “set dressing”
- **TacoScape**: mesh-based audio visualizer surfaces (dance floors, domes, walls)
- **DepthFX**: depth/volume-styled visuals (raymarch-inspired look and 3D space effects)

## Recommended workflow

1. Import the package (see [Installation](installation.md)).
2. Drop in the provided example prefab(s) for each shader family.
3. Verify the shader renders in Play Mode.
4. Add AudioLink (see [AudioLink setup](audiolink-setup.md)).
5. Enable effects gradually and tune:
   - global intensity
   - per-effect intensity
   - band selection (global vs per-effect)
   - smoothing (where available)

## How to think about AudioLink

AudioLink provides multiple “bands” (bass → treble). Different effects feel best on different bands.

- Use **bass** for large, slow, physical motion (pulses, ripples, expansion)
- Use **mids** for “busy” motion (glitches, glyphs, detail animation)
- Use **treble** for sharp flicker (sparks, fine jitter), but always apply smoothing/limiting for comfort

## If something looks wrong

Start with [Troubleshooting](troubleshooting.md) and work top to bottom.
