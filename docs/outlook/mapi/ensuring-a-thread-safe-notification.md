---
title: Sicherstellen einer Thread-Safe Benachrichtigung
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
# <a name="ensuring-a-thread-safe-notification"></a>Sicherstellen einer Thread-Safe Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Ihr Client auf einer Multithreadplattform ausgeführt wird, müssen Sie möglicherweise sicher sein, dass Aufrufe ihrer [IMAPIAdviseSink::OnNotify-Methoden](imapiadvisesink-onnotify.md) für einen bestimmten Thread ausgeführt werden. Da Aufrufe von **OnNotify** in der Regel in jedem Thread auftreten können, ist es möglich, Benachrichtigungen zu unerwarteten und unerwünschten Threads zu erhalten, was zu Fehlern führt, die schwer zu debuggen sind. 
  
Rufen Sie [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) auf, bevor Sie Advise aufrufen, um zu gewährleisten, dass Anrufe an **OnNotify** für eine bestimmte Benachrichtigung im selben Thread ausgeführt werden, der für den **Anruf "Advise"** verwendet **wurde.** ** **HrThisThreadAdviseSink**** erstellt ein neues Advise Sink-Objekt aus Ihrem Advise Sink-Objekt. Übergeben Sie dieses neue Objekt im Aufruf von **Advise**. Alle Clients mit beratenden Sinkobjekten, die möglicherweise nicht außerhalb des Kontexts eines bestimmten Threads funktionieren, sollten immer mit **HrThisThreadAdviseSink** erstellte Ratensenkenobjekte registrieren.
  

