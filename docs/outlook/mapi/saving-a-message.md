---
title: Speichern einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420931"
---
# <a name="saving-a-message"></a>Speichern einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor eine Nachricht gespeichert wird, rufen Clients in der Regel die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Nachricht auf, um neben den Nachrichtentexteigenschaften, Anlageneigenschaften, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und eigenschaften, die der Empfängerliste zugeordnet sind, einige Eigenschaften zu setzen.
  
Legen Sie **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft auf eine Zeichenzeichenfolge wie IPM. Beachten Sie, dass die Klasse der ausgehenden Nachricht beschrieben wird. Clients sollten zwar **PR_MESSAGE_CLASS** für alle ausgehenden Nachrichten festlegen, aber der Nachrichtenspeicheranbieter gibt einen Standardwert an, wenn Sie ihn nicht festlegen. Die Standardnachrichtenklasse für ausgehende Nachrichten ist IPM. 
  
Legen Sie das MSGFLAG_UNSENT in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) -Eigenschaft. Legen Sie bei Bedarf auch die MSGFLAG_READ und MSGFLAG_UNMODIFIED ein. Durch festlegen MSGFLAG_UNMODIFIED kann eine Nachricht unter Komposition eine übermittelte Nachricht simulieren. MSGFLAG_UNMODIFIED können nur von Clients festgelegt werden, bevor eine Nachricht zum ersten Mal gespeichert wurde. 
  
Wenn Sie bereit sind, eine dauerhafte Kopie einer nicht gesendeten Nachricht zu erstellen, rufen Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) für die Nachricht und alle anlagen auf. Wenn Sie die Nachricht sofort senden möchten, müssen Sie **SaveChanges nicht aufrufen.** Der Aufruf von **SubmitMessage speichert** die Nachricht intern als Teil der Verarbeitung. 
  
Beim Aufrufen **von SaveChanges** sollten Sie das Flag KEEP_OPEN_READWRITE angeben, mit dem die Nachricht zu einem späteren Zeitpunkt geändert werden kann. Andere festgelegte Flags sind FORCE_SAVE, das angibt, dass die Nachricht oder Anlage nach dem Festlegen von Änderungen geschlossen werden soll, KEEP_OPEN_READONLY, das angibt, dass keine weiteren Änderungen vorgenommen werden, und das Flag, das dem Nachrichtenspeicheranbieter das Batchen von Clientanforderungen ermöglicht, MAPI_DEFERRED_ERRORS.
  
Es ist wichtig, dass **Sie SaveChanges für** jede Anlage in der Nachricht aufrufen, bevor **Sie SaveChanges für** die Nachricht aufrufen. Wenn Sie eine Anlage nicht speichern, wird die Anlage nicht in die Nachricht einbezogen, wenn sie gesendet wird, und sie wird nicht in der Anlagentabelle der Nachricht angezeigt. Wenn Die Nachricht nach dem Speichern aller Anlagen nicht gespeichert werden kann, gehen sowohl die Nachricht als auch die Anlagen verloren. 
  
Wenn **SaveChanges** aufgerufen wird, aktualisiert der Nachrichtenspeicheranbieter die folgenden Eigenschaften: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) listet alle primären Empfänger auf.
    
- **PR_DISPLAY_TO** listet alle Carbon copy-Empfänger auf. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) listet alle blinden #A0 auf.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** legt MSGFLAG_HASATTACH fest, ob eine oder mehrere Anlagen gespeichert wurden, und MSGFLAG_UNMODIFIED, um zu zeigen, dass die Nachricht geändert wurde. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) enthält die aktuelle Größe der Nachricht.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) bietet Zugriff auf die Anlagentabelle.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) bietet Zugriff auf die Empfängertabelle.
    
Einige Nachrichteneigenschaften werden in der Regel von Clients oder Dienstanbietern bereitgestellt, wenn eine Nachricht erstellt wird. Wenn ein Client sie nicht festlegen will, liegt es an dem Nachrichtenspeicheranbieter, sie zum Zeitpunkt des Aufrufs von **SaveChanges** zu aktualisieren. Wenn beispielsweise die Eigenschaften **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) einer Nachricht festgelegt wurden, wenn die Nachricht erstellt wurde, müssen sie nicht zur Zeit geändert werden. Nachrichtenspeicheranbieter, die sie bei der Nachrichtenerstellung nicht festlegen, müssen sie jedoch beim ersten Aufruf von **SaveChanges** festlegen. 
  
Wenn **SaveChanges** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gespeicherten Daten jetzt verloren gehen. Nachrichtenspeicheranbieter, die ein Client-Server-Modell für ihre Implementierung verwenden, geben diesen Wert möglicherweise zurück, wenn eine Netzwerkverbindung verloren geht oder der Server nicht ausgeführt wird. Bevor Sie einen Fehler an den Benutzer zurückgeben, versuchen Sie, die Daten ein zweites Mal zu schreiben und zu speichern, indem Sie einen Aufruf von **SetProps** gefolgt von einem weiteren Aufruf von **SaveChanges machen.** Wenn die Daten lokal zwischengespeichert werden, sollte dies kein Problem sein. Wenn jedoch kein lokaler Cache vorhanden ist oder der zweite **SaveChanges-Aufruf** fehlschlägt, wird ein Fehler angezeigt, um den Benutzer auf das Problem zu warnen. 
  

