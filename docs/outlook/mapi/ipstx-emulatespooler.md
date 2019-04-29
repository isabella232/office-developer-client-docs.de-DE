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
  
Legt einen lokalen Speicher für die Emulation des Outlook-Protokoll-Managers zum Spoolen ausgehender Nachrichten an einen Server fest.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  in Legen Sie diesen Parameter auf true fest, wenn der lokale Speicher den Spooler emulieren soll; Legen Sie ihn auf false fest, wenn nicht. 
    
## <a name="remarks"></a>Bemerkungen

Ein lokaler Speicher ruft **IPSTX:: EmulateSpooler** auf, um als Outlook-Protokoll-Manager zu fungieren und Nachrichten in der ausgehenden Warteschlange auf dem Back-End-Server (beispielsweise MSN Server oder AOL Server) zur Verarbeitung zu spoolen. Emulieren eines Spoolers während der Synchronisierung ruft der Speicher die folgenden beiden Methoden auf: 
  
1. **[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** zum Abrufen der ausgehenden Warteschlange von Nachrichten im Speicher. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook-Protokoll-Manager emuliert. 
    
2. **[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** , um den alleinigen Zugriff auf eine Nachricht in der ausgehenden Warteschlange zu sichern, bevor Sie an den Server gesendet wird. Diese Methode ist nur erfolgreich, wenn der Speicher den Outlook-Protokoll-Manager emuliert. Nach dem Senden der Nachricht ruft der Informationsspeicher diese Methode erneut auf, um den alleinigen Zugriff darauf zu veröffentlichen. 
    
> [!NOTE]
> Seit Outlook 2002 hat der Outlook-Protokoll-Manager den MAPI-Spooler ersetzt und ist für das Spoolen ausgehender Nachrichten an Back-End-Server verantwortlich. 
  
## <a name="see-also"></a>Siehe auch



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

