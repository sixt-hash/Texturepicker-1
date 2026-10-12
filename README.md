# Texture Picker (Fabric, Minecraft 1.21.1)

Press **K** in game (rebindable under Controls > Texture Picker) to open the picker.

1. Search for a block or item texture (e.g. `stone`, `diamond_sword`).
   Only textures that exist in 2+ of your enabled packs are listed.
2. Click it to see every pack's version side by side with a preview.
3. Click the pack you want. Resources reload and that texture now comes from that pack.
   "Use default" removes your choice again.

Choices are saved in `config/texturepicker.json`.

## Build
You need JDK 21. Easiest way to get the Gradle wrapper: copy `gradlew`, `gradlew.bat`
and the `gradle/` folder from https://github.com/FabricMC/fabric-example-mod
into this folder, then run:

    ./gradlew build

The mod jar appears in `build/libs/` (use the one without `-sources`).
Put it in your `mods` folder together with Fabric Loader 0.16+ and Fabric API for 1.21.1.

## Limits
- Block and item textures only (entity textures not included yet).
- Only the first 9 packs (highest priority first) are shown per texture.
- Overrides apply to the PNG; animation .mcmeta files come from the same chosen pack.
