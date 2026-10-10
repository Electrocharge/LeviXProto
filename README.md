# LeviXProto

Android package: `org.levixproto.hax`

This repo builds [LiteLDev/LeviLaunchroid](https://github.com/LiteLDev/LeviLaunchroid) (Apache-2.0) with a new application id. GitHub Actions checks out that launcher, applies `patches/levixproto.patch`, and compiles the native preloader with **NDK r28c**.

Pinned upstream commit: `a2e3fa22192d431531591578dfa5823327d48355`

Native pieces Actions builds:

- `app/src/main/cpp/CMakeLists.txt`
- submodule `app/src/main/cpp/preloader` (`LiteLDev/preloader-android`)
- submodule `app/src/main/cpp/libHttpClient`

The Java/Kotlin namespace stays `org.levimc.launcher` so upstream sources still compile. Android installs the app as `org.levixproto.hax`.

## Download the APK

After a green run on `main`, open **Actions → Android CI → the run → Artifacts → LeviXProto-debug**.

## Launching Minecraft

Same as LeviLaunchroid: import your own official Minecraft: Bedrock APK inside the app, then press Launch. This repo does not bundle Minecraft.

## Not included

ProtoHax packet / multiplayer cheat modules are not part of this build.
