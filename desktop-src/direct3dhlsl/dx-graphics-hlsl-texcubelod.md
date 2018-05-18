---
title: texCUBElod
description: Samples a cube texture with mipmaps. The mipmap LOD is specified in t.w.
ms.assetid: 'fa7b236d-2c52-42bd-9123-919541f9e675'
keywords: ["texCUBElod HLSL"]
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
---

# texCUBElod

Samples a cube texture with mipmaps. The mipmap LOD is specified in t.w.



| ret texCUBElod(s, t) |
|----------------------|



�

## Parameters



| Item                                                   | Description                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[in\] The sampler state.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[in\] The texture coordinate.<br/> |



�

## Return Value

The value of the texture data.

## Type Description



| Name | In/Out | [**Template Type**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Component Type**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md#component-and-template-types) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**vector**](dx-graphics-hlsl-intrinsic-functions.md#component-and-template-types) | [**float**](https://msdn.microsoft.com/library/windows/desktop/aa383751)                        | 4    |
| ret  | out    | [**vector**](dx-graphics-hlsl-intrinsic-functions.md#component-and-template-types) | [**float**](https://msdn.microsoft.com/library/windows/desktop/aa383751)                        | 4    |



�

## Minimum Shader Model

This function is supported in the following shader models.



| Shader Model                                              | Supported               |
|-----------------------------------------------------------|-------------------------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | yes (pixel shader only) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | yes (pixel shader only) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no                      |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                      |



�

## See also

<dl> <dt>

[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

�

�




