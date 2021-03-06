---
title: WritePropertyValue 函数 （非托管 API 参考）
description: WritePropertyValue 函数将字节写入属性。
ms.date: 11/06/2017
api_name:
- WritePropertyValue
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- WritePropertyValue
helpviewer_keywords:
- WritePropertyValue function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6aafb918616d27cf6289a8747f3336b2e813beb6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33461079"
---
# <a name="writepropertyvalue-function"></a>WritePropertyValue 函数
将指定的数目的字节写入由属性句柄识别的属性。

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>语法  
  
```  
HRESULT WritePropertyValue (
   [in] int                  vFunc, 
   [in] IWbemObjectAccess*   ptr, 
   [in] long                 lHandle,
   [in] long                 lNumBytes,
   [in] byte*                aData
); 
```  

## <a name="parameters"></a>参数

`vFunc`  
[in]未使用此参数。

`ptr`  
[in]指向的指针[IWbemObjectAccess](https://msdn.microsoft.com/library/aa391770(v=vs.85).aspx)实例。

`lHandle`  
[in]一个整数，包含标识此属性的句柄。 可通过调用检索句柄[GetPropertyHandle](getpropertyhandle.md)函数。   

`lNumBytes`  
[in]正在写入的属性的字节数。 请参阅[备注](#remarks)部分以了解更多信息。

`pHandle`   
[out]指向包含数据的字节数组的指针。

## <a name="return-value"></a>返回值

此函数返回以下值中定义*WbemCli.h*标头文件，或者你可以定义它们常量作为在代码中：

|返回的常量  |值  |描述  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | 0x80041008 | 参数不是有效的。 |
|`WBEM_E_TYPE_MISMATCH` | 0x80041005 | 出现类型不匹配。 |
|`WBEM_S_NO_ERROR` | 0 | 函数调用成功。  |
  
## <a name="remarks"></a>备注

此函数包装对的调用[IWbemClassObject::WritePropertyValue](https://msdn.microsoft.com/library/aa391783(v=vs.85).aspx)方法。

使用此函数可设置字符串和所有其他非`DWORD`或非-`QWORD`数据。

对于非字符串属性值，`lNumBytes`必须是指定的属性类型的正确的数据大小。 字符串属性值，`lNumBytes`必须是长度以字节为单位，指定的字符串和字符串本身必须为偶数长度以字节为单位，以 null 终止字符开始便遵循。

## <a name="requirements"></a>要求  
**平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** WMINet_Utils.idl  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>请参阅  
[WMI 和性能计数器 （非托管 API 参考）](index.md)
