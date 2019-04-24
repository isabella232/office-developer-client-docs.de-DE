---
title: Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299062"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie das **MAPI_NO_CACHE** -Flag zum Öffnen eines Ordners oder einer Nachricht in einem Nachrichtenspeicher auf dem Remoteserver verwendet wird, wenn sich Microsoft Office Outlook im Exchange-Cache-Modus befindet. 
  
Der Exchange-Cache-Modus ermöglicht es Outlook, eine lokale Kopie des Postfachs eines Benutzers zu verwenden, während Outlook eine Onlineverbindung mit einer Remotekopie des Postfachs des Benutzers auf dem Exchange-Remoteserver verwaltet. Wenn Outlook im Exchange-Cache-Modus ausgeführt wird, werden standardmäßig alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, auch mit dem zwischengespeicherten Nachrichtenspeicher verbunden. Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden mit der lokalen Kopie des Postfachs vorgenommen.
  
Ein Client oder Dienstanbieter kann die Verbindung mit dem lokalen Nachrichtenspeicher außer Kraft setzen und eine Nachricht oder einen Ordner im Remotespeicher öffnen, indem das Bit für **MAPI_NO_CACHE** im Parameter *ulFlags* beim Aufrufen von **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** festgelegt wird. 
  
Im folgenden Codebeispiel wird gezeigt, wie Sie **IMsgStore:: OpenEntry** mit dem **MAPI_NO_CACHE** -Flag aufrufen, das im *ulFlags* -Parameter festgelegt ist, um den Stammordner im Remotenachrichtenspeicher zu öffnen. 
  
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

Wenn Sie den Nachrichtenspeicher mit dem **MDB_ONLINE** -Flag auf dem Remoteserver geöffnet haben, müssen Sie das **MAPI_NO_CACHE** -Flag nicht verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

