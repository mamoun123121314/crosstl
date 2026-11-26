<!-- Written from coverage.json by tools/coverage/docs.py when the Coverage workflow publishes. Do not edit. -->

# HLSL

Measured on commit [`52c8879`](https://github.com/CrossGL/crosstl/commit/52c8879d0a023f757943283413208e345a54f854) at 2026-11-26T04:55:56Z (CrossTL 3.9.0) by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). The Coverage workflow writes this page from `coverage.json` each time it publishes; [COVERAGE.md](../COVERAGE.md) defines each outcome. Score = supported / (supported + refused + wrong).

The [backend guide](https://github.com/CrossGL/crosstl/blob/main/docs/source/backends/directx.rst) describes how CrossTL translates HLSL.

| Direction | Score | Supported | Refused | Wrong | Untested | Executed | Reference tool |
|---|---:|---:|---:|---:|---:|---|---|
| output | 100.0 % | 831 | 0 | 0 | 0 | 530 on d3d12-warp, 359 on vulkan-lavapipe | dxc (libdxcompiler.so: 1.9(5191-d355aa83)(1.9.0.5191)) |
| input | 100.0 % | 831 | 0 | 0 | 0 | 531 on d3d12-warp, 360 on vulkan-lavapipe | dxc (libdxcompiler.so: 1.9(5191-d355aa83)(1.9.0.5191)) |

## Feature lists

- [DXC v1.9.2602.24 intrinsic table](https://github.com/microsoft/DirectXShaderCompiler/blob/d355aa8364d34df3f0822ba0de8d1dfc75ae6f48/utils/hct/gen_intrin_main.txt), pinned at `d355aa8364d3`
- [DXC v1.10.2605.37 (Shader Model 6.10 preview) intrinsic table](https://github.com/microsoft/DirectXShaderCompiler/blob/c4d8f4f99aa221da58cd540bf2099a2889632ab6/utils/hct/gen_intrin_main.txt), pinned at `c4d8f4f99aa2`

## By category

Each cell counts the supported features of a category over its supported, refused and wrong ones.

| Category | output | input |
|---|---:|---:|
| compute | 13/13 | 13/13 |
| control-flow | 62/62 | 62/62 |
| function | 205/205 | 205/205 |
| graphics | 63/63 | 63/63 |
| method | 291/291 | 291/291 |
| operator | 50/50 | 50/50 |
| resource | 67/67 | 67/67 |
| stage | 14/14 | 14/14 |
| type | 66/66 | 66/66 |

## Translation pairs

The cells of the translation matrix that translate HLSL straight to another language or another language straight to it, measured on commit [`35ed8c7`](https://github.com/CrossGL/crosstl/commit/35ed8c7dc43264b625206cb6bf60d0858d205616) at 2026-11-25T11:13:42Z. Each cell measures the features of the source's input row that the target has too, and its page lists the gaps.

| Source | Target | Score | Supported | Refused | Wrong | Untested | Executed |
|---|---|---:|---:|---:|---:|---:|---|
| HLSL | CUDA | [95.4 %](../pairs/hlsl-to-cuda.md) | 229 | 7 | 4 | 0 | compile-only |
| HLSL | GLSL ES | [88.2 %](../pairs/hlsl-to-gles.md) | 352 | 24 | 23 | 7 | compile-only |
| HLSL | GLSL | [94.8 %](../pairs/hlsl-to-glsl.md) | 421 | 20 | 3 | 0 | yes |
| HLSL | HIP | [95.4 %](../pairs/hlsl-to-hip.md) | 230 | 7 | 4 | 0 | compile-only |
| HLSL | Metal | [96.3 %](../pairs/hlsl-to-metal.md) | 368 | 8 | 6 | 0 | compile-only |
| HLSL | Mojo | [0.0 %](../pairs/hlsl-to-mojo.md) | 0 | 13 | 204 | 0 | compile-only |
| HLSL | Rust | [46.2 %](../pairs/hlsl-to-rust.md) | 255 | 289 | 8 | 0 | yes |
| HLSL | Slang | [96.0 %](../pairs/hlsl-to-slang.md) | 499 | 11 | 10 | 0 | yes |
| HLSL | SPIR-V | [93.8 %](../pairs/hlsl-to-spirv.md) | 423 | 20 | 8 | 0 | yes |
| HLSL | WebGL | [73.3 %](../pairs/hlsl-to-webgl.md) | 11 | 4 | 0 | 0 | compile-only |
| HLSL | WGSL | [87.2 %](../pairs/hlsl-to-wgsl.md) | 395 | 54 | 4 | 1 | yes |
| CUDA | HLSL | [94.7 %](../pairs/cuda-to-hlsl.md) | 251 | 9 | 5 | 0 | compile-only |
| GLSL | HLSL | [94.9 %](../pairs/glsl-to-hlsl.md) | 408 | 12 | 10 | 0 | yes |
| HIP | HLSL | [94.4 %](../pairs/hip-to-hlsl.md) | 251 | 8 | 7 | 0 | compile-only |
| Metal | HLSL | [92.0 %](../pairs/metal-to-hlsl.md) | 358 | 12 | 19 | 0 | compile-only |
| Mojo | HLSL | [0.0 %](../pairs/mojo-to-hlsl.md) | 0 | 217 | 0 | 0 | compile-only |
| Rust | HLSL | [48.0 %](../pairs/rust-to-hlsl.md) | 239 | 164 | 95 | 0 | yes |
| Slang | HLSL | [90.8 %](../pairs/slang-to-hlsl.md) | 483 | 22 | 27 | 0 | yes |
| SPIR-V | HLSL | [93.3 %](../pairs/spirv-to-hlsl.md) | 404 | 19 | 10 | 0 | yes |
| WebGL | HLSL | [99.6 %](../pairs/webgl-to-hlsl.md) | 256 | 0 | 1 | 0 | compile-only |
