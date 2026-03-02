# Performance guide

TacoFX can look wild without being irresponsible, but stacking and vertex motion can add up. This guide focuses on practical tuning.

## What usually costs the most

1. **Full-screen effects** (TacoScreenFX)
   - cost scales with screen resolution
   - heavy warps/glitches cost more than subtle overlays

2. **Raymarch/volume looks** (DepthFX)
   - cost scales with step count / complexity
   - be conservative in public instances

3. **Vertex displacement** (TacoMeshShader / TacoScape)
   - cost scales with vertex count
   - dense dance floors look great but can be expensive

## Safe stacking recommendations

- Start with 1–2 subtle ScreenFX overlays
- Add 1 “hero” warp/glitch, then stop
- Prefer per-effect opacity controls to prevent over-warping
- If you use treble-driven motion, add smoothing/limiting

## Debug checklist

- Profile in Unity + test in VRChat
- Test with a full instance (worst case)
- Provide an in-world “panic off” (global intensity to 0 / disable all)
