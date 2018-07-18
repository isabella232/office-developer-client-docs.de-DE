---
title: Zugriff auf einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: 8bb1e9bfc4d816daf4285d083c87bb3bea4e1139
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791826"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Zugriff auf einen Speicher auf dem Remoteserver, wenn Outlook im Exchange-Cache-Modus befindet
 
**Betrifft**: Outlook 
  
Dieses Thema enthält ein Codebeispiel in C++, das zeigt, wie Sie die Kennzeichen **MAPI_NO_CACHE** zum Öffnen eines Ordners oder einer Nachricht auf einen Nachrichtenspeicher auf dem Remoteserver, wenn Microsoft Office Outlook in der Exchange-Cache-Modus befindet. 
  
Exchange-Cache-Modus ermöglicht Outlook eine lokale Kopie des Postfachs eines Benutzers verwendet, während Outlook eine online-Verbindung zu einer remote-Kopie des Postfachs des Benutzers, auf dem Exchange-Remoteserver verwaltet. Wenn Outlook im Exchange-Cache-Modus, wird standardmäßig ausgeführt wird werden alle MAPI-Lösungen, die auf der gleichen Sitzung anmelden auch mit dem Cache Nachrichtenspeicher verbunden. Anhand der lokalen Kopie des Postfachs werden alle Daten, die zugegriffen werden kann und alle vorgenommenen Änderungen vorgenommen.
  
Ein Client oder Dienstanbieter kann die Verbindung mit den lokalen Nachrichtenspeicher überschreiben und öffnen Sie eine Nachricht oder einen Ordner auf dem remote-Speicher durch das Bit beim Aufruf von **[IMsgStore::OpenEntry](imsgstore-openentry.md)** für **MAPI_NO_CACHE** im *UlFlags* -Parameter festlegen. 
  
Das folgende Codebeispiel zeigt, wie **IMsgStore::OpenEntry** mit dem im Parameter *UlFlags* legen Sie zum Öffnen des Ordners "Root" auf dem remote-Nachrichtenspeicher **MAPI_NO_CACHE** -Flag aufrufen. 
  
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

Wenn Sie mit dem **MDB_ONLINE** -Flag auf dem Remoteserver Nachrichtenspeicher geöffnet haben, müssen Sie keinen **MAPI_NO_CACHE** -Flag verwenden. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Öffnen eines Speichers auf dem Remote-Server, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

