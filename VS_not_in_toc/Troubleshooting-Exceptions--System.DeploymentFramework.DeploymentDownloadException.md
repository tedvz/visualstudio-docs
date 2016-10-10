---
title: "Troubleshooting Exceptions: System.DeploymentFramework.DeploymentDownloadException"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55ec7af5-b1d1-4db2-8af8-3c708f521cc7
caps.latest.revision: 12
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
# Troubleshooting Exceptions: System.DeploymentFramework.DeploymentDownloadException
A `T:System.DeploymentFramework.DeploymentDownloadException` occurs if a network exception of any kind occurs when an application update is being downloaded.  
  
## Associated Tips  
 **Examine InnerException to determine the underlying System.Net or System.IO exception.**  
 This exception occurs whenever there is a network exception when an application update is being downloaded. Examine the exception's <xref:System.Exception.InnerException?qualifyHint=False> property to determine the underlying exception.  
  
## See Also  
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)