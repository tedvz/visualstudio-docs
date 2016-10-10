---
title: "Class &#39;&lt;classname&gt;&#39; must either be declared &#39;MustInherit&#39; or override the following inherited &#39;MustOverride&#39; member(s): &lt;membername(s)&gt;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7fba7a3b-c918-44ba-ae85-20312615c1ce
caps.latest.revision: 8
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
# Class &#39;&lt;classname&gt;&#39; must either be declared &#39;MustInherit&#39; or override the following inherited &#39;MustOverride&#39; member(s): &lt;membername(s)&gt;
Classes derived from base classes that contain `MustOverride` members must either override such members or use the `MustInherit` modifier.  
  
 **Error ID:** BC30610  
  
### To correct this error  
  
-   Add the `MustInherit` modifier to the class definition.  
  
-   Declare an override using the `Overrides` keyword.  
  
## See Also  
 [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Inheritance in Visual Basic](assetId:///e5e6e240-ed31-4657-820c-079b7c79313c)