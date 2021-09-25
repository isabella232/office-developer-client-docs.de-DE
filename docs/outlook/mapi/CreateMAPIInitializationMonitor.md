---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI-Initialisierungsmonitor
Last modified: April 27, 2021
ms.openlocfilehash: 13992b8094429b61e5f980653b621d0e188ce8c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588329"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**Gilt für:** Outlook 2016 | Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>MAPI-Initialisierungsmonitor

Es gibt Fälle, in denen eine Anwendung, die MAPI nutzt, wissen möchte, wann die Initialisierung abgeschlossen ist. Beispielsweise verfügen sie über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion auf die MAPI-Initialisierung möchte die Anwendung einige Aufgaben ausführen, aber nicht immer den MAPI-Stapel hochdrehen. Der Initialisierungsmonitor stellt diese Funktionalität über eine Funktion (exportiert aus OLMAPI32.DLL) und einige einfache Schnittstellen bereit, die unten beschrieben werden.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```

#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

Dieser Einstiegspunkt, der aus OLMAPI32.DLL exportiert wurde, ermöglicht es dem Aufrufer, eine Schnittstelle abzurufen, um den aktuellen Initialisierungsstatus abzurufen, einen Rückruf für den Abschluss der Initialisierung einzurichten oder den aktuellen Thread zu blockieren, bis er abgeschlossen ist. Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur von Threads, die es abgerufen haben. Im Gegensatz zu anderen Objekten, die von mapi verfügbar gemacht werden, ist dieses Objekt gültig, solange die DLL geladen ist, es kann in allen Initialisierungssitzungen wiederverwendet werden und vor oder nach dem Aufruf von MAPIInitialize genutzt werden. Gibt Erfolg oder Fehler über einen COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen Ausgabeparameter zu.
  
## <a name="parameters"></a>Parameter
  
 _ppInitMonitor_
> [out] Ein Zeiger, der die neu erstellte Instanz des MAPI-Initialisierungsmonitors empfängt.
  
## <a name="return-values"></a>Rückgabewerte

S_OK
> Eine neue Instanz des Initialisierungsmonitors wurde erfolgreich erstellt.

E_OUTOFMEMORY
> Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu kisten.

## <a name="see-also"></a>Siehe auch
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
