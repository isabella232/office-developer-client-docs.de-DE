---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a630db9edb03c67f1f8e2c7a3b19088a88b1123b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620506"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt einen lokalen Speicher fest, um den Outlook-Protokoll-Manager zum Spoolen ausgehender Nachrichten an einen Server zu emulieren.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Legen Sie diesen Parameter auf "True" fest, wenn der lokale Speicher den Spooler emulieren soll. legen Sie ihn auf "False" fest, wenn nicht. 
    
## <a name="remarks"></a>Bemerkungen

Ein lokaler Speicher ruft **IPSTX::EmulateSpooler** auf, um als Outlook Protokoll-Manager zu fungieren und Nachrichten in der ausgehenden Warteschlange zur Verarbeitung an den Back-End-Server (z. B. MSN-Server oder AOL-Server) zu senden. Beim Emulieren eines Spoolers während der Synchronisierung ruft der Speicher dann die folgenden beiden Methoden auf: 
  
1. **[IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md)** um die ausgehende Warteschlange von Nachrichten im Store abzurufen. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook Protocol Manager emuliert. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** zum Sichern des alleinigen Zugriffs auf eine Nachricht in der ausgehenden Warteschlange direkt vor dem Senden an den Server. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook Protocol Manager emuliert. Nach dem Senden der Nachricht ruft der Speicher diese Methode erneut auf, um den alleinigen Zugriff darauf freizugeben. 
    
> [!NOTE]
> Seit Outlook 2002 ersetzte der Outlook Protocol Manager den MAPI-Spooler und wurde für die Warteschlange ausgehender Nachrichten an Back-End-Server verantwortlich. 
  
## <a name="see-also"></a>Siehe auch



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

