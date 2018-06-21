---
Description: Web Services on Devices API (WSDAPI) provides support for the Devices Profile for Web Services (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI Specification Compliance
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WSDAPI Specification Compliance

Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](http://go.microsoft.com/fwlink/p/?linkid=59069) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices. DPWS assembles basic WS specifications, such as [WS-Eventing](http://go.microsoft.com/fwlink/p/?linkid=96173), [WS-Discovery](http://go.microsoft.com/fwlink/p/?linkid=87841), and [WS-MetadataExchange](http://go.microsoft.com/fwlink/p/?linkid=95657), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices. This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.

The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](https://msdn.microsoft.com/en-us/library/ms735119(v=VS.85).aspx) or [WS-Management](http://go.microsoft.com/fwlink/p/?linkid=96673)).

The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI. These topics describe the implementation of WSDAPI relative to the underlying specifications. They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.

-   [DPWS Specification Compliance](dpws-specification-compliance.md)
-   [WS-Discovery Specification Compliance](ws-discovery-specification-compliance.md)
-   [WS-MetadataExchange and WS-Transfer Specification Compliance](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md)

## Related topics

<dl> <dt>

[WSD Device Development](wsd-device-development.md)
</dt> <dt>

[WSD Device Implementation Recommendations](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 


