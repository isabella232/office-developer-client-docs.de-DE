---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568840"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Synchronisierung in den aktuellen Status beendet und diesen Status beendet.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>HinwBemerkungeneise

Der Client muss für jeden Aufruf von [IOSTX::SyncBeg](iostx-syncbeg.md) **IOSTX::SyncEnd** aufrufen. Die entsprechenden-Datenstruktur enthält Informationen an, ob der Client den aktuellen Status erfolgreich abgeschlossen wurde, damit der interne Zustand von Outlook bereinigen kann.
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

