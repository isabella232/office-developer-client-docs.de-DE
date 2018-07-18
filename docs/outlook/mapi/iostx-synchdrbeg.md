---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792711"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Betrifft**: Outlook 
  
Synchronisierung für ein Nachrichtenkopf gestartet.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameter

 _cbeid_
  
> [in] Die Anzahl von Bytes in die Eintrags-ID für die Nachricht.
    
 _lpeid_
  
> [in] Die Eintrags-ID für die Nachricht.
    
 _ppv_
  
>  [in] / [out] Zeiger auf die Struktur **[HDRSYNC](hdrsync.md)** für die Nachrichtenkopfzeile. 
    
## <a name="remarks"></a>Bemerkungen

Bei **IOSTX::SyncHdrBeg**Speichern der lokalen Kopie Übergänge, um den [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md). Outlook initialisiert die **HDRSYNC** -Struktur mit der aktuellen Darstellung der Kopfzeile der Nachricht in den Speicher und die des übergeordneten Ordners für den Client. Der Client muss dann eine vollständige e-Mail-Element (als *PmsgFull* in **HDRSYNC** ) heruntergeladen werden. Wenn dies erfolgreich war, wird der Client *UlFlags* auch in **HDRSYNC** als **HSF_OK**. Bei **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** Outlook überprüft das Ergebnis in **HDRSYNC** und verwendet die Informationen in **HDRSYNC** zum Aktualisieren der lokalen Nachrichtenkopf. 
  
## <a name="see-also"></a>Siehe auch



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI-Konstanten](mapi-constants.md)

