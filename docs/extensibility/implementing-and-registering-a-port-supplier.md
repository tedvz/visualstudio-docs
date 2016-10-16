---
title: "Implementing and Registering a Port Supplier"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "debugging [Debugging SDK], registering port suppliers"
  - "port suppliers, registering"
ms.assetid: fb057052-ee16-4272-8e16-a4da5dda0ad4
caps.latest.revision: 17
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Implementing and Registering a Port Supplier
The role of a port supplier is to track and supply ports, which in turn manage processes. At the time a port needs to be created, the port supplier is instantiated using CoCreate with the port supplier's GUID (the session debug manager [SDM] will use the port supplier the user selected or the port supplier specified by the project system). The SDM will then call [CanAddPort](../extensibility/idebugportsupplier2--canaddport.md) to see if any ports can be added. If a port can be added, a new port is requested by calling [AddPort](../extensibility/idebugportsupplier2--addport.md) and passing it an [IDebugPortRequest2](../extensibility/idebugportrequest2.md) that describes the port. `AddPort` will return a new port represented by an [IDebugPort2](../extensibility/idebugport2.md) interface.  
  
## Discussion  
 A port is created by a port supplier, which is in turn associated with a machine or debug server. A server can enumerate its port suppliers through the[EnumPortSuppliers](../extensibility/idebugcoreserver2--enumportsuppliers.md) method, and a port supplier can enumerate its ports through the [EnumPorts](../extensibility/idebugportsupplier2--enumports.md) method.  
  
 In addition to the typical COM registration, a port supplier must register itself with Visual Studio by placing its CLSID and name in specific registry locations. A Debugging SDK helper function called `SetMetric` handles this chore: it is called once for each item to be registered, thus:  
  
```cpp#  
SetMetric(metrictypePortSupplier,  
          <GUID of your port supplier>,  
          metricCLSID,  
          <CLSID of your port supplier>,  
          false,  
          NULL)  
SetMetric(metrictypePortSupplier,  
          <GUID of your port supplier>,  
          metricName,  
          <name of your port supplier>,  
          false,  
          NULL);  
```  
  
 A port supplier unregisters itself by calling `RemoveMetric` (another Debugging SDK helper function) once for each item that was registered, thus:  
  
```cpp#  
RemoveMetric(metrictypePortSupplier,  
             <GUID of your port supplier>,  
             metricCLSID,  
             NULL);  
RemoveMetric(metrictypePortSupplier,  
             <GUID of your port supplier>,  
             metricName,  
             NULL);  
```  
  
> [!NOTE]
>  The [SDK Helpers for Debugging](../extensibility/sdk-helpers-for-debugging.md)`SetMetric` and `RemoveMetric` are static functions defined in dbgmetric.h and compiled into ad2de.lib. The `metrictypePortSupplier`, `metricCLSID`, and `metricName` helpers are also defined in dbgmetric.h.  
  
 A port supplier can supply its name and GUID through the methods [GetPortSupplierName](../extensibility/idebugportsupplier2--getportsuppliername.md) and [GetPortSupplierId](../extensibility/idebugportsupplier2--getportsupplierid.md), respectively.  
  
## See Also  
 [Implementing a Port Supplier](../extensibility/implementing-a-port-supplier.md)   
 [SDK Helpers for Debugging](../extensibility/sdk-helpers-for-debugging.md)   
 [Port Suppliers](../extensibility/port-suppliers.md)