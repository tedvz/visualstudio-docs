---
title: "Compiler Error CS1002"
ms.custom: na
ms.date: 10/01/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 659b7abf-9311-40c9-9594-5372464c6148
caps.latest.revision: 7
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Compiler Error CS1002
; expected  
  
 The compiler detected a missing semicolon. A semicolon in required at the end of every statement in C#. A statement may span more than one line.  
  
 The following sample generates CS1002:  
  
```  
// CS1002.cs  
namespace x  
{  
   abstract public class clx  
   {  
      int i   // CS1002, missing semicolon  
  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```  
  
## See Also  
 [Statements](../Topic/Statements%20\(C%23%20Programming%20Guide\).md)