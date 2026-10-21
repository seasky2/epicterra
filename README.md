# Epicterra

Epic Terrain terrain (0.1.4b) for Minecraft 1.21 / 1.21.1, without its biome list, so it works together with Terralith.

## How it works

Epic Terrain ships its own `dimension/overworld.json` (a full biome list), which conflicts with biome packs like Terralith: one always overrides the other. Epicterra is Epic Terrain with exactly that one file removed. It provides terrain only, and lets Terralith provide the biomes.

## Usage

1. Install [Terralith](https://modrinth.com/datapack/terralith) (tested with v2.5.8, newer versions work too)
2. Enable this pack **above** Terralith on the world creation datapack screen
3. Do not enable the original Epic Terrain pack at the same time
4. Recommended: [WorldgenFeatureFix](https://modrinth.com/mod/worldgenfeaturefix), which fixes the vanilla lake crash ([MC-273228](https://bugs.mojang.com/browse/MC-273228)) that the Epic Terrain author says affects 0.1.4a~b on 1.21

## Why not the official Epic Terrain Compatible

The newer [Epic Terrain Compatible](https://modrinth.com/datapack/epic-terrain_compatible) line solves the same conflict, but stacks 50 `cache_2d` nodes in its density functions, which crashes c2me OpenCL acceleration with `Cannot register more caches`. This pack uses only 18 cache like nodes and works fine with OpenCL enabled.

## Contents

```
epicterrain_0.1.4b_Beta_1.20.5~1.21.1.zip  minus  data/minecraft/dimension/overworld.json  =  epicterra-1.0.0.zip
```

Verified identical (same 85 files, same sizes) to a field tested hybrid build.

## Notes

- One terrain engine per world. Do not combine with Tectonic, Terratonic or other terrain packs
- Start a new world when changing packs. Do not swap terrain mid-world
- pack_format 15, supported_formats up to 48 (Minecraft 1.21 / 1.21.1)

## Credits and license

- [Epic Terrain](https://modrinth.com/datapack/epicterrain) by WonderfulAiChen, MIT license. Epicterra is a derivative (one file removed) redistributed under MIT with credit. Consider supporting the author!
- [Terralith](https://modrinth.com/datapack/terralith) by Stardust Labs, required separately under its own license. Not bundled here.
- Pack assembled by [seasky2](https://github.com/seasky2).
