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
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439576"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Synchronisierung im aktuellen Zustand und beendet diesen Status.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Bemerkungen

Der Client muss **IOSTX:: SyncEnd** für jeden Aufruf von [IOSTX:: SyncBeg](iostx-syncbeg.md)aufrufen. Die entsprechende Datenstruktur enthält Informationen, um anzugeben, ob der Client den aktuellen Zustand erfolgreich abgeschlossen hat, damit Outlook seinen internen Status bereinigen kann.
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

