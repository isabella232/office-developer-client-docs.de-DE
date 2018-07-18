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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 69853dbec46b08c4dc402012fb7f1074f30ebf52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792699"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Betrifft**: Outlook 
  
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

