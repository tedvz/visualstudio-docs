---
title: "Compiler Error CS1526"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1526"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1526"
ms.assetid: 92feeb9f-e577-4c08-b12b-c19822857200
caps.latest.revision: 9
ms.author: "billchi"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Compiler Error CS1526
A new expression requires (), [], or {} after type  
  
 The [new](../Topic/new%20\(C%23%20Reference\).md) operator, used to dynamically allocate memory for an object, was not specified correctly.  
  
## Example  
 The following sample shows how to use `new` to allocate space for an array and an object.  
  
```  
// CS1526.cs  
public class y  
{  
   public static int i = 0;  
   public int myi = 0;  
}  
  
public class z  
{  
   public static void Main()  
   {  
      y py = new y;   // CS1526  
      y[] aoys = new y[10];   // Array of Ys  
  
      for (int i = 0; i < aoys.Length; i++)  
         aoys[i] = new y();   // an object of type y  
   }  
}  
```