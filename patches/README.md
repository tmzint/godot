# PATCHES

The following patches add:
* a post light composition shader hook that allows for more stylized lighting.
* a fix for texture alpha of a transparent viewport always being 1.0 in shaders
* away to force TEXTURE_USAGE_STORAGE_BIT for the color buffer of viewports when using the mobile renderer
* port of automatic instancing from the clustered forward render to the forward mobile render

based on:
* https://github.com/godotengine/godot/pull/113200
  - https://github.com/godotengine/godot/commit/147c9faf556597786d6dfdbdb3666fb33a7c534e
  - https://github.com/godotengine/godot/commit/3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0
* https://github.com/godotengine/godot/issues/78207
  - https://github.com/godotengine/godot/pull/119321
* https://github.com/godotengine/godot/issues/96737
* https://github.com/godotengine/godot/pull/111511

Order:
* [147c9faf556597786d6dfdbdb3666fb33a7c534e.patch](147c9faf556597786d6dfdbdb3666fb33a7c534e.patch)
* [3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0.patch](3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0.patch)
* [69e6cb6593861f4c1c87dbea499fd0838f7522c5.patch](69e6cb6593861f4c1c87dbea499fd0838f7522c5.patch)
* [add_use_color_storage_flag_to_viewports.patch](add_use_color_storage_flag_to_viewports.patch)
* (OPTIONAL: SIMPLE TEST DID NOT IMPROVE PERFORMANCE) [automatic_instancing_mobile.patch](automatic_instancing_mobile.patch)

## Building:

Strip build: `scons platform=linuxbsd production=yes target=editor`
Debug build: `scons platform=linuxbsd production=yes target=editor debug_symbols=yes`

Output at `[godot.linuxbsd.editor.x86_64](../bin/godot.linuxbsd.editor.x86_64)`

see https://docs.godotengine.org/en/latest/engine_details/development/compiling/compiling_for_linuxbsd.html
