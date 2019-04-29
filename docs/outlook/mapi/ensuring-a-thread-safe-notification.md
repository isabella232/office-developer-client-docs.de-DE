---
title: Sicherstellen einer Thread sicheren Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424847"
---
# <a name="ensuring-a-thread-safe-notification"></a>Sicherstellen einer Thread sicheren Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihr Client auf einer Multithread-Plattform ausgeführt wird, müssen Sie möglicherweise sicherstellen, dass Aufrufe an Ihre [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methoden in einem bestimmten Thread stattfinden. Da Aufrufe von **OnNotify** in der Regel in einem beliebigen Thread auftreten können, ist es möglich, Benachrichtigungen zu unerwarteten und unerwünschten Threads zu erhalten, was zu Fehlern führt, die schwierig zu Debuggen sind. 
  
Um sicherzustellen, dass Aufrufe von onNotify für eine bestimmte Benachrichtigung für den gleichen Thread ausgeführt werden, der für den **Advise** -Aufruf verwendet wurde, rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, bevor **Sie** **Advise**aufrufen. * * * * HrThisThreadAdviseSink * * * * erstellt ein neues Advise-Senke-Objekt aus dem Advise-Senke-Objekt. Führen Sie dieses neue Objekt im Aufruf von **Advise**aus. Alle Clients mit Advise-Senke-Objekten, die möglicherweise nicht außerhalb des Kontexts eines bestimmten Threads funktionieren, sollten immer Advise-Senke-Objekte registrieren, die mit **HrThisThreadAdviseSink**erstellt wurden.
  

