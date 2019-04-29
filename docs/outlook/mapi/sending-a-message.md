---
title: Senden einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423622"
---
# <a name="sending-a-message"></a>Senden einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie bereit sind, eine Nachricht zu senden, rufen Sie die zugehörige [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf. **SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und legt das MSGFLAG_SUBMIT-Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht fest.
  
Wenn der Nachrichtenspeicher Anbieter eng mit einem Transportanbieter gekoppelt ist, gibt er die Nachricht direkt an den Transport, der Sie an das Messagingsystem übermittelt. Wenn nicht eng gekoppelt, informiert der Nachrichtenspeicher Anbieter die MAPI-Spooler, dass die ausgehende Warteschlange geändert wurde und der MAPI-Spooler die Nachricht an einen geeigneten Transportanbieter überträgt.
  
Wenn Sie Benutzern das Abbrechen eines Sendevorgangs gestatten, rufen Sie [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) auf, um dieses Feature zu implementieren. **AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange. Benutzer können das Senden von Ereignissen beenden, bis die Nachricht an das zugrunde liegende Messagingsystem gesendet wird. 
  
Wenn **SUBMITMESSAGE** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gesendeten Daten jetzt verloren gehen. Bevor Sie versuchen, ein zweites Mal zu senden, schreiben Sie die Nachricht erneut, indem Sie [IMAPIProp::](imapiprop-setprops.md) SetProps und [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)aufrufen. Zeigt dem Benutzer einen Fehler an, wenn diese **IMAPIProp** -Aufrufe fehlschlagen oder wenn **SubmitMessage** ein zweites Mal fehlschlägt. 
  
Geben Sie nach einem erfolgreichen Anruf bei **SubmitMessage**den Speicherplatz frei, der für die Empfängerliste reserviert wurde, und geben Sie die Nachricht und ihre Anlagen frei. Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Vorgänge für die Zeiger für diese Objekte zu. Die einzige Ausnahme ist das Aufrufen von **IUnknown:: Release**. Es sind keine weiteren Anrufe zulässig, da viele Nachrichtenspeicher Anbieter Eintragsbezeichner für gesendete Nachrichten ungültig machen.
  

