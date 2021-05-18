---
title: Implementieren Thread-Safe Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413528"
---
# <a name="implementing-thread-safe-objects"></a>Implementieren Thread-Safe Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bei Objekten, die von Schnittstellenmethodesaufrufen direkt zurückgegeben werden, liegt es in der Verantwortung des Anbieters, die Threadsicherheit sicherzustellen. Bei Rückrufobjekten liegt es in der Verantwortung der Clientanwendung.
  
Ein Client kann einen threadsicheren Benachrichtigungsrückruf implementieren, indem er das MAPI-Hilfsprogramm [HrThisThreadAdviseSink aufruft.](hrthisthreadadvisesink.md) **HrThisThreadAdviseSink** wandelt eine nicht threadsichere Ratensenke in eine threadsichere Absenke um. Für Statusrückrufe gibt es kein solches Hilfsprogramm. Ein Client kann das MAPI-threadsichere Progress-Objekt verwenden oder manuell erstellen. 
  
Ein threadsicheres Objekt ist möglicherweise auch threadsicher. Ein Thread-orientiertes Objekt behält einen separaten Kontext für jeden Thread bei, der es verwendet. Dienstanbieter müssen die Threadsensibilisierung in ihren threadsicheren Objekten nicht unterstützen, auch wenn die Unterstützung der Threadsensibilisierung in einigen Situationen hilfreich sein kann. Zwei MAPI-Tabellen bieten immer einen eigenen Kontext per Definition. Eine Tabelle, die für verschiedene Threads verwendet wird, bietet keinen eindeutigen Kontext.
  
Ein Client kann zwischen dem Empfangen von Benachrichtigungen für denselben Thread, der für den **MAPIInitialize-Aufruf** verwendet wurde, für denselben Thread, der für den **Aufruf "Advise"** verwendet wurde, oder für einen separaten Thread im Besitz von MAPI auswählen. Um sicherzustellen, dass Benachrichtigungen im selben Thread eintreffen, der zum Aufrufen von **MAPIInitialize** verwendet wurde, ruft ein Client [MAPIInitialize](mapiinitialize.md) auf und übergibt null im **ulFlags-Element** der MAPIINIT_0 [Struktur.](mapiinit_0.md) Benachrichtigungen werden dann während der Hauptnachrichtenschleife zugestellt. 
  
Zum Empfangen von Benachrichtigungen im MAPI-eigenen Thread ruft ein Client **MAPIInitialize** mit dem **ulFlags-Mitglied** der **MAPIINIT_0-Struktur** auf MAPI_MULTITHREAD_NOTIFICATIONS. Der **Advise-Aufruf** erfolgt mit dem Ratensenkenobjekt des Clients und nicht mit einer umschlossenen Version. 
  
Um sicherzustellen, dass Benachrichtigungen im selben Thread eintreffen, der zum Aufrufen von **Advise** verwendet wurde, ruft ein Client [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf und übergibt die neu erstellte umschlossene Ratensenke an **Advise** und nicht an die ursprüngliche Ratensenke. **MAPIInitialize** kann mit einem der beiden Flagwerte aufgerufen werden. 
  

