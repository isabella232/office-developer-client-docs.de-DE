---
title: Sicherstellen einer Thread-Safe benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a0154e82227adc381b2e53cee47562be7ba3112b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601086"
---
# <a name="ensuring-a-thread-safe-notification"></a>Sicherstellen einer Thread-Safe benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihr Client auf einer Multithreadplattform ausgeführt wird, müssen Sie möglicherweise sicherstellen, dass Aufrufe ihrer [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) in einem bestimmten Thread erfolgen. Da Aufrufe von **OnNotify** in der Regel in jedem Thread auftreten können, ist es möglich, Benachrichtigungen für unerwartete und unerwünschte Threads zu empfangen, was zu Fehlern führt, die nur schwer zu debuggen sind. 
  
Um sicherzustellen, dass Aufrufe von **OnNotify** für eine bestimmte Benachrichtigung im gleichen Thread erfolgen, der für den **Advise-Aufruf** verwendet wurde, rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) vor dem Aufrufen von **Advise** auf. ** **HrThisThreadAdviseSink** erstellt ein neues Advise-Senkenobjekt aus Ihrem Advise-Senkenobjekt. Übergeben Sie dieses neue Objekt im Aufruf von **Advise**. Alle Clients mit empfohlenen Senkenobjekten, die möglicherweise nicht außerhalb des Kontexts eines bestimmten Threads funktionieren, sollten immer empfohlenen Senkenobjekte registrieren, die mit **HrThisThreadAdviseSink** erstellt wurden.
  

