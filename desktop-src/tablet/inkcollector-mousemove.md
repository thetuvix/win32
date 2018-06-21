---
Description: Occurs when the mouse pointer is moved over the InkCollector or InkOverlay object.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: InkCollector.MouseMove event
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# InkCollector.MouseMove event

Occurs when the mouse pointer is moved over the [**InkCollector**](https://msdn.microsoft.com/en-us/library/ms695519(v=VS.85).aspx) or [**InkOverlay**](https://msdn.microsoft.com/en-us/library/ms698599(v=VS.85).aspx) object.

## Syntax


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## Parameters

<dl> <dt>

*Button* \[in\]
</dt> <dd>

The mouse button that was pressed.

</dd> <dt>

*Shift* \[in\]
</dt> <dd>

The state of the SHIFT key.

</dd> <dt>

*pX* \[in\]
</dt> <dd>

The x-coordinate, in pixels, of a mouse click.

</dd> <dt>

*pY* \[in\]
</dt> <dd>

The y-coordinate, in pixels, of a mouse click.

</dd> <dt>

*Cancel* \[in, out\]
</dt> <dd>

**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.

</dd> </dl>

## Return value

This event does not return a value.

## Remarks

> [!Note]  
> The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space. This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.

 

> [!Note]  
> Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events. Canceling some of these events may have unanticipated results.

 

This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.

## Requirements



|                                     |                                                                                                                     |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP Tablet PC Edition \[desktop apps only\]<br/>                                                       |
| Minimum supported server<br/> | None supported<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt> </dl> |
| Library<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## See also

<dl> <dt>

[**InkCollector Class**](https://msdn.microsoft.com/en-us/library/ms695519(v=VS.85).aspx)
</dt> <dt>

[**InkMouseButton Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 



