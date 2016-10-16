---
title: "IDebugModule2::GetInfo"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "IDebugModule2::GetInfo"
helpviewer_keywords: 
  - "GetInfo method"
  - "IDebugModule2::GetInfo method"
ms.assetid: de337e66-294f-4ac9-b21e-71fac7418e36
caps.latest.revision: 10
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# IDebugModule2::GetInfo
Gets information about this module.  
  
## Syntax  
  
```cpp#  
HRESULT GetInfo(   
   MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO*       pInfo  
);  
```  
  
```cpp#  
int GetInfo(   
   enum_MODULE_INFO_FIELDS dwFields,  
   MODULE_INFO[]           pInfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [MODULE_INFO_FIELDS](../extensibility/module_info_fields.md) enumeration that specify which fields of `pInfo` are to be filled out.  
  
 `pInfo`  
 [in, out] A [MODULE_INFO](../extensibility/module_info.md) structure that is filled in with a description of the module.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The [MODULE_INFO](../extensibility/module_info.md) structure contains the name of the module that is displayed in the **Modules** window.  
  
## See Also  
 [IDebugModule2](../extensibility/idebugmodule2.md)   
 [MODULE_INFO_FIELDS](../extensibility/module_info_fields.md)   
 [MODULE_INFO](../extensibility/module_info.md)