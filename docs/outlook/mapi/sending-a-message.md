---
title: Senden einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 291d1b5595c8f0779b5d5644397a1ebfd2576a0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629585"
---
# <a name="sending-a-message"></a>Senden einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie zum Senden einer Nachricht bereit sind, rufen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf. **SubmitMessage** platziert die Nachricht in der ausgehenden Warteschlange und legt das flag MSGFLAG_SUBMIT in der **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht fest.
  
Wenn der Nachrichtenspeicheranbieter eng mit einem Transportanbieter gekoppelt ist, wird die Nachricht direkt an den Transport übergeben, der sie an das Messagingsystem übermittelt. Wenn die Verbindung nicht eng ist, informiert der Nachrichtenspeicheranbieter den MAPI-Spooler darüber, dass sich die ausgehende Warteschlange geändert hat, und der MAPI-Spooler überträgt die Nachricht an einen entsprechenden Transportanbieter.
  
Wenn Sie Zulassen, dass Benutzer einen Sendevorgang abbrechen, rufen [Sie IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) auf, um dieses Feature zu implementieren. **AbortSubmit** entfernt die Nachricht aus der ausgehenden Warteschlange. Benutzer können verhindern, dass ein Senden erfolgt, bis die Nachricht an das zugrunde liegende Messagingsystem gesendet wird. 
  
Wenn **SubmitMessage** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gesendeten Daten jetzt verloren gehen. Bevor Sie versuchen, ein zweites Mal zu senden, schreiben Sie die Nachricht erneut, indem Sie [IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::SaveChanges](imapiprop-savechanges.md)aufrufen. Zeigt dem Benutzer einen Fehler an, wenn diese **IMAPIProp-Aufrufe** fehlschlagen oder **wenn SubmitMessage** ein zweites Mal fehlschlägt. 
  
Geben Sie nach einem erfolgreichen Aufruf von **SubmitMessage** alle Speicher frei, der für die Empfängerliste reserviert wurde, und geben Sie die Nachricht und deren Anlagen frei. Nachdem eine Nachricht gesendet wurde, lässt MAPI keine weiteren Vorgänge für die Zeiger für diese Objekte zu. Die einzige Ausnahme besteht **darin, IUnknown::Release aufzurufen.** Es sind keine weiteren Aufrufe zulässig, da viele Nachrichtenspeicheranbieter Eintragsbezeichner für gesendete Nachrichten ungültig macht.
  

