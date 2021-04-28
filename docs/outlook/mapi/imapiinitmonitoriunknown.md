---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062046"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**Gilt für**: Outlook 2013 | Outlook 2016 | Outlook 2019

Es gibt Zeiten, in denen eine Anwendung, die MAPI verwendet, wissen möchte, wann die Initialisierung abgeschlossen ist. Sie verfügt beispielsweise über mehrere Threads, die MAPI initialisieren könnten, oder als Reaktion auf die initialisierte MAPI möchte die Anwendung einige Aufgaben ausführen, möchte jedoch nicht immer den MAPI-Stapel spinn. Der Initialisierungsmonitor stellt diese Funktionalität über ein [CreateMAPIInitializationMonitor-Objekt](createmapiinitializationmonitor.md) bereit.

| Schnellinfos | result |
|:-----|:-----|
|Erbt von:  <br/> |IUnknown  <br/> |
|Implementiert von:  <br/> | OLMAPI32.DLL <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>Vtable-Reihenfolge

| Funktion | description |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |Gibt den aktuellen Status der MAPI-Initialisierung zurück.  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |Initiiert einen BLOCKING-Aufruf für diesen Thread, der entweder zurückgeht, wenn die angegebene Anzahl von Millisekunden verstrichen ist oder MAPI initialisiert wurde.  INFINITE kann für unendliche Wartezeiten verwendet werden.  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |Starten Sie eine Wartezeit auf die MAPI-Initialisierung oder die angegebene Anzahl von Millisekunden bis zum Verstreichen. Dadurch wird eine IMAPIWaitResult-Schnittstelle zurück, die "End" aufgerufen haben sollte, um mit dem Warten zu beginnen.  Dadurch kann der Aufrufer steuern, welcher Thread während der Wartezeit blockiert wird. <br/> |
