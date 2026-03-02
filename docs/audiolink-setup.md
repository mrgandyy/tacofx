# AudioLink setup

## What is AudioLink?

AudioLink is a VRChat community standard that provides real-time audio analysis to shaders using a texture. TacoFX samples that texture to drive intensity, motion, and timing.

## Install AudioLink (worlds)

1. Import the AudioLink package into your project.
2. Add the AudioLink prefab to your scene (usually near world root).
3. Enter Play Mode and confirm AudioLink is running.

## How TacoFX uses AudioLink

TacoFX effects generally support:
- **Global band selection**: a project-wide “default band”
- **Per-effect band override**: (if implemented in your build) lets one effect hit on bass while another hits on highs

If an effect includes an **Audio Smoothing** control:
- raise smoothing to reduce flicker
- prefer smoothing for sharp/high-frequency bands

## Troubleshooting AudioLink

If nothing reacts:
- Confirm AudioLink prefab exists in the scene
- Confirm the world audio is playing
- Test with an obvious band (bass) and higher intensity
- See [Troubleshooting](troubleshooting.md#audiolink-not-reacting)
