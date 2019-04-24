---
title: Implementieren von Thread sicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310038"
---
# <a name="implementing-thread-safe-objects"></a>Implementieren von Thread sicheren Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei Objekten, die von Schnittstellenmethoden aufrufen direkt zurückgegeben werden, obliegt es dem Anbieter, die Threadsicherheit sicherzustellen. Bei Rückrufobjekten ist es die Aufgabe der Clientanwendung.
  
Ein Client kann einen threadsicheren Benachrichtigungsrückruf implementieren, indem er das MAPI-Dienstprogramm [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transformiert eine nicht threadsichere Advise-Senke in ein threadsicheres. Für Status Rückrufe gibt es kein solches Hilfsprogramm. Ein Client kann das MAPI-threadsichere Progress-Objekt verwenden oder manuell erstellen. 
  
Ein threadsicheres Objekt ist möglicherweise auch nicht Thread fähig. Ein Thread fähiges Objekt verwaltet einen separaten Kontext für jeden Thread, der es verwendet. Dienstanbieter müssen die Thread Erkennung in ihren threadsicheren Objekten nicht unterstützen, obwohl die Unterstützung der Thread Erkennung in einigen Situationen nützlich sein kann. Zwei MAPI-Tabellen stellen immer ihren eigenen Kontext per Definition bereit. Eine Tabelle, die in verschiedenen Threads verwendet wird, bietet keinen eindeutigen Kontext.
  
Ein Client kann zwischen dem Empfang von Benachrichtigungen für den gleichen Thread, der für den **MAPIInitialize** -Aufruf verwendet wurde, im gleichen Thread, der für den **Advise** -Aufruf verwendet wurde, oder in einem separaten Thread, der im Besitz von MAPI ist, wählen. Um sicherzustellen, dass Benachrichtigungen für den gleichen Thread eingehen, der zum Aufrufen von **MAPIInitialize**verwendet wurde, Ruft ein Client [MAPIInitialize](mapiinitialize.md) auf und übergibt 0 (null) im **ulFlags** -Element der [MAPIINIT_0](mapiinit_0.md) -Struktur. Benachrichtigungen werden dann während der Hauptmeldungsschleife übermittelt. 
  
Um Benachrichtigungen über den MAPI-besessenen Thread zu erhalten, Ruft ein Client **MAPIInitialize** mit dem **ulFlags** -Element der **MAPIINIT_0** -Struktur auf MAPI_MULTITHREAD_NOTIFICATIONS festgelegt. Der **Advise** -Aufruf erfolgt mit dem Advise-Objekt des Clients und nicht mit einer umbrochenen Version. 
  
Um sicherzustellen, dass Benachrichtigungen für den gleichen Thread eingehen, der zum Aufrufen von **Advise**verwendet wurde, Ruft ein Client [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf und übergibt die **** neu erstellte umschlossene Advise-Senke anstatt der ursprünglichen Advise-Senke. **MAPIInitialize** kann mit einem der beiden Flags-Werte aufgerufen werden. 
  

