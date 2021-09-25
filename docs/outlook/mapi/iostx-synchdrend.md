---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: d246754dd0ac9b131808b05d5ac669aee0f5d542
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564078"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Synchronisierung für einen Nachrichtenkopf.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parameter

 _pprog_
  
> [in] **[IMAPIProgress-Schnittstelle](imapiprogressiunknown.md)** für die Synchronisierung von verschobenen oder kopierten Nachrichten. Die Typdefinition von **LPMAPIPROGRESS** finden Sie unter mapidefs.h. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Bei **[IOSTX::SyncBeg](iostx-syncbeg.md)** wechselt der lokale Speicher in den Headerstatus der [Downloadnachricht.](download-message-header-state.md) Der Client lädt ein vollständiges Nachrichtenelement herunter (wie *pmsgFull* in **[HDRSYNC).](hdrsync.md)** Wenn dies erfolgreich ist, legt der Client auch  *ulFlags*  in **HDRSYNC** als **HSF_OK** fest. Bei **IOSTX::SyncHdrEnd** überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet *pprog* und die Informationen in **HDRSYNC,** um den lokalen Nachrichtenkopf zu aktualisieren. 
  
Der lokale Speicher kehrt in den Zustand zurück, in dem er sich vor dem vorherigen **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** befand. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

