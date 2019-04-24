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
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332186"
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

 _pProg_
  
> in **[IMAPIProgress](imapiprogressiunknown.md)** -Schnittstelle für die Synchronisierung von verschobenen oder kopierten Nachrichten. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Bemerkungen

Bei **[IOSTX:: SyncBeg](iostx-syncbeg.md)** gibt der lokale Speicher den [Status des Download Nachrichtenkopfs](download-message-header-state.md)ein. Der Client lädt ein vollständiges Nachrichtenelement (als *pmsgFull* in **[HDRSYNC](hdrsync.md)** ) herunter. Wenn dies erfolgreich ist, legt der Client auch *ulFlags* in **HDRSYNC** als **HSF_OK**fest. Bei **IOSTX:: SyncHdrEnd**überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet *pProg* und die Informationen in **HDRSYNC** , um den lokalen Nachrichtenkopf zu aktualisieren. 
  
Der lokale Speicher wird in den Zustand zurückgegeben, in dem er vor dem vorhergehenden **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

