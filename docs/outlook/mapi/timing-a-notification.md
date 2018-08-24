---
title: Zeitliches steuern einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b4b0292ab16eabe30755fe84885a29fb8e3ce295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595195"
---
# <a name="timing-a-notification"></a>Zeitliches steuern einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da ereignisbenachrichtigung einen asynchronen Prozess ist, können Sie jederzeit nicht unbedingt benachrichtigt werden, unmittelbar nachdem das Ereignis eingetreten ist.
  
 Der Zeitpunkt der Aufrufe an die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode variiert je nach der Implementierung der Advise-Quelle Dienstanbieter. Dienstanbieter können Ihren Client entweder benachrichtigt werden: 
  
- Gleichzeitig mit dem Ereignis.
    
- Direkt nach dem Ereignis.
    
- An einem später Punkt nach der Ereignis möglicherweise nach einem Aufruf **Unadvise** . 
    
Die meisten Dienstanbieter Aufrufen **OnNotify** , nachdem die MAPI-Methode für das Ereignis verantwortliche an die aufrufende zurückgegeben hat. Beispielsweise werden Benachrichtigungen für Nachrichten gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem Aufruf von [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder die Nachricht nach dem Aufruf von **IUnknown** freigegeben ist. Bis die Benachrichtigung gesendet wird, sind keine Änderungen im Nachrichtenspeicher sichtbar. 
  
Sie können aus einer Datenquelle Advise Benachrichtigungen empfangen, nachdem Sie **Unadvise** um eine Registrierung abzubrechen aufgerufen haben. Achten Sie darauf, dass Ihre Advise-Empfänger Version erst nach seiner Referenzzähler auf 0 (null), nicht nach einem erfolgreichen Aufruf der **Unadvise** gefallen hat. Gehen Sie nicht, da Sie **Unadvise** aufgerufen haben der Advise-Empfänger nicht mehr benötigt wird. 
  

