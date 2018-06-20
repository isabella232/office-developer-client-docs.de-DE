---
title: Sicherstellen, dass eine Benachrichtigung threadsicheren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791627"
---
# <a name="ensuring-a-thread-safe-notification"></a>Sicherstellen, dass eine Benachrichtigung threadsicheren

  
  
**Betrifft**: Outlook 
  
Wenn der Client auf eine Multithread-Plattform ausgeführt wird, benötigen Sie möglicherweise die Assurance, dass Anrufe an Ihre [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Methoden für einen bestimmten Thread auftreten. Da Anrufe an **OnNotify** in der Regel auf einem beliebigen Thread auftreten können, ist es möglich, Benachrichtigung bei unerwarteten und unerwünschte Threads, führt zu Fehlern, die schwierig zu debuggen sind. 
  
Sicherstellen, dass Anrufe an **OnNotify** für eine bestimmte Benachrichtigung rufen Sie auf dem gleichen Thread, der für die **Advise** verwendet wurde, rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) vor **Advise**vorgenommen werden. ** ** HrThisThreadAdviseSink *** erstellt ein neues Advise-Empfänger-Objekt aus der Advise-Empfängerobjekt. Übergeben Sie den Anruf an **Advise**dieses neue Objekt. Alle Clients mit Advise-Empfänger,-Objekten, die möglicherweise nicht außerhalb des Kontexts von einem bestimmten Thread verwendet werden sollte immer registrieren, advise-Empfängerobjekten mit **HrThisThreadAdviseSink**erstellt.
  

