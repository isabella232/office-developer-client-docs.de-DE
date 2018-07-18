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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792718"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Betrifft**: Outlook 
  
Synchronisierung in den aktuellen Status beendet und diesen Status beendet.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Bemerkungen

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

