---
Description: A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: ID3DXEffectStateManager::SetNPatchMode method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXEffectStateManager::SetNPatchMode method

A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.

## Syntax


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## Parameters

<dl> <dt>

*nSegments* \[in\]
</dt> <dd>

Type: **[**FLOAT**](https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx)**

Break the surface into this number of subdivisions. This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/desktop/api).

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/en-us/library/Bb401631(v=MSDN.10).aspx)**

The user-implemented method should return S\_OK. If the callback fails when setting the device state, either of the following will occur:

-   The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/desktop/api)) will fail.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 



