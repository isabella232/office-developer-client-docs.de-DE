---
title: Zugreifen auf einen Speicher auf dem Remoteserver, wenn sich Outlook im Modus "Cached Exchange" befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: b74419367888e6567cadb7f722a455bdddcb9aeb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580146"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Zugreifen auf einen Speicher auf dem Remoteserver, wenn sich Outlook im Modus "Cached Exchange" befindet
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie sie mithilfe des **MAPI_NO_CACHE-Flags** einen Ordner oder eine Nachricht in einem Nachrichtenspeicher auf dem Remoteserver öffnen, wenn sich Microsoft Office Outlook im Modus "Cached Exchange" befindet. 
  
Der zwischengespeicherte Exchange modus ermöglicht Outlook die Verwendung einer lokalen Kopie des Postfachs eines Benutzers, während Outlook eine Onlineverbindung mit einer Remotekopie des Postfachs des Benutzers auf dem Remoteserver Exchange verwaltet. Wenn Outlook im Modus "Cached Exchange" ausgeführt wird, sind alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, ebenfalls mit dem zwischengespeicherten Nachrichtenspeicher verbunden. Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden an der lokalen Kopie des Postfachs vorgenommen.
  
Ein Client oder Dienstanbieter kann die Verbindung mit dem lokalen Nachrichtenspeicher überschreiben und eine Nachricht oder einen Ordner im Remotespeicher öffnen, indem das Bit für **MAPI_NO_CACHE** im  *ulFlags-Parameter*  festgelegt wird, wenn **[IMsgStore::OpenEntry](imsgstore-openentry.md)** aufgerufen wird. 
  
Das folgende Codebeispiel zeigt, wie **IMsgStore::OpenEntry** mit dem im *ulFlags-Parameter* festgelegten **MAPI_NO_CACHE** Flag aufgerufen wird, um den Stammordner im Remotenachrichtenspeicher zu öffnen. 
  
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

Wenn Sie den Nachrichtenspeicher mit dem **Flag MDB_ONLINE** auf dem Remoteserver geöffnet haben, müssen Sie nicht das **flag MAPI_NO_CACHE** verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

