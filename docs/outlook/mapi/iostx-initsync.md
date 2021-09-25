---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5157637bfd133f09af180253790ae3299c807417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587958"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informiert den lokalen Nachrichtenspeicher, dass die Synchronisierung gestartet werden soll.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Kennzeichen zum Ermitteln des geeigneten Verhaltens während der Synchronisierung. Outlook verwendet diese Flags in jedem Status des Replikationsstatuscomputers, um die Informationen zu ermitteln, die für den Client bereitgestellt werden sollen. Wenn der Client beispielsweise **SYNC_ONLY_ASSOCIATED** übergibt, gibt Outlook nur Informationen im Zusammenhang mit zugeordneten (oder ausgeblendeten) Elementen zurück. 
    
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

