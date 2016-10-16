---
title: "CA2120: Secure serialization constructors"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CA2120"
  - "SecureSerializationConstructors"
helpviewer_keywords: 
  - "SecureSerializationConstructors"
  - "CA2120"
ms.assetid: e9989da1-55a0-43f8-9aa9-da86afae3b41
caps.latest.revision: 16
ms.author: "douge"
manager: "douge"
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
# CA2120: Secure serialization constructors
|||  
|-|-|  
|TypeName|SecureSerializationConstructors|  
|CheckId|CA2120|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 The type implements the \<xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> interface, is not a delegate or interface, and is declared in an assembly that allows partially trusted callers. The type has a constructor that takes a \<xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> object and a \<xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> object (the signature of the serialization constructor). This constructor is not secured by a security check, but one or more of the regular constructors in the type is secured.  
  
## Rule Description  
 This rule is relevant for types that support custom serialization. A type supports custom serialization if it implements the \<xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> interface. The serialization constructor is required and is used to de-serialize, or re-create objects that have been serialized using the \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*?displayProperty=fullName> method. Because the serialization constructor allocates and initializes objects, security checks that are present on regular constructors must also be present on the serialization constructor. If you violate this rule, callers that could not otherwise create an instance could use the serialization constructor to do this.  
  
## How to Fix Violations  
 To fix a violation of this rule, protect the serialization constructor with security demands that are identical to those protecting other constructors.  
  
## When to Suppress Warnings  
 Do not suppress a violation of the rule.  
  
## Example  
 The following example shows a type that violates the rule.  
  
 [!code[FxCop.Security.SerialCtors#1](../codequality/codesnippet/CSharp/ca2120--secure-serialization-constructors_1.cs)]  
  
## Related Rules  
 [CA2229: Implement serialization constructors](../codequality/ca2229--implement-serialization-constructors.md)  
  
 [CA2237: Mark ISerializable types with SerializableAttribute](../codequality/ca2237--mark-iserializable-types-with-serializableattribute.md)  
  
## See Also  
 \<xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName>   
 \<xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>   
 \<xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>