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
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590911"
---
# <a name="sending-a-message"></a>Senden einer Nachricht

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie eine Nachricht senden möchten, rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode. **SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und das Flag MSGFLAG_SUBMIT in der Nachricht **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft festgelegt.
  
Die Nachricht Speicheranbieter gibt, wenn eng mit eines Transportdienstes verknüpft die Nachricht direkt an die Übertragung, die es an die messaging-System übermittelt. Wenn dies nicht eng gekoppelt, der Speicheranbieter Nachricht informiert die MAPI-Warteschlange, die die ausgehende Warteschlange geändert hat und die MAPI-Warteschlange übermittelt die Nachricht an einen entsprechenden Transport-Dienstanbieter.
  
Wenn Sie einen Sendevorgang Abbrechen Benutzern ermöglichen, rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) , um dieses Feature zu implementieren. **AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange. Können Benutzer so beenden Sie einen Send auftritt, bis die Nachricht an die zugrunde liegenden messaging-System erhält. 
  
Wenn **SubmitMessage** MAPI_E_CORRUPT_DATA zurückgibt, wird davon ausgegangen Sie, dass die gesendeten Daten ist jetzt verloren. Bevor Sie versuchen, ein zweites Mal senden, müssen schreiben Sie die Nachricht erneut durch Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Für den Benutzer ein Fehler angezeigt, wenn diese **IMAPIProp** Aufrufe fehlschlagen oder **SubmitMessage** ein zweites Mal fehlschlägt. 
  
Freien Sie nach einem erfolgreichen Aufruf von **SubmitMessage**Speicher, für die Empfängerliste zugewiesen wurde, und freigeben Sie die Nachricht und ihre Anhänge. Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Operationen auf den Zeiger für diese Objekte. Die einzige Ausnahme ist **IUnknown**aufrufen. Keine anderen Aufrufe sind zulässig, da viele Nachricht Anbieter Eintragsbezeichner für Nachrichten für ungültig erklärt, die gesendet wurden.
  

