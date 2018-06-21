---
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navigating a Tree of Item Objects
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Navigating a Tree of Item Objects

> [!Note]  
> This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer. See [Windows Image Acquisition Automation Layer](http://msdn.microsoft.com/en-us/library/windows/desktop/ms630827.aspx).

 

An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device. Using this technique, an application selects and acquires an image without the use of a dialog box.

A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects. The child items in the tree represent folders and images for a camera or scan beds for a scanner.

After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.

Enumerate this collection (recursively, if necessary) to navigate item tree.

 

 


