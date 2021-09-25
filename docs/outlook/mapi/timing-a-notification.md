---
title: Timing einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 55bc73a914802e8b3d794348d0bc28c4cdbafda9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590933"
---
# <a name="timing-a-notification"></a>Timing einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da es sich bei der Ereignisbenachrichtigung um einen asynchronen Prozess handelt, können Sie jederzeit benachrichtigt werden, nicht unbedingt unmittelbar nach Eintreten des Ereignisses.
  
 Der Zeitpunkt der [Aufrufe ihrer IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) variiert je nach Dienstanbieter, der die Empfehlungsquelle implementiert. Dienstanbieter können Ihren Client über Folgendes benachrichtigen: 
  
- Gleichzeitig mit dem Ereignis.
    
- Direkt nach dem Ereignis.
    
- Zu einem späteren Zeitpunkt nach dem Ereignis, möglicherweise nach einem **Unadvise-Aufruf.** 
    
Die meisten Dienstanbieter rufen **OnNotify auf,** nachdem die für das Ereignis zuständige MAPI-Methode an den Aufrufer zurückgegeben wurde. Benachrichtigungen zu Nachrichten werden beispielsweise gesendet, wenn Änderungen an der Nachricht gespeichert werden, nach dem [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) oder wenn die Nachricht nach dem **IUnknown::Release-Aufruf** freigegeben wird. Bis zum Senden der Benachrichtigung sind keine Änderungen im Nachrichtenspeicher sichtbar. 
  
Sie können Benachrichtigungen von einer Empfehlungsquelle erhalten, nachdem Sie **"Unadvise"** aufgerufen haben, um eine Registrierung abzubrechen. Stellen Sie sicher, dass Sie Ihre Empfehlungssenke erst freigeben, nachdem die Referenzanzahl auf Null gefallen ist, und nicht nach einem erfolgreichen **Unadvise-Aufruf.** Gehen Sie nicht davon aus, dass die Empfehlungssenke nicht mehr erforderlich ist, da Sie **"Unadvise"** aufgerufen haben. 
  

