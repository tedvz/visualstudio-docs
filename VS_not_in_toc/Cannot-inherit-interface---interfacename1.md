---
title: "Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; from which the interface &#39;&lt;interfacename4&gt;&#39; inherits for some type arguments"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64a66ec7-0f5f-4804-a92b-9a6279fdfd6d
caps.latest.revision: 5
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
# Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; from which the interface &#39;&lt;interfacename4&gt;&#39; inherits for some type arguments
A generic interface inherits from two or more generic interfaces, and two of the inheritances could conflict for certain values of type arguments.  
  
 The following statements can generate this error.  
  
```  
Public Interface interfaceA(Of u)  
End Interface  
Public Interface interfaceX(Of v)  
    Inherits interfaceA(Of v)  
End Interface  
Public Interface interfaceY(Of w)  
    Inherits interfaceA(Of w)  
End Interface  
Public Interface derivedInterface(Of t1, t2)  
    Inherits interfaceX(Of t1), interfaceY(Of t2)  
End Interface  
```  
  
 If `derivedInterface` is constructed or implemented supplying the same type to both `t1` and `t2`, it must inherit two versions of `interfaceA` with identical type arguments. Doing so would produce an ambiguity about which version to access.  
  
 **Error ID:** BC32122  
  
### To correct this error  
  
-   Change one of the type arguments supplied to the derived interface so that there is no conflict.  
  
     -or-  
  
-   Remove from the `Inherits` statement one of the interfaces causing the potential inheritance or implementation conflict.  
  
## See Also  
 [NOT IN BUILD: Interfaces Overview](assetId:///f96bb470-c1b8-4c73-89bc-6f536b798da1)   
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)   
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)