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
ms.openlocfilehash: f696d9739014659812de3309ec885f37a6f85cc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572137"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

 **ulSize**
  
> Die Größe der Struktur.
    
 **ulFlags**
  
> Ein Flag, der angibt, welche Art von Synchronisierung. Es muss eine der folgenden Werte sein:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0 x 00000200  <br/> |Senden Sie die Nachricht an den Server (derzeit nicht in Verwendung).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Push-Hierarchie auf dem Server geändert wird.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Pull Hierarchie Änderungen vom Server an.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0 x 00000040  <br/> |Drücken Sie auf Server Nachricht ändert.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Ziehen Sie Meldung Änderungen vom Server.  <br/> |
|SYNC_ON_DEMAND  <br/> |0 x 20000000  <br/> |Die Synchronisierung wurde vom Benutzer initiiert und eine höhere Priorität sein.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Sollte nur Kopfzeilen und nicht vollständige synchronisieren.  <br/> |
   
 **psesSync**
  
> [IN] Ein Zeiger auf die MAPI-Sitzung.
    
 **punkCallBack**
  
> [IN] Ein Zeiger auf die Schnittstelle auf dem laufenden bereitstellen. Die Schnittstelle für Abfragen verwendet werden [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] Das Ereignis, das ausgeführt wird, wenn der Thread, der soeben erstellte abgeschlossen ist. Der Mauszeiger muss gültig sein, da das Ereignis enthalten wird.
    
## <a name="see-also"></a>Siehe auch



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

