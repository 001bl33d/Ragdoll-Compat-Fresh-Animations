# Ragdoll Compat: Fresh Animations

Version 1.0.0 — Minecraft 1.21.1 / NeoForge — client-side addon.

Keeps mob ragdolls intact when using Sable ragdolls with Fresh Animations and EMF.
Ragdolls use independent vanilla models and original Minecraft base textures.
Living mobs retain their resource-pack animations, including after recovery.
Player ragdolls are outside this addon's scope.

## Installation

1. Close Minecraft.
2. Remove any earlier mob-ragdoll-emf-compat test addon. Install only one version.
3. Add `ragdoll-compat-fresh-animations-neoforge-1.21.1-1.0.0.jar` to your client mods folder.
4. Keep the original dependency mods and resource packs installed and enabled.
5. Test newly spawned mobs; existing ragdolls can retain previously captured geometry.

This addon supplements the original mods; it does not replace them. Keep it off a dedicated server.
Remove this addon to uninstall. No configuration changes are required.

## Compatibility

- Minecraft 1.21.1; Java 21; NeoForge 21.1.x.
- Sable Player Ragdoll **0.7.5** and Entity Model Features **3.3.12** are required and version-pinned.
- Keep their dependencies, including Sable and Entity Texture Features, installed.
- Validated setup: NeoForge 21.1.264, Sable 2.0.6, ETF 7.2.6, Ragdoll Reactions 0.7.0,
  Ragdoll Corpse 0.3.0, and Fresh Animations 1.11.
- Original player patch 1.9.1 was also present in the user's profile; this addon adds no player hooks.
- NeoForge supplies MixinExtras (0.5.5 in the validated profile).

## Known limitations

A brief visible model change can occur when entering or leaving ragdoll. This release
preserves the working Test 2 behavior; transition smoothing is not included.
Unusual modded model constructors may fall back to their original models and log a warning.
Not every mob, resource pack or equipment layer has been tested. Original base textures
are used for Minecraft mobs; this is not a universal bypass for every third-party renderer.

## Validation

The user confirmed Test 2 works in-game, with the brief transition noted above.
Release 1.0.0 changes naming, metadata, icon and packaging only; rendering logic is unchanged.
Java 21 compilation and injection-target checks passed. A fresh release startup test is not claimed.

## Credits and license

See CREDITS.md, LICENSE and ARTWORK.md. This is an independent community addon, not an
official release of Sable, Fresh Animations, EMF, NeoForge or Minecraft.
Original dependency jars, Fresh Animations assets and Minecraft assets are not bundled.
Minecraft base textures are read from the user's installation at runtime.
