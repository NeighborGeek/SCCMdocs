---
title: "GetEULA Method in Class SMS_SettingsDefinitionBase | Microsoft Docs"
ms.custom: ""
ms.date: "09/20/2016"
ms.prod: "configuration-manager"
ms.reviewer: ""
ms.suite: ""
ms.technology:
  - "configmgr-other"
ms.tgt_pltfrm: ""
ms.topic: "article"
applies_to:
  - "System Center Configuration Manager (current branch)"
ms.assetid: b4be2023-a18c-4475-a10a-d269806507a3
caps.latest.revision: 5
author: "shill-ms"
ms.author: "v-suhill"
manager: "mbaldwin"
---
# GetEULA Method in Class SMS_SettingsDefinitionBase
The `GetEULA` Windows Management Instrumentation (WMI) class method, in System Center Configuration Manager, gets the localized Microsoft Software License Terms text of the configuration item.  

 The following syntax is simplified from Managed Object Format (MOF) code and defines the method.  

## Syntax  

```  
SInt32 GetEULA(  
      String EULA  
);  
```  

#### Parameters  
 `EULA`  
 Data type: `String`  

 Qualifiers: [out]  

 A value identifying the localized license terms.  

## Return Values  
 An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.  

 For information about handling returned errors, see [About Configuration Manager Errors](../../../develop/core/understand/about-configuration-manager-errors.md).  

## Remarks  
 Your application should call this method only if the `EulaExists` property is set to `true` in the configuration item. This property is defined in the [SMS_ConfigurationItemBaseClass Server WMI Class](../../../develop/reference/compliance/sms_configurationitembaseclass-server-wmi-class.md).  

## Requirements  

## Runtime Requirements  
 For more information, see [Configuration Manager Server Runtime Requirements](../../../develop/core/reqs/server-runtime-requirements.md).  

## Development Requirements  
 For more information, see [Configuration Manager Server Development Requirements](../../../develop/core/reqs/server-development-requirements.md).  

## See Also  
 [SMS_ConfigurationItem Server WMI Class](../../../develop/reference/compliance/sms_configurationitem-server-wmi-class.md)   
 [SMS_ConfigurationItemBaseClass Server WMI Class](../../../develop/reference/compliance/sms_configurationitembaseclass-server-wmi-class.md)