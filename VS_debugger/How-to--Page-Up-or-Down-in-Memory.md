---
title: "How to: Page Up or Down in Memory"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 50b30a68-66f6-43f8-a48b-59ce12c95471
caps.latest.revision: 18
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# How to: Page Up or Down in Memory
When you view memory contents in a **Memory** window or the **Disassembly** window, you can use the vertical scrollbar to move up or down in the memory space.  
  
### To page up or down in memory  
  
1.  To page down (move to a higher memory address), click the vertical scrollbar below the scroll box.  
  
2.  To page up (move to a lower memory address), click the vertical scrollbar above the thumb.  
  
 You will also notice that the vertical scrollbar operates in a nonstandard manner. The address space of a modern computer is very large, and it would be easy to get lost by grabbing the scrollbar thumb and dragging it to a random location. For this reason, the thumb is "springloaded" and always remains in the center of the scrollbar. In native code applications, you can page up or down, but cannot scroll about freely.  
  
 In managed applications, disassembly is limited to one function and you can scroll normally.  
  
 You will notice that the higher addresses appear at the bottom of the window. To view a higher address, you must move down, not up.  
  
#### To move up or down one instruction  
  
-   Click the arrow at the top or bottom of the vertical scrollbar.  
  
## See Also  
 [Memory Windows](../VS_debugger/Memory-Windows.md)   
 [How to: Use the Disassembly Window](../VS_debugger/How-to--Use-the-Disassembly-Window.md)   
 [Viewing Data in the Debugger](../VS_debugger/Viewing-Data-in-the-Debugger.md)