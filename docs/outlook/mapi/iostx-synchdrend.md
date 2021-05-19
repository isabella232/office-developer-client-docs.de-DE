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
description: 'Letzte Änderung: 03. Juli 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432772"
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
    
## <a name="remarks"></a>Hinweise

Bei **[IOSTX::SyncBeg](iostx-syncbeg.md)** gibt der lokale Speicher den Status ["Nachrichtenkopf herunterladen" ein.](download-message-header-state.md) Der Client lädt ein vollständiges Nachrichtenelement herunter (als  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ). Wenn dies erfolgreich ist, legt der Client *auch ulFlags* in **HDRSYNC als** **HSF_OK.** Bei **IOSTX::SyncHdrEnd** überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet *pprog* und die Informationen in **HDRSYNC,** um den lokalen Nachrichtenkopf zu aktualisieren. 
  
Der lokale Speicher kehrt in den Zustand zurück, in dem er sich vor dem vorherigen **[IOSTX::SyncHdrBeg -Wert auftrat.](iostx-synchdrbeg.md)** 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

