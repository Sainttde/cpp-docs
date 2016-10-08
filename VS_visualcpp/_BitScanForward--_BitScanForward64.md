---
title: "_BitScanForward, _BitScanForward64"
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
ms.topic: article
ms.assetid: 405e60fb-0815-42a7-9b02-6fc035122203
caps.latest.revision: 12
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
# _BitScanForward, _BitScanForward64
**Microsoft Specific**  
  
 Search the mask data from least significant bit (LSB) to the most significant bit (MSB) for a set bit (1).  
  
## Syntax  
  
```  
unsigned char _BitScanForward(  
   unsigned long * Index,  
   unsigned long Mask  
);  
unsigned char _BitScanForward64(  
   unsigned long * Index,  
   unsigned __int64 Mask  
);  
```  
  
#### Parameters  
 [out] `Index`  
 Loaded with the bit position of the first set bit (1) found.  
  
 [in] `Mask`  
 The 32-bit or 64-bit value to search.  
  
## Return Value  
 0 if the mask is zero; nonzero otherwise.  
  
## Remarks  
 If a set bit is found, the bit position of the first set bit found is returned in the first parameter. If no set bit is found, 0 is returned; otherwise, 1 is returned.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_BitScanForward`|x86, ARM, x64|  
|`_BitScanForward64`|ARM, x64|  
  
 **Header file** <intrin.h>  
  
## Example  
  
```  
// BitScanForward.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(_BitScanForward)  
  
int main()  
{  
   unsigned long mask = 0x1000;  
   unsigned long index;  
   unsigned char isNonzero;  
  
   cout << "Enter a positive integer as the mask: " << flush;  
   cin >> mask;  
   isNonzero = _BitScanForward(&index, mask);  
   if (isNonzero)  
   {  
      cout << "Mask: " << mask << " Index: " << index << endl;  
   }  
   else  
   {  
      cout << "No set bits found.  Mask is zero." << endl;  
   }  
}  
```  
  
## Input  
  
```  
12  
```  
  
## Sample Output  
  
```  
Enter a positive integer as the mask:   
Mask: 12 Index: 2  
```  
  
### END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../VS_visualcpp/Compiler-Intrinsics.md)