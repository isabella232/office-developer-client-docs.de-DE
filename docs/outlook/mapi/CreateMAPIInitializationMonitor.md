---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: MAPI-Initialisierungsmonitor
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062053"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**Gilt für**: Outlook 2016 | Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>MAPI-Initialisierungsmonitor

Es gibt Zeiten, in denen eine Anwendung, die MAPI verwendet, wissen möchte, wann die Initialisierung abgeschlossen ist. Sie verfügt beispielsweise über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion darauf, dass MAPI initialisiert wird, möchte die Anwendung einige Aufgaben ausführen, möchte aber nicht immer den MAPI-Stapel spinn. Der Initialisierungsmonitor stellt diese Funktionalität über eine Funktion (exportiert aus OLMAPI32.DLL) und einige einfache Schnittstellen bereit, die unten beschrieben werden.

Dies ist ein Einstiegspunkt, der aus OLMAPI32.DLL dadurch kann der Aufrufer eine Schnittstelle abrufen, um den aktuellen Initialisierungsstatus abzurufen, einen Rückruf für den Initialisierungsabschluss einrichten oder den aktuellen Thread blockieren, bis er abgeschlossen ist. Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur vom Thread, der es abgerufen hat. Im Gegensatz zu anderen Objekten, die von MAPI verfügbar gemacht werden, ist dieses Objekt auch gültig, solange die DLL geladen wird, sie kann in initialisierungssitzungen erneut verwendet werden und vor oder nach dem Aufrufen von MAPIInitialize verwendet werden. Gibt Erfolg oder Fehler über ein COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen out-Parameter zu.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

Dieser aus OLMAPI32.DLL exportierte Einstiegspunkt ermöglicht dem Aufrufer das Abrufen einer Schnittstelle zum Abfragen des aktuellen Initialisierungszustands, zum Einrichten eines Rückrufs für den Initialisierungsabschluss oder zum Blockieren des aktuellen Threads, bis er abgeschlossen ist. Das von dieser API zurückgegebene Objekt ist wiederverwendbar und threadsicher und kann von jedem Thread aufgerufen werden, nicht nur vom Thread, der es abgerufen hat. Im Gegensatz zu anderen Objekten, die von MAPI verfügbar gemacht werden, ist dieses Objekt auch gültig, solange die DLL geladen wird, sie kann in initialisierungssitzungen erneut verwendet werden und vor oder nach dem Aufrufen von MAPIInitialize verwendet werden. Gibt Erfolg oder Fehler über ein COM-Standard-HRESULT zurück und weist einer Instanz von IMAPIInitMonitor einen out-Parameter zu.
  
## <a name="quick-info"></a>QuickInfo

| Bezeichner | result |
|:-----|:-----|
|Exportiert von:  <br/> |olmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |

## <a name="parameters"></a>Parameter
  
 _ppInitMonitor_
> [out] Ein Zeiger zum Empfangen der neu erstellten Instanz des MAPI-Initialisierungsmonitors.
  
## <a name="return-values"></a>Rückgabewerte

S_OK
> Eine neue Instanz des Initialisierungsmonitors wurde erfolgreich erstellt.

E_OUTOFMEMORY
> Es war nicht genügend Arbeitsspeicher vorhanden, um ein neues Objekt zu kisten.

## <a name="see-also"></a>Siehe auch
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
