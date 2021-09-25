---
title: Implementieren von Thread-Safe-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf3b3e9dddaeb09a15ab658b6a6cd6d8447c4140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630544"
---
# <a name="implementing-thread-safe-objects"></a>Implementieren von Thread-Safe-Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei Objekten, die direkt von Schnittstellenmethodenaufrufen zurückgegeben werden, liegt es in der Verantwortung des Anbieters, die Threadsicherheit sicherzustellen. Bei Rückrufobjekten liegt es in der Verantwortung der Clientanwendung.
  
Ein Client kann einen threadsicheren Benachrichtigungsrückruf implementieren, indem er das MAPI-Hilfsprogramm [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)aufruft. **HrThisThreadAdviseSink** transformiert eine nicht threadsichere Empfehlungssenke in eine threadsichere. Für Statusrückrufe gibt es kein solches Hilfsprogramm. Ein Client kann das MAPI-threadsichere Statusobjekt verwenden oder manuell erstellen. 
  
Ein threadsicheres Objekt ist möglicherweise auch threadfähig. Ein threadfähiges Objekt behält einen separaten Kontext für jeden Thread bei, der es verwendet. Dienstanbieter müssen threadbezogene Informationen in ihren threadsicheren Objekten nicht unterstützen, obwohl die Unterstützung des Thread-Bewusstseins in einigen Situationen hilfreich sein kann. Zwei MAPI-Tabellen stellen per Definition immer ihren eigenen Kontext bereit. Eine Tabelle, die in verschiedenen Threads verwendet wird, bietet keinen eindeutigen Kontext und sollte keinen eindeutigen Kontext bereitstellen.
  
Ein Client kann zwischen dem Empfangen von Benachrichtigungen im selben Thread wählen, der für den **MAPIInitialize-Aufruf** verwendet wurde, für denselben Thread, der für den **Advise-Aufruf** verwendet wurde, oder für einen separaten Thread, der der MAPI gehört. Um sicherzustellen, dass Benachrichtigungen im gleichen Thread eingehen, der zum Aufrufen von **MAPIInitialize** verwendet wurde, ruft ein Client [MAPIInitialize](mapiinitialize.md) auf und übergibt null im **ulFlags-Element** der [MAPIINIT_0-Struktur.](mapiinit_0.md) Benachrichtigungen werden dann während der Hauptnachrichtenschleife übermittelt. 
  
Um Benachrichtigungen im MAPI-eigenen Thread zu erhalten, ruft ein Client **MAPIInitialize** mit dem **ulFlags-Mitglied** der **MAPIINIT_0** Struktur auf MAPI_MULTITHREAD_NOTIFICATIONS festgelegt auf. Der **Advise-Aufruf** erfolgt mit dem Empfehlungssenkenobjekt des Clients und nicht mit einer umschlossenen Version. 
  
Um sicherzustellen, dass Benachrichtigungen auf demselben Thread eingehen, der zum Aufrufen von **"Advise"** verwendet wurde, ruft ein Client [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf und übergibt die neu erstellte, umschlossene Empfehlungssenke anstelle der ursprünglichen Empfehlungssenke an **Advise.** **MAPIInitialize** kann mit beiden Flagwerten aufgerufen werden. 
  

