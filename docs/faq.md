# FAQ

## Does TacoFX work on Quest?
No. TacoFX Ultimate is designed for **VRChat PC worlds**.

## Do I need AudioLink?
AudioLink is required for music-reactive behavior. Without AudioLink, effects should still render but will not react to audio.

## Why does my mesh shrink/grow as a whole?
That usually means the shader is applying a single amplitude to all vertices (uniform displacement). For visualizer surfaces, you want position/UV-dependent waves so vertices move differently across the mesh. See [TacoScape](tacoscape.md) and [Troubleshooting](troubleshooting.md#uniform-mesh-motion-breathing).

## Why do tiling/offset sliders do nothing?
Those controls must be wired into the effect’s UV sampling. If they don’t do anything, the shader is not applying the tiling/offset to the UVs. See [Troubleshooting](troubleshooting.md#tilingoffset-sliders-do-nothing).

## Why is an AudioLink effect flickering too aggressively?
Try:
- lower intensity
- switch to bass/low-mid bands
- increase smoothing (if available)
- avoid high-contrast full-screen strobe in VR
