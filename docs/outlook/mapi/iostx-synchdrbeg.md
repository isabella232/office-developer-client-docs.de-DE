---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8059830b65045890ceb4b3e75bd059c420e58761
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592277"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Startet die Synchronisierung für einen Nachrichtenkopf.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameter

 _cbeid_
  
> [in] Die Anzahl der Bytes in der Eintrags-ID für die Nachricht.
    
 _lpeid_
  
> [in] Die Eintrags-ID für die Nachricht.
    
 _Ppv_
  
>  [in]/[out] Zeiger auf die **[HDRSYNC-Struktur](hdrsync.md)** für den Nachrichtenkopf. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Bei **IOSTX::SyncHdrBeg** wechselt der lokale Speicher in den Headerstatus der [Downloadnachricht.](download-message-header-state.md) Outlook initialisiert für den Client die **HDRSYNC-Struktur** mit der aktuellen Darstellung des Nachrichtenkopfs im Speicher und im übergeordneten Ordner. Der Client muss dann ein vollständiges Nachrichtenelement herunterladen (wie *pmsgFull* in **HDRSYNC).** Wenn dies erfolgreich war, legt der Client auch  *ulFlags*  in **HDRSYNC** als **HSF_OK** fest. Bei **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** überprüft Outlook das Ergebnis in **HDRSYNC** und verwendet die Informationen in **HDRSYNC,** um den lokalen Nachrichtenkopf zu aktualisieren. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

