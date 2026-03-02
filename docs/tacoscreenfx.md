# TacoScreenFX

TacoScreenFX is a screen-space shader system designed to run on a **camera-aligned quad** (or equivalent setup). It’s intended for club/rave environments where you want layered visual treatment without touching every mesh in the world.

## Setup

- Use the provided example prefab/material
- Ensure the quad is correctly placed relative to the camera
- Validate in **Game View / Play Mode**

## Stacking model

TacoScreenFX is designed for **stacking** multiple effects.
Typical stacking order:
1. subtle base treatment (vignette, dirt/halo, scanlines)
2. motion distortion (heat haze, warp)
3. glitch/impact (datamosh, blocks)
4. specialty warps (droste/kaleidoscope) with opacity controls

## Master intensity

If your build includes **Master Intensity**, it should:
- multiply every enabled effect’s intensity
- act as a global “panic knob” for creators

## Tiling and offset

If an effect exposes **Tiling** and **Offset**, it should change the sampled texture’s UVs.

If you adjust tiling/offset and see no change:
- the control is not wired to sampling (see [Troubleshooting](troubleshooting.md#tilingoffset-sliders-do-nothing))

## Comfort and safety

Avoid rapid full-screen strobe.
If an effect is driven by high-frequency bands:
- use smoothing / limiters
- keep intensity conservative for public instances
