---
title: "ICommandPropertiesImpl::GetProperties"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "ICommandPropertiesImpl::GetProperties"
  - "ICommandPropertiesImpl.GetProperties"
  - "GetProperties"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GetProperties method"
ms.assetid: 1bee5f1b-bd08-435a-956a-e4cebcdf5d5e
caps.latest.revision: 9
ms.author: "mblome"
manager: "ghogen"
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
# ICommandPropertiesImpl::GetProperties
Returns all the requested property sets using the command's property map.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetProperties)(   
   const ULONG cPropertyIDSets,   
   const DBPROPIDSET rgPropertyIDSets[],   
   ULONG * pcPropertySets,   
   DBPROPSET ** prgPropertySets    
);  
```  
  
#### Parameters  
 See [ICommandProperties::GetProperties](https://msdn.microsoft.com/en-us/library/ms723119.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 See [BEGIN_PROPSET_MAP](../data/begin_propset_map.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ICommandPropertiesImpl Class](../data/icommandpropertiesimpl-class.md)   
 [ICommandPropertiesImpl::SetProperties](../data/icommandpropertiesimpl--setproperties.md)