---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a92089c9df921259b0df638ec94b118fa53276cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613926"
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

 _Hresult_
  
> [in] Der Rückgabewert der fehlgeschlagenen Methode.
    
 _ulFlags_
  
> [in] Nicht verwendet, auf 0 (Null) festgelegt.
    
 _lppMAPIError_
  
> [out] Verweist auf eine MAPI [MAPIERROR-Struktur,](mapierror.md) die Informationen zum letzten Fehler enthält, der für ein Tabellenobjekt aufgetreten ist. 
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

