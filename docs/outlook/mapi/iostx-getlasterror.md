---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332165"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft erweiterte Informationen zum letzten Fehler ab.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
>  in Fehlercode. 
    
 _ulFlags_
  
>  [in] Flags, die Verhalten ändern. Dies muss 0 sein. 
    
 _lppMAPIError_
  
>  Out Zeiger auf die **MAPIERROR** -Struktur, die die erweiterten Informationen für den Fehler enthält. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMAPIERROR**. 
    
## <a name="see-also"></a>Siehe auch



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

