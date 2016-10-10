---
title: "&#39;GoTo &lt;linelabel&gt;&#39; is not valid because &#39;&lt;linelabel&gt;&#39; is inside a &#39;Using&#39; statement that does not contain this statement"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ebec3cac-d378-4e9b-a792-12e9ece5599e
caps.latest.revision: 9
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
# &#39;GoTo &lt;linelabel&gt;&#39; is not valid because &#39;&lt;linelabel&gt;&#39; is inside a &#39;Using&#39; statement that does not contain this statement
A `GoTo` statement outside a `Using` construction attempts to branch to a line label inside the construction.  
  
 It is not valid to branch from anywhere outside a `Using`...`End Using` construction to anywhere inside the construction.  
  
 **Error ID:** BC36009  
  
### To correct this error  
  
-   Change the line label in the `GoTo` statement to a label that is not inside any `For`...`Next`, `For Each`...`Next`, `SyncLock`...`End SyncLock`, `Try`...`Catch`...`Finally`, `With`...`End With`, or `Using`...`End Using` construction.  
  
     -or-  
  
-   Remove the `GoTo` statement entirely. The only way you can enter a `Using`...`End Using` construction is to allow control to pass to the `Using` statement itself.  
  
## See Also  
 [GoTo Statement](../Topic/GoTo%20Statement.md)   
 [Using Statement](../Topic/Using%20Statement%20\(Visual%20Basic\).md)