---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418708"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Diese Struktur wird mit [IMAPISync::SynchronizeInBackground verwendet.](imapisyncsynchronizeinbackground.md)
  
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
  
> Ein Flag, das den Synchronisierungstyp angibt. Dies muss einer der folgenden Werte sein:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Senden Sie die Nachricht an den Server (derzeit nicht verwendet).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Pushhierarchieänderungen an den Server.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Ziehen Sie Hierarchieänderungen vom Server ab.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Push-Nachrichtenänderungen an den Server.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Ziehen von Nachrichtenänderungen vom Server.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |Die Synchronisierung wurde vom Benutzer initiiert und sollte eine höhere Priorität haben.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Sollte nur Kopfzeilen synchronisieren und keine vollständigen Textkörper.  <br/> |
   
 **psesSync**
  
> [IN] Ein Zeiger auf die MAPI-Sitzung.
    
 **punkCallBack**
  
> [IN] Ein Zeiger auf die Schnittstelle, auf der Fortschritt erzielt werden soll. Es kann zum Abfragen der Schnittstelle für [IMAPISyncProgressCallback : IUnknown verwendet werden.](imapisyncprogresscallbackiunknown.md)
    
 **\*phSyncDoneEvent**
  
> [OUT] Das Ereignis, das auftritt, wenn der gerade erstellte Thread abgeschlossen ist. Der Zeiger muss gültig sein, da er das Ereignis enthält.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

