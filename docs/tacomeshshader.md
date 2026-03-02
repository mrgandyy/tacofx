# TacoMeshShader

TacoMeshShader is a mesh/surface shader family for props and environments, with optional vertex motion.

## When to use it

Great for:
- stage pieces, frames, portals
- walls/floors with reactive surface detail
- props that should “feel alive” in music

## Vertex motion vs surface motion

- **Surface motion**: UV animation, scrolling patterns, emissive pulses
- **Vertex motion**: actually moves the mesh vertices (requires enough vertex density)

If your mesh “breathes” as a whole:
- the displacement is likely uniform (one amplitude applied to all vertices)
- prefer position/UV-dependent displacement for wave-like motion (especially for TacoScape)

## Color + hue control

If your build includes:
- local Color A/B
- local hue shift toggle/speed

Use local hue shift when you want multiple effects to stack without fighting the global palette.

## Shape considerations

Some effects depend on:
- mesh UV quality
- vertex density
- object scale

If an effect looks great on a plane but bad on a sphere:
- that’s usually a UV/space assumption
- consider switching the effect’s coordinate mode (UV vs object vs world), if available
