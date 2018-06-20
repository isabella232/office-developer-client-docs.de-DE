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
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792713"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Betrifft**: Outlook 
  
Synchronisierung für ein Nachrichtenkopf endet.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parameter

 _pprog_
  
> [in] **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschoben oder kopiert Nachrichten. Finden Sie unter mapidefs.h für die Definition des **LPMAPIPROGRESS**Typs. 
    
## <a name="remarks"></a>Hinweise

Gibt ein der lokale Speicher nach **[IOSTX::SyncBeg](iostx-syncbeg.md)** den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md). Der Client lädt eine vollständige e-Mail-Element (als *PmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter. Wenn dies erfolgreich ist, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**. Bei **IOSTX::SyncHdrEnd**Outlook überprüft das Ergebnis in **HDRSYNC** und *Pprog* und die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf verwendet. 
  
Auf den Status, in dem vor den vorherigen **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** gibt der lokale Speicher zurück. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX: IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

