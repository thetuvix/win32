---
Description: To create a Direct3D device, first create a Direct3D object (see Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Creating a Device (Direct3D 9)
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Creating a Device (Direct3D 9)

To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/desktop/api)). All rendering devices created by a Direct3D object share the same physical resources. If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.

First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device. The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &amp;d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Next, create the Direct3D device. The following [**IDirect3D9::CreateDevice**](/windows/desktop/api) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &amp;d3dpp, &amp;d3dDevice ) ) )
    return E_FAIL;
```



Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.

After creating the device, set its state.

## Related topics

<dl> <dt>

[Direct3D Devices](direct3d-devices.md)
</dt> </dl>

 

 


