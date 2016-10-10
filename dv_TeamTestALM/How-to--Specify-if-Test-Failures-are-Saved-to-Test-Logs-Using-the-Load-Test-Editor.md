---
title: "How to: Specify if Test Failures are Saved to Test Logs Using the Load Test Editor"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08a7fe98-a7f7-4b8d-94a3-ec82b65a2aaf
caps.latest.revision: 28
manager: douge
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
# How to: Specify if Test Failures are Saved to Test Logs Using the Load Test Editor
After you create your load test with the **New Load Test Wizard**, you can use the **Load Test Editor** to change the load test properties to meet your testing needs and goals. See [Creating load tests](../Topic/Creating%20load%20tests.md).  
  
> [!NOTE]
>  For a complete list of the run settings properties and their descriptions, see [Load Test Run Settings Properties](../dv_TeamTestALM/Load-Test-Run-Settings-Properties.md).  
  
 You can specify if you want to have the test log saved if a test fails in a load test by using the Load Test Editor to change the **Save Log on Test Failure** property in the Properties window.  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
### To specify if the test log is saved when a test fails in a scenario  
  
1.  Open a load test.  
  
     The Load Test Editor appears. The load test tree is displayed.  
  
2.  In the load test trees **Run Settings** folder, choose the run settings node that you want to specify the maximum number of test iterations for.  
  
3.  On the **View** menu, select **Properties Window**.  
  
     The run settings categories and properties are displayed in the Properties window.  
  
4.  In the **Save Log on Test Failure** property, select either True or False to specify if you want to save the test log in the event of a test failure in the scenario.  
  
     After you have finished changing the property, choose **Save** on the **File** menu.  
  
     The data that is saved in the log can be viewed using the Load Test Analyzer's Tables view. For more information, see [Analyzing Load Test Results and Errors in the Tables View](../dv_TeamTestALM/Analyzing-Load-Test-Results-and-Errors-in-the-Tables-View-of-the-Load-Test-Analyzer.md) and [Load Test Analyzer Overview](../dv_TeamTestALM/Load-Test-Analyzer-Overview.md).  
  
## See Also  
 [Editing Load Test Scenarios](../dv_TeamTestALM/Editing-Load-Test-Scenarios-Using-the-Load-Test-Editor.md)   
 [Creating load tests](../Topic/Creating%20load%20tests.md)   
 [Editing Load Test Scenarios](../dv_TeamTestALM/Editing-Load-Test-Scenarios-Using-the-Load-Test-Editor.md)   
 [How to: Configure Collecting Full Details to Enable the Virtual User Activity Chart](../dv_TeamTestALM/How-to--Configure-Load-Tests-to-Collect-Full-Details-to-Enable-Virtual-User-Activity-in-Test-Results.md)   
 [How to: Specify How Frequently Test Logs are Saved](../dv_TeamTestALM/How-to--Specify-How-Frequently-Test-Logs-are-Saved-Using-the-Load-Test-Editor.md)