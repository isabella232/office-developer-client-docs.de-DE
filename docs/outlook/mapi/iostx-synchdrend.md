---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591331"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Synchronisierung für ein Nachrichtenkopf endet.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parameter

 _pprog_
  
> [in] **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschoben oder kopiert Nachrichten. Finden Sie unter mapidefs.h für die Definition des **LPMAPIPROGRESS**Typs. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Gibt ein der lokale Speicher nach **[IOSTX::SyncBeg](iostx-syncbeg.md)** den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md). Der Client lädt eine vollständige e-Mail-Element (als *PmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter. Wenn dies erfolgreich ist, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**. Bei **IOSTX::SyncHdrEnd**Outlook überprüft das Ergebnis in **HDRSYNC** und *Pprog* und die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf verwendet. 
  
Auf den Status, in dem vor den vorherigen **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** gibt der lokale Speicher zurück. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

