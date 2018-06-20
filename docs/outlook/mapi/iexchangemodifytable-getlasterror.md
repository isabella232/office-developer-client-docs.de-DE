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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792060"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Betrifft**: Outlook 
  
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



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

