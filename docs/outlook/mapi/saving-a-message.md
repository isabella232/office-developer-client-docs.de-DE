---
title: Speichern einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af55a8a8a48be1ee92cb11ea8e793ac2afef2a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586824"
---
# <a name="saving-a-message"></a>Speichern einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor eine Nachricht gespeichert wird, rufen Clients in der Regel die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Nachricht auf, um zusätzlich zu den Nachrichtentexteigenschaften, Anlageneigenschaften, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und eigenschaften, die der Empfängerliste zugeordnet sind, einige Eigenschaften festzulegen.
  
Legen Sie die **Eigenschaft PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) auf eine Zeichenfolge wie IPM fest. Beachten Sie, dass die Klasse der ausgehenden Nachricht beschrieben wird. Obwohl Clients **PR_MESSAGE_CLASS** für alle ausgehenden Nachrichten festlegen sollten, wird ein Standardwert vom Nachrichtenspeicheranbieter bereitgestellt, wenn Sie ihn nicht festlegen. Die Standardnachrichtenklasse für ausgehende Nachrichten ist IPM. 
  
Legen Sie das flag MSGFLAG_UNSENT in der **Eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) fest. Legen Sie bei Bedarf auch die Flags MSGFLAG_READ und MSGFLAG_UNMODIFIED fest. Durch Festlegen des MSGFLAG_UNMODIFIED kann eine Nachricht in der Komposition eine zugestellte Nachricht simulieren. MSGFLAG_UNMODIFIED können nur von Clients festgelegt werden, bevor eine Nachricht zum ersten Mal gespeichert wurde. 
  
Wenn Sie bereit sind, eine dauerhafte Kopie einer nicht gesendeten Nachricht zu erstellen, rufen Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) für die Nachricht und alle anlagen auf. Wenn Sie beabsichtigen, die Nachricht sofort zu senden, müssen Sie **SaveChanges** nicht aufrufen. Der Aufruf von **SubmitMessage** speichert die Nachricht intern im Rahmen der Verarbeitung. 
  
Beim Aufrufen von **SaveChanges empfiehlt** es sich, das KEEP_OPEN_READWRITE-Flag anzugeben, mit dem die Nachricht zu einem späteren Zeitpunkt geändert werden kann. Andere festlegbare Flags sind FORCE_SAVE, die angeben, dass die Nachricht oder Anlage geschlossen werden soll, nachdem Änderungen vorgenommen wurden, KEEP_OPEN_READONLY, was bedeutet, dass keine weiteren Änderungen vorgenommen werden, und das Flag, das es dem Nachrichtenspeicheranbieter ermöglicht, Clientanforderungen MAPI_DEFERRED_ERRORS zu stapeln.
  
Es ist wichtig, dass Sie **SaveChanges** für jede Anlage in der Nachricht aufrufen, bevor Sie **SaveChanges** für die Nachricht aufrufen. Wenn Sie eine Anlage nicht speichern können, wird die Anlage beim Senden nicht in die Nachricht eingeschlossen, und sie wird nicht in der Anlagentabelle der Nachricht angezeigt. Wenn Sie die Nachricht nach dem Speichern aller Anlagen nicht speichern können, gehen sowohl die Nachricht als auch die Anlagen verloren. 
  
Wenn **SaveChanges** aufgerufen wird, aktualisiert der Nachrichtenspeicheranbieter die folgenden Eigenschaften: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) listet alle primären Empfänger auf.
    
- **PR_DISPLAY_TO** listet alle Empfänger von Kopierkopien auf. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) listet alle Blindkopieempfänger auf.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** legt MSGFLAG_HASATTACH fest, ob eine oder mehrere Anlagen gespeichert wurden, und löscht MSGFLAG_UNMODIFIED, um anzuzeigen, dass die Nachricht geändert wurde. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) enthält die aktuelle Größe der Nachricht.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ermöglicht den Zugriff auf die Anlagentabelle.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) ermöglicht den Zugriff auf die Empfängertabelle.
    
Einige Nachrichteneigenschaften werden in der Regel von Clients oder Dienstanbietern bereitgestellt, wenn eine Nachricht erstellt wird. Wenn ein Client nicht bereit ist, sie festzulegen, liegt es beim Nachrichtenspeicheranbieter, ihn beim Aufruf von **SaveChanges** zu aktualisieren. Wenn beispielsweise die Eigenschaften **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) einer Nachricht beim Erstellen der Nachricht festgelegt wurden, müssen sie nicht zur Speicherzeit geändert werden. Nachrichtenspeicheranbieter, die es nicht versäumen, sie bei der Nachrichtenerstellung festzulegen, müssen sie jedoch festlegen, wenn **SaveChanges** zum ersten Mal aufgerufen wird. 
  
Wenn **SaveChanges** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gespeicherten Daten jetzt verloren gehen. Nachrichtenspeicheranbieter, die ein Clientservermodell für ihre Implementierung verwenden, können diesen Wert zurückgeben, wenn eine Netzwerkverbindung unterbrochen wird oder der Server nicht ausgeführt wird. Versuchen Sie vor dem Zurückgeben eines Fehlers an den Benutzer, die Daten ein zweites Mal zu schreiben und zu speichern, indem Sie einen Aufruf von **SetProps** gefolgt von einem weiteren Aufruf von **SaveChanges** ausführen. Wenn die Daten lokal zwischengespeichert werden, sollte dies kein Problem darstellen. Wenn jedoch kein lokaler Cache vorhanden ist oder der zweite **SaveChanges-Aufruf** fehlschlägt, wird ein Fehler angezeigt, um den Benutzer auf das Problem hinzuweisen. 
  

