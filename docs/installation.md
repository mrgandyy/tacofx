# Installation

## Requirements

- Unity **Built-in Render Pipeline**
- VRChat SDK3 (Worlds)
- AudioLink (recommended, required for reactive features)

## Import

1. In Unity: **Assets → Import Package → Custom Package…**
2. Select the TacoFX Ultimate `.unitypackage`
3. Import everything (unless you know exactly what you’re excluding)

## Example prefabs

TacoFX includes example prefabs/materials for each shader family.

Recommended:
- Use the example prefab first
- Duplicate it
- Customize the duplicate

This keeps a known-good reference in your project.

## Common gotchas

- **URP/HDRP**: TacoFX is intended for Built-in RP. URP/HDRP projects often “work” but look incorrect or miss features.
- **Scene view vs game view**: some screen-space setups only show correctly in Play Mode / Game View.
- **Post-processing confusion**: TacoScreenFX is not Unity Post Processing Stack. It’s a shader rendered on a quad (different setup).

Next: [AudioLink setup](audiolink-setup.md)
