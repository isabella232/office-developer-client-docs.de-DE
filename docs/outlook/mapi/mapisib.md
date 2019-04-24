---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270210"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur wird mit [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)verwendet.
  
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

## <a name="members"></a>Elemente

 **ulSize**
  
> Die Größe der Struktur.
    
 **ulFlags**
  
> Ein Flag, das den Synchronisierungs angibt. Dabei muss es sich um einen der folgenden Werte handeln:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Senden Sie die Nachricht an den Server (derzeit nicht verwendet).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Hierarchieänderungen auf dem Server pushen.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Hierarchieänderungen vom Server abrufen.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Push Message Changes to Server.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Nachrichtenänderungen vom Server abrufen.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |Die Synchronisierung wurde vom Benutzer initiiert und sollte eine höhere Priorität haben.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Sollte nur Kopfzeilen und keine vollständigen Körper synchronisieren.  <br/> |
   
 **psesSync**
  
> IN Ein Zeiger auf die MAPI-Sitzung.
    
 **punkCallBack**
  
> IN Ein Zeiger auf die Schnittstelle, für die der Fortschritt bereitgestellt werden soll. Sie kann zum Abfragen der Schnittstelle für [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)verwendet werden.
    
 **\*phSyncDoneEvent**
  
> Out Das Ereignis, das auftritt, wenn der soeben erstellte Thread abgeschlossen ist. Der Zeiger muss gültig sein, da er das Ereignis enthält.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

