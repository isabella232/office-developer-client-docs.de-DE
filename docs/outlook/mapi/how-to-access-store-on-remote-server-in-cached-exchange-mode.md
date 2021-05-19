---
title: Zugreifen auf einen Speicher auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Letzte Änderung: 02. Juli 2012'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420731"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Zugreifen auf einen Speicher auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie Sie das **MAPI_NO_CACHE-Flag** verwenden, um einen Ordner oder eine Nachricht in einem Nachrichtenspeicher auf dem Remoteserver zu öffnen, wenn Microsoft Office Outlook sich im Cached Exchange Mode befindet. 
  
Im cached Exchange Mode können Outlook eine lokale Kopie des Postfachs eines Benutzers verwenden, während Outlook eine Onlineverbindung mit einer Remotekopie des Postfachs des Benutzers auf dem Remoteserver Exchange verwaltet. Wenn Outlook im Cached Exchange Mode ausgeführt wird, sind standardmäßig alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, auch mit dem zwischengespeicherten Nachrichtenspeicher verbunden. Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden für die lokale Kopie des Postfachs vorgenommen.
  
Ein Client oder Dienstanbieter kann die Verbindung zum lokalen Nachrichtenspeicher überschreiben und eine Nachricht oder einen Ordner im Remotespeicher öffnen, indem er das Bit für **MAPI_NO_CACHE** im  *ulFlags-Parameter*  beim Aufrufen von **[IMsgStore::OpenEntry](imsgstore-openentry.md)** festlegen. 
  
Im folgenden Codebeispiel wird gezeigt, wie **IMsgStore::OpenEntry** mit dem im *ulFlags-Parameter* festgelegten **MAPI_NO_CACHE-Flag** zum Öffnen des Stammordners im Remotenachrichtenspeicher aufruft. 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

Wenn Sie den Nachrichtenspeicher  mit dem MDB_ONLINE auf dem Remoteserver geöffnet haben, müssen Sie das MAPI_NO_CACHE **verwenden.** 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

