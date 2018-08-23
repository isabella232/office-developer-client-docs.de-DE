---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594292"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zu den letzten aufgetretenen Fehler in einem Table-Objekt zurück.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Der Rückgabewert von der Methode, die nicht erfolgreich.
    
 _ulFlags_
  
> [in] Nicht verwendet, auf 0 (null) festgelegt.
    
 _lppMAPIError_
  
> [out] Verweist auf eine MAPI- [MAPIERROR](mapierror.md) -Struktur, die Informationen über den letzten Fehler enthält, die für ein Table-Objekt aufgetreten sind. 
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

