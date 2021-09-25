---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 416b4ddc3a5798b1621907f7bc22f9bc440a655a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613814"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Synchronisierung im aktuellen Zustand und beendet diesen Zustand.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Bemerkungen

Der Client muss **IOSTX::SyncEnd** für jeden Aufruf von [IOSTX::SyncBeg](iostx-syncbeg.md)aufrufen. Die entsprechende Datenstruktur enthält Informationen, um anzugeben, ob der Client den aktuellen Zustand erfolgreich abgeschlossen hat, damit Outlook den internen Zustand bereinigen kann.
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

