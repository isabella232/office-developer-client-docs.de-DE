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
  
Wenn Sie zum Senden einer Nachricht bereit sind, rufen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf. **SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und legt das MSGFLAG_SUBMIT-Flag in der **PR_MESSAGE_FLAGS** - Eigenschaft der Nachricht ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) fest.
  
Wenn der Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist, übergibt die Nachricht die Nachricht direkt an den Transport, der sie an das Messagingsystem übermittelt. Wenn nicht eng gekoppelt, informiert der Nachrichtenspeicheranbieter den MAPI-Spooler, dass die ausgehende Warteschlange geändert wurde, und der MAPI-Spooler überträgt die Nachricht an einen geeigneten Transportanbieter.
  
Wenn Sie Benutzern das Abbrechen eines Sendevorgangs erlauben, rufen Sie [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) auf, um dieses Feature zu implementieren. **AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange. Benutzer können das Senden beenden, bis die Nachricht an das zugrunde liegende Messagingsystem gesendet wird. 
  
Wenn **SubmitMessage** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gesendeten Daten verloren gehen. Bevor Sie versuchen, ein zweites Mal zu senden, schreiben Sie die Nachricht erneut, indem Sie [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::SaveChanges aufrufen.](imapiprop-savechanges.md) Zeigt dem Benutzer einen Fehler an, wenn diese **IMAPIProp-Aufrufe** fehlschlagen oder **wenn SubmitMessage** ein zweites Mal fehlschlägt. 
  
Geben Sie nach einem erfolgreichen Aufruf von **SubmitMessage** den für die Empfängerliste zugewiesenen Arbeitsspeicher frei, und geben Sie die Nachricht und ihre Anlagen frei. Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Vorgänge an den Zeigern für diese Objekte zu. Die einzige Ausnahme ist das Aufrufen **von IUnknown::Release**. Es sind keine weiteren Aufrufe zulässig, da viele Nachrichtenspeicheranbieter Eingabebezeichner für gesendete Nachrichten ungültig machen.
  

