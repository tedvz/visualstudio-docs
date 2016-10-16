---
title: "Content Definition Dialog Box"
ms.custom: na
ms.date: "10/04/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "MessageContent.UI"
ms.assetid: 7e4237c3-90a1-4149-bd8a-3643d1dde0df
caps.latest.revision: 3
ms.author: "erikre"
manager: "erikre"
translation.priority.ht: 
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
# Content Definition Dialog Box
The **Content Definition** dialog box is used in [!INCLUDE[wfd1](../workflowdesigner/includes/wfd1_md.md)] to configure the **Content** properties of the \<xref:System.ServiceModel.Activities.Send>, \<xref:System.ServiceModel.Activities.Receive>, \<xref:System.ServiceModel.Activities.SendReply>, and \<xref:System.ServiceModel.Activities.ReceiveReply> activities. [!INCLUDE[crabout](../codequality/includes/crabout_md.md)] the activity designers that use this box, see the [Send](../workflowdesigner/send-activity-designer.md), [Receive](../workflowdesigner/receive-activity-designer.md), [ReceiveAndSendReply](../workflowdesigner/receiveandsendreply-template-designer.md), and [SendAndReceiveReply](../workflowdesigner/sendandreceivereply-template-designer.md) topics.  
  
 The following table describes the user interface (UI) elements of the **Initialize Correlation** dialog box.  
  
|UI Element|Description|  
|----------------|-----------------|  
|**Message**|Specifies the message content with the **Message data** expression text box and the type by using the **Message type** drop-down list box. By default, the **Content Definition** uses the \<xref:System.ServiceModel.Activities.ReceiveMessageContent>, which expects a \<xref:System.ServiceModel.Channels.Message> or a message contract type within the workflow service definition.|  
|**Parameters**|Click the **Parameters** radio button to use \<xref:System.ServiceModel.Activities.ReceiveParametersContent>, which expects a data contract. Use the data grid to set a generic collection of \<xref:System.Activities.OutArgument> key/value pairs whose values are assigned to variable parameters in the current workflow.|  
  
 The **Content Definition** dialog box is used by the **Send**, **Receive**, **ReceiveAndSendReply**, and **SendAndReceiveReply** designers. Accessing them is similar in each case and the Receive case is used here to illustrate the procedure.  
  
 The **Receive** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] surface wherever activities are usually placed. This creates a \<xref:System.ServiceModel.Activities.Receive> activity with a default \<xref:System.Activities.Activity.DisplayName*> of Receive. Select the **Receive** activity designer and click the ellipsis button next to the (Content) text for the **Content** property in the property grid for the **Content Definition** dialog box to appear.  
  
 The content can be specified within the **Message** section for a \<xref:System.ServiceModel.Activities.ReceiveMessageContent> activity or within the **Parameter** section for a \<xref:System.ServiceModel.Activities.ReceiveParametersContent> activity.  
  
## See Also  
 [Workflow Designer UI Help](../workflowdesigner/workflow-designer-ui-help.md)