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
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424511"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen zum letzten Fehler zurück, der in einem Tabellenobjekt aufgetreten ist.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parameter

 _hResult_
  
> [in] Der Rückgabewert der methode, die fehlgeschlagen ist.
    
 _ulFlags_
  
> [in] Nicht verwendet, auf 0 (Null) festgelegt.
    
 _lppMAPIError_
  
> [out] Zeigt auf eine [MAPI MAPIERROR-Struktur,](mapierror.md) die Informationen zum letzten Fehler enthält, der für ein Tabellenobjekt aufgetreten ist. 
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

