# PATCHES

The following patches add:
* a post light composition shader hook that allows for more stylized lighting.
* a fix for texture alpha of a transparent viewport always being 1.0 in shaders

based on:
* https://github.com/godotengine/godot/pull/113200
  - https://github.com/godotengine/godot/commit/147c9faf556597786d6dfdbdb3666fb33a7c534e
  - https://github.com/godotengine/godot/commit/3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0
* https://github.com/godotengine/godot/issues/78207
  - https://github.com/godotengine/godot/pull/119321

Order:
* [147c9faf556597786d6dfdbdb3666fb33a7c534e.patch](147c9faf556597786d6dfdbdb3666fb33a7c534e.patch)
* [3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0.patch](3cdd6f6dec8cd20991dc5ace555dbc7ab14cfca0.patch)
* [69e6cb6593861f4c1c87dbea499fd0838f7522c5.patch](69e6cb6593861f4c1c87dbea499fd0838f7522c5.patch)

## Building:

Strip build: `scons platform=linuxbsd production=yes target=editor`
Debug build: `scons platform=linuxbsd production=yes target=editor debug_symbols=yes`

Output at `[godot.linuxbsd.editor.x86_64](../bin/godot.linuxbsd.editor.x86_64)`

see https://docs.godotengine.org/en/latest/engine_details/development/compiling/compiling_for_linuxbsd.html
