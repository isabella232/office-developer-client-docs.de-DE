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
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584681"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft Informationen über den letzten Fehler erweitert.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameter

 _hResult_
  
>  [in] Fehlercode. 
    
 _ulFlags_
  
>  [in] Flags, die Verhalten ändern. Dies muss 0 sein. 
    
 _lppMAPIError_
  
>  [out] Zeiger auf die **MAPIERROR** -Struktur, die erweiterte Informationen für den Fehler enthält. Finden Sie unter mapidefs.h für die Definition des **LPMAPIERROR**Typs. 
    
## <a name="see-also"></a>Siehe auch



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

