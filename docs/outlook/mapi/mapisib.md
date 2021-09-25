---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a36ba483e7a4dd2215dc17e2268e151ce8bbea6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575456"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur wird mit [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md)verwendet.
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> Die Größe der Struktur.
    
 **ulFlags**
  
> Ein Kennzeichen, das den Typ der Synchronisierung angibt. Es muss einer der folgenden Werte sein:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Senden Sie die Nachricht an den Server (wird derzeit nicht verwendet).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Hierarchieänderungen per Push an den Server übertragen.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Hierarchieänderungen vom Server abrufen.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Pushnachrichtänderungen an den Server.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Abrufen von Nachrichtenänderungen vom Server.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |Die Synchronisierung wurde vom Benutzer initiiert und sollte eine höhere Priorität haben.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Sollte nur Kopfzeilen synchronisieren und keine vollständigen Texte.  <br/> |
   
 **psesSync**
  
> [IN] Ein Zeiger auf die MAPI-Sitzung.
    
 **callBack**
  
> [IN] Ein Zeiger auf die Schnittstelle, auf der der Fortschritt bereitgestellt werden soll. Es kann verwendet werden, um die Schnittstelle nach [IMAPISyncProgressCallback : IUnknown abfragt.](imapisyncprogresscallbackiunknown.md)
    
 **\*phSyncDoneEvent**
  
> [OUT] Das Ereignis, das eintritt, wenn der gerade erstellte Thread abgeschlossen ist. Der Zeiger muss gültig sein, da er das Ereignis enthält.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

