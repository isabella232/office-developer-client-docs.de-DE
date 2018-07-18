---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792707"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Betrifft**: Outlook 
  
Informiert dem lokalen Nachrichtenspeicher, dass Synchronisierung gestartet.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Kennzeichen, die um entsprechende Verhalten während der Synchronisierung zu bestimmen. Outlook verwendet diese Flags in jedem Status des Computers Zustand Replikation, um die Informationen zu ermitteln, die für den Client bereitgestellt werden sollen. Angenommen, wenn der Client **SYNC_ONLY_ASSOCIATED**übergibt, wird Outlook nur Informationen im Zusammenhang mit der zugehörigen (oder ausgeblendet) Elemente zurück. 
    
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

