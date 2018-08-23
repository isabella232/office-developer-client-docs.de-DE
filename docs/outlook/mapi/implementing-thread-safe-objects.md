---
title: Implementieren von threadsicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2f8235caceec8b27b2b14fac26d51e9e31ce1024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579774"
---
# <a name="implementing-thread-safe-objects"></a>Implementieren von threadsicheren Objekten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bei Objekten, die direkt von Schnittstelle-Methodenaufrufen zurückgegeben werden, ist es des Anbieters Verantwortung Threadsicherheit sicherzustellen. Mit Callback-Objekten ist es der Clientanwendung Verantwortung.
  
Ein Client kann einen Rückruf threadsicheren Benachrichtigung durch Aufrufen des MAPI-Dienstprogramms [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)implementieren. **HrThisThreadAdviseSink** Wandelt einen nicht threadsicheren Advise-Empfänger in eine threadsicheren. Für Rückrufe ausgeführt gibt es keine solche Dienstprogramm. Ein Client kann wahlweise verwenden Sie das MAPI-Objekt threadsicheren Fortschritt oder manuell erstellen. 
  
Ein Objekt threadsicheren möglicherweise oder ist möglicherweise auch nicht Thread-fähigen. Ein Thread-fähigen-Objekt behält einen separaten Kontext für jeden Thread, der verwendet wird. Dienstanbieter sind zur Unterstützung der Thread-zur Förderung des Bekanntheitsgrads in ihre Objekte threadsicheren nicht erforderlich, obwohl Thread-zur Förderung des Bekanntheitsgrads Unterstützung in manchen Fällen nützlich sein kann. Zwei MAPI-Tabellen bieten einen eigenen Kontext immer per Definition. Eine Tabelle, die auf verschiedenen Threads verwendet nicht und sollte nicht eindeutigen Kontext bereit.
  
Ein Client haben die Wahl zwischen empfangen von Benachrichtigungen auf dem gleichen Thread, der für die **"MAPIInitialize"** verwendet wurde aufrufen, auf dem gleichen Thread, die für den Anruf **Advise** verwendet wurde, oder in einem getrennten Thread MAPI gehören. Um sicherzustellen, dass Benachrichtigungen auf dem gleichen Thread eintreffen, die zum Aufrufen von **"MAPIInitialize"** verwendet wurde, einem Client ["MAPIInitialize"](mapiinitialize.md) aufgerufen und übergibt NULL im **UlFlags** -Member der Struktur [MAPIINIT_0](mapiinit_0.md) . Benachrichtigungen werden dann während der Nachrichtenschleife Hauptfenster gesendet. 
  
Erhalt von Benachrichtigungen für den MAPI-gehören Thread, ruft ein Client **"MAPIInitialize"** mit dem **UlFlags** -Member der **MAPIINIT_0** Struktur auf MAPI_MULTITHREAD_NOTIFICATIONS festgelegt. Der **Advise** -Aufruf erfolgt mit des Clients advise-Empfängerobjekt statt einer gepackten Version. 
  
Um sicherzustellen, dass Benachrichtigungen auf dem gleichen Thread eintreffen, die zum Aufrufen der **Advise**verwendet wurde, von einem Client [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) aufgerufen und übergibt, die neu erstellte umfließendem, advise-Empfänger, der **Advise** und nicht die ursprünglichen Advise-Empfänger. **"MAPIInitialize"** kann mit beiden Flagwert aufgerufen werden. 
  

