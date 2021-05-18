---
title: Timing einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411148"
---
# <a name="timing-a-notification"></a>Timing einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da es sich bei der Ereignisbenachrichtigung um einen asynchronen Prozess handelt, können Sie jederzeit benachrichtigt werden, nicht unbedingt unmittelbar nach dem Ereignis.
  
 Der Zeitpunkt der Anrufe an Ihre [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) variiert je nach Dienstanbieter, der die Ratgeberquelle implementieren. Dienstanbieter können Ihren Client entweder benachrichtigen: 
  
- Gleichzeitig mit dem Ereignis.
    
- Direkt nach dem Ereignis.
    
- Zu einem späteren Zeitpunkt nach dem Ereignis, möglicherweise nach einem **Unadvise-Aufruf.** 
    
Die meisten Dienstanbieter rufen **OnNotify** auf, nachdem die für das Ereignis zuständige MAPI-Methode an den Aufrufer zurückgegeben wurde. Beispielsweise werden Benachrichtigungen zu Nachrichten gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) oder wenn die Nachricht nach dem **IUnknown::Release-Aufruf** freigegeben wird. Bis zum Senden der Benachrichtigung werden keine Änderungen im Nachrichtenspeicher angezeigt. 
  
Sie können Benachrichtigungen von einer Informationsquelle erhalten, nachdem Sie **Unadvise** zum Abbrechen einer Registrierung aufgerufen haben. Stellen Sie sicher, dass Sie ihre Ratensenke erst los lassen, nachdem die Referenzanzahl auf Null gefallen ist, und nicht nach einem erfolgreichen **Unadvise-Aufruf.** Gehen Sie nicht davon aus, dass die Ratensenke nicht mehr erforderlich ist, da Sie **Unadvise** aufgerufen haben. 
  

