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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360396"
---
# <a name="timing-a-notification"></a>Timing einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da es sich bei der Ereignisbenachrichtigung um einen asynchronen Prozess handelt, können Sie jederzeit benachrichtigt werden, nicht unbedingt unmittelbar nach dem Ereignis.
  
 Der Zeitpunkt der Aufrufe Ihrer [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode variiert je nach dem Dienstanbieter, der die Advise-Quelle implementiert. Dienstanbieter können Ihren Client entweder Benachrichtigen: 
  
- Gleichzeitig mit dem Ereignis.
    
- Direkt nach dem Ereignis.
    
- Zu einem späteren Zeitpunkt nach dem Ereignis, möglicherweise **** nach einem Unadvise-Aufruf. 
    
Die meisten Dienstanbieter **** rufen OnNotify auf, nachdem die für das Ereignis zuständige MAPI-Methode an den Aufrufer zurückgegeben wurde. Benachrichtigungen an Nachrichten werden beispielsweise gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem Aufruf von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) oder nach der Veröffentlichung der Nachricht nach dem Aufruf von **IUnknown:: Release** . Bis zum Senden der Benachrichtigung sind keine Änderungen im Nachrichtenspeicher sichtbar. 
  
Sie können Benachrichtigungen von einer Advise-Quelle erhalten, nachdem Sie **Unadvise** aufgerufen haben, um eine Registrierung abzubrechen. Stellen Sie sicher, dass Sie Ihre Advise-Senke erst freigeben, nachdem der Verweiszähler auf Null gesunken ist **** , nicht nach einem erfolgreichen Unadvise-Aufruf. Gehen Sie nicht davon aus, dass die **** Advise-Senke nicht mehr erforderlich ist, weil Sie Unadvise aufgerufen haben. 
  

