---
title: "Compiler Error C3532"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 51067853-eda8-4f59-86e8-8924e16d3a95
caps.latest.revision: 6
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
# Compiler Error C3532
'type': incorrect usage of 'auto'  
  
 The indicated type cannot be declared with the `auto` keyword. For example, you cannot use the `auto` keyword to declare an array or a method return type.  
  
### To correct this error  
  
1.  Ensure that the initialization expression yields a valid type.  
  
2.  Ensure that you do not declare an array or a method return type.  
  
## Example  
 The following example yields C3532 because the `auto` keyword cannot declare a method return type.  
  
```  
// C3532a.cpp  
// Compile with /Zc:auto  
auto f(){}   // C3532  
```  
  
## Example  
 The following example yields C3532 because the `auto` keyword cannot declare an array.  
  
```  
// C3532b.cpp  
// Compile with /Zc:auto  
int main()  
{  
   int x[5];  
   auto a[5];            // C3532  
   auto b[1][2];         // C3532  
   auto y[5] = x;        // C3532  
   auto z[] = {1, 2, 3}; // C3532  
   auto w[] = x;         // C3532  
   return 0;  
}  
```  
  
## See Also  
 [auto Keyword](../VS_visualcpp/auto-Keyword.md)