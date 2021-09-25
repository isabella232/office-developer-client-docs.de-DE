---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 27, 2021
ms.openlocfilehash: 5eaac9c74bc08b8525e21f805d68d8c0d4cb5072
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575995"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019

Es gibt Fälle, in denen eine Anwendung, die MAPI nutzt, wissen möchte, wann die Initialisierung abgeschlossen ist. Beispielsweise verfügt sie über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion auf die Initialisierung der MAPI möchte die Anwendung einige Aufgaben ausführen, aber nicht immer den MAPI-Stapel hochdrehen. Der Initialisierungsmonitor stellt diese Funktionalität über ein [CreateMAPIInitializationMonitor-Objekt bereit.](createmapiinitializationmonitor.md)

| Quickinfos | result |
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> | OLMAPI32.DLL <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>VTable-Reihenfolge

| Funktion | description |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |Gibt den aktuellen Status der MAPI-Initialisierung zurück.  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgegeben wird, wenn die angegebene Anzahl von Millisekunden abgelaufen ist oder mapi initialisiert wurde.  INFINITE kann für eine unendliche Wartezeit verwendet werden.  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |Starten Sie eine Wartezeit für die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden. Dadurch wird eine IMAPIWaitResult-Schnittstelle zurückgegeben, bei der "End" aufgerufen werden sollte, um die Wartezeit zu beginnen.  Dadurch kann der Aufrufer steuern, welcher Thread während des Wartens blockiert wird. <br/> |

## <a name="see-also"></a>Siehe auch

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
