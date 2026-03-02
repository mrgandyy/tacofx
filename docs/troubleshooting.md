# Troubleshooting

Work top-to-bottom. Most issues are setup or material configuration.

## AudioLink not reacting

- Confirm AudioLink prefab exists in the scene
- Confirm world audio is playing
- Increase effect intensity temporarily
- Test bass band first
- Verify you’re in Play Mode / Game View for screen-space setups

## Tiling/offset sliders do nothing

Symptoms:
- You change tiling/offset, but the texture pattern never changes.

Cause:
- UV transforms are not applied to the sampler UVs.

Fix:
- Ensure the shader uses `uv = uv * tiling + offset` (or Unity `_ST` style) before sampling.

## Uniform mesh motion (breathing)

Symptoms:
- The whole object scales up/down or lifts uniformly.

Cause:
- displacement uses one global scalar (single AudioLink sample) applied to all vertices.

Fix:
- use position/UV-dependent displacement (waves/noise field)
- normalize by bounds/scale so it behaves consistently across meshes

## Violent flicker / strobe

Symptoms:
- sharp flashes, uncomfortable motion, “epileptic” behavior.

Fix:
- add smoothing / attack-release
- clamp max per-frame change
- avoid treble bands for full-screen flashes
- reduce contrast/intensity

## Clipping into floors

Symptoms:
- an effect intersects the ground plane or clips at the base.

Fix:
- add height bias / ground offset
- clamp displacement near base using local position or a mask
