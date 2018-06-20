---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a8e353bbb4f276169ae26ba9d05821158bf55f00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792817"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Betrifft**: Outlook 
  
Outlook-Protokoll-Manager, um ausgehende Nachrichten an einen Server Spoolen emulieren ein lokales Speichers festgelegt.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Legen Sie diesen Parameter auf true fest, wenn der lokale Speicher die Warteschlange emulieren soll; Legen Sie ihn auf False, wenn nicht. 
    
## <a name="remarks"></a>Hinweise

Ein lokales Speichers **IPSTX::EmulateSpooler** fungieren als ein Outlook Protokollmanager, Einreihen in die Warteschlange Nachrichten in der ausgehenden Warteschlange auf dem Back-End-Server (beispielsweise MSN-Server oder AOL-Server) für die Verarbeitung von Anrufen. Emulieren einer Warteschlange während der Synchronisation, ruft der Speicher dann diese beiden Methoden: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** zum Abrufen der ausgehenden Warteschlange von Nachrichten in den Speicher. Diese Methode ist nur dann, wenn der Informationsspeicher die Outlook-Protokollmanager emulieren ist erfolgreich. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** zum Sichern der alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange einfach, bevor sie an den Server gesendet wird. Diese Methode ist nur dann, wenn der Informationsspeicher die Outlook-Protokollmanager emulieren ist erfolgreich. Nach dem Senden der Nachricht, ruft der Speicher diese Methode erneut aus, um die alleinige Zugriff darauf freigeben. 
    
> [!NOTE]
> Seit Outlook 2002 die Outlook-Protokollmanager ersetzt die MAPI-Warteschlange und aus dem Back-End-Server für ausgehende Nachrichten in Warteschlange zuständig. 
  
## <a name="see-also"></a>Siehe auch



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

