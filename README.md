# MF-Extras

# d3d8to9 — 60 FPS Limit Patch

This patch adds a **60 FPS frame rate limit** to `d3d8to9`.

## Changes

- Adds a `LimitFramerateTo60FPS()` function.
- Limits frames to approximately **60 FPS**.
- Applies the limit to:
  - `Direct3DDevice8::Present()`
  - `Direct3DSwapChain8::Present()`
- Uses high-precision Windows timing for consistent frame pacing.
- Adds the function declaration to `d3d8types.hpp`.
- Adds a Visual Studio `.vcxproj.user` file.

## Result

The game/application is limited to approximately **60 FPS** without changing the main Direct3D 8 → Direct3D 9 functionality.
