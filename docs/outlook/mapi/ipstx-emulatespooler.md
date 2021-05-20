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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438953"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt einen lokalen Speicher fest, um den Outlook Protokoll-Manager zu emulieren, um ausgehende Nachrichten mit einem Server zu spoolen.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Legen Sie diesen Parameter auf True, wenn der lokale Speicher den Spooler emulieren soll. legen Sie ihn auf False, falls nicht. 
    
## <a name="remarks"></a>Hinweise

Ein lokaler Speicher ruft **IPSTX::EmulateSpooler** auf, um als Outlook-Protokoll-Manager zu fungieren und Nachrichten in der ausgehenden Warteschlange zur Verarbeitung an den Back-End-Server (z. B. MSN-Server oder AOL-Server) zu spoolen. Beim Emulieren eines Spoolers während der Synchronisierung ruft der Speicher dann die folgenden beiden Methoden auf: 
  
1. **[IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md)** um die ausgehende Warteschlange mit Nachrichten im Store zu erhalten. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook simuliert. 
    
2. **[IMsgStore::SetLockState,](imsgstore-setlockstate.md)** um den alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange zu sichern, kurz bevor sie an den Server gesendet wird. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook simuliert. Nach dem Senden der Nachricht ruft der Store diese Methode erneut auf, um den alleinigen Zugriff darauf frei zu geben. 
    
> [!NOTE]
> Seit Outlook 2002 ersetzte der Outlook-Protokoll-Manager den MAPI-Spooler und wurde für das Spooling ausgehender Nachrichten an Back-End-Server verantwortlich. 
  
## <a name="see-also"></a>Siehe auch



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

