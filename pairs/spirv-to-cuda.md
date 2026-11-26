# CrossTL translation matrix: SPIR-V to CUDA

Measured on commit [`35ed8c7`](https://github.com/CrossGL/crosstl/commit/35ed8c7dc43264b625206cb6bf60d0858d205616) at 2026-11-25T11:13:42Z by the [Coverage workflow](https://github.com/CrossGL/crosstl/actions/workflows/coverage.yml). CrossTL translated each native SPIR-V probe whose feature CUDA has too straight to CUDA, and nvcc checked the result. It is compile-only. [COVERAGE.md](../COVERAGE.md#translation-matrix) describes the matrix and has every other cell.

Score 5.2 %: 13 supported, 0 refused, 236 wrong, 2 untested.

## Gaps

<details>
<summary>236 gaps: 0 refused, 236 wrong</summary>

Wrong, by cause:

- `ptxas probe.ptx, line N; fatal : Parsing error near '_': syntax error` (221): `Acos`, `Asin`, `Atan2`, `Ceil`, `Cos`, `Cosh`, `Exp`, `Exp2`, `FAbs`, `FMax`, `FMin`, `Floor`, `Fma`, `FrexpStruct`, `InverseSqrt`, `Ldexp`, `Log`, `Log2`, `ModfStruct`, `OpAtomicAnd`, `OpAtomicCompareExchange`, `OpAtomicExchange`, `OpAtomicIAdd`, `OpAtomicOr`, `OpAtomicUMax`, `OpAtomicUMin`, `OpAtomicXor`, `OpBitReverse`, `OpBitcast`, `OpIsInf`, `OpIsNan`, `OpMemoryBarrier`, `Pow`, `Round`, `RoundEven`, `Sin`, `Sinh`, `Sqrt`, `Tan`, `Tanh`, `Trunc`, `aggregate-equality`, `aggregate-inout-parameter`, `array`, `array-of-arrays`, `array-of-structs`, `array-parameter`, `barrier-in-loop`, `bitwise-logic`, `block-scope`, `bool-array`, `bool-conversion`, `boolean-logic`, `break`, `buffer-element-argument`, `buffer-in-helper`, `call-result-access`, `chained-assignment`, `chained-conditional`, `comma-operator`, `compound-assignment`, `compute`, `condition-assignment`, `conditional-expression`, `conditional-side-effect`, `const-local`, `const-parameter`, `constant-array-size`, `constant-expression`, `constant-struct`, `continue`, `control-attribute`, `default-only-switch`, `deferred-initialization`, `do-while-continue`, `do-while-loop`, `double`, `early-return`, `empty-statement`, `float-arithmetic`, `float-comparison`, `float-loop-counter`, `float-remainder`, `float-to-integer`, `for-loop`, `for-loop-variants`, `forward-declaration`, `function-call`, `function-overloading`, `global-constant`, `global-shadowing`, `half`, `if-else`, `implicit-conversion`, `increment-decrement`, `increment-in-index`, `indexed-compound-assignment`, `infinite-loop`, `inout-argument-lvalues`, `inout-parameter`, `int16`, `int64`, `int8`, `integer-arithmetic`, `integer-buffer`, `integer-division`, `integer-literal-limits`, `integer-promotion`, `integer-storage-image`, `integer-to-float`, `intrinsic-name`, `invocation-id-in-helper`, `literal-suffixes`, `local-invocation-id`, `local-invocation-index`, `local-struct`, `loop-condition-call`, `loop-counter-write`, `loop-in-switch`, `loop-return`, `lvalue-increment`, `multi-variable-loop`, `multiple-declarators`, `negation`, `nested-call`, `nested-loop`, `nested-member-assignment`, `nested-struct`, `nested-struct-buffer`, `nested-switch`, `nested-unary`, `num-workgroups`, `numeric-literals`, `octal-literal`, `operator-precedence`, `out-parameter`, `out-parameter-forwarding`, `read-only-buffer`, `read-write-image`, `reserved-identifier`, `reserved-member-name`, `reserved-type-name`, `restrict-buffer`, `sampled-texture`, `shared-2d-array`, `shared-memory`, `shared-memory-in-helper`, `shared-struct-array`, `shared-vector-array`, `short-circuit-logic`, `sibling-redeclaration`, `signed-comparison`, `signed-division`, `signed-shift`, `signed-to-unsigned`, `storage-image`, `storage-image-1d`, `storage-image-3d`, `storage-image-array`, `struct`, `struct-array-buffer`, `struct-array-member`, `struct-array-parameter`, `struct-buffer`, `struct-buffer-copy`, `struct-buffer-packing`, `struct-conditional`, `struct-constructor`, `struct-copy`, `struct-parameter`, `struct-return`, `struct-vector-member`, `switch`, `switch-case-scope`, `switch-default-position`, `switch-fallthrough`, `switch-in-loop`, `switch-return`, `texel-buffer`, `texture-1d`, `texture-1d-array`, `texture-2d-array`, `texture-3d`, `texture-argument`, `texture-cube`, `texture-cube-array`, `texture-in-helper`, `uint16`, `uint64`, `uint8`, `uniform-array`, `uniform-bool`, `uniform-buffer`, `uniform-integer`, `uniform-members`, `uniform-std140-array`, `uniform-std140-vector`, `uniform-struct-array`, `uniform-unsigned`, `uniform-vector-array`, `uniform-vector-packing`, `unorm-storage-image`, `unreachable-statement`, `unsigned-buffer`, `unsigned-comparison`, `unsigned-countdown`, `unsigned-division`, `unsigned-float-conversion`, `unsigned-negation`, `unsigned-shift`, `unsigned-switch`, `unsigned-wraparound`, `value-parameter-mutation`, `vector-array`, `vector-buffer`, `vector-conditional`, `void-return`, `volatile-buffer`, `while-loop`, `workgroup-id`, `workgroup-size`
- `expression must be a modifiable lvalue` (5): `array-initializer`, `constant-array`, `constant-vector-array`, `reserved-global-name`, `zero-initializer`
- `identifier "<feature>" is undefined in device code` (4): `num-subgroups`, `subgroup-id`, `subgroup-invocation-id`, `subgroup-size`
- `no instance of overloaded function "acosh" matches the argument list`: `Acosh`
- `no instance of overloaded function "asinh" matches the argument list`: `Asinh`
- `no instance of overloaded function "atanh" matches the argument list`: `Atanh`
- `no instance of overloaded function "fmax" matches the argument list`: `NMax`
- `no instance of overloaded function "fmin" matches the argument list`: `NMin`
- `no operator "=" matches these operands`: `OpBitCount`

</details>

<details>
<summary>2 untested: type 2</summary>

- `slangc or spirv-dis is not installed` (2): `pointer-arithmetic`, `pointer-local`

</details>
