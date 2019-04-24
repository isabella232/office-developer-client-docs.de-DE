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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283121"
---
# <a name="saving-a-message"></a>Speichern einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor eine Nachricht gespeichert wird, rufen Clients in der Regel die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Nachricht auf, um zusätzlich zu den Nachrichtentext Eigenschaften, Anlageneigenschaften, **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) und Eigenschaften eine Reihe von Eigenschaften festzulegen. der Empfängerliste zugeordnet.
  
Legen Sie die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft auf eine Zeichenfolge wie IPM. Beachten Sie, dass die Klasse der ausgehenden Nachricht beschrieben wird. Obwohl Clients **PR_MESSAGE_CLASS** für alle ausgehenden Nachrichten festlegen sollen, wird vom Nachrichtenspeicher Anbieter ein Standardwert angegeben, wenn Sie ihn nicht festlegen. Die Standardnachrichtenklasse für ausgehende Nachrichten ist IPM. 
  
Legen Sie das MSGFLAG_UNSENT-Flag in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft fest. Legen Sie, falls gewünscht, auch die MSGFLAG_READ-und MSGFLAG_UNMODIFIED-Flags fest. Das Festlegen des MSGFLAG_UNMODIFIED ermöglicht es einer Nachricht Unterkomposition, eine zugestellte Nachricht zu simulieren. MSGFLAG_UNMODIFIED kann nur von Clients festgelegt werden, bevor eine Nachricht zum ersten Mal gespeichert wurde. 
  
Wenn Sie bereit sind, eine dauerhafte Kopie einer nicht gesendeten Nachricht zu erstellen, rufen Sie [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) für die Nachricht und alle zugehörigen Anlagen auf. Wenn Sie die Nachricht sofort senden möchten, müssen Sie **SaveChanges**nicht aufrufen. Der Aufruf von **SubmitMessage** speichert die Nachricht intern als Teil ihrer Verarbeitung. 
  
Beim Aufrufen **** von SaveChanges empfiehlt es sich, das KEEP_OPEN_READWRITE-Flag anzugeben, mit dem die Nachricht zu einem späteren Zeitpunkt geändert werden kann. Weitere Settable-Flags sind FORCE_SAVE, was darauf hinweist, dass die Nachricht oder Anlage nach dem Commit der Änderungen geschlossen werden soll, KEEP_OPEN_READONLY, was bedeutet, dass keine weiteren Änderungen vorgenommen werden, und die Kennzeichnung, die es dem Nachrichtenspeicher Anbieter ermöglichen soll, Batch Clientanforderungen, MAPI_DEFERRED_ERRORS.
  
Es ist wichtig, dass Sie **SaveChanges** für jede Anlage in der Nachricht aufrufen, bevor **** Sie SaveChanges für die Nachricht aufrufen. Wenn Sie eine Anlage nicht speichern, wird die Anlage nicht in die Nachricht aufgenommen, wenn Sie gesendet wird, und Sie wird nicht in der Anlagentabelle der Nachricht angezeigt. Wenn Sie die Nachricht nach dem Speichern aller Anlagen nicht speichern, gehen sowohl die Nachricht als auch die Anlagen verloren. 
  
Wenn **SaveChanges** aufgerufen wird, aktualisiert der Nachrichtenspeicher Anbieter die folgenden Eigenschaften: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) Listet alle primären Empfänger auf.
    
- **PR_DISPLAY_TO** listet alle Empfänger von Kohlenstoff Kopien auf. 
    
- **PR_DISPLAY_BCC** ([Pidtagdisplaybcc (](pidtagdisplaybcc-canonical-property.md)) Listet alle Blind Carbon Copy-Empfänger auf.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** legt MSGFLAG_HASATTACH fest, wenn eine oder mehrere Anlagen gespeichert wurden, und löscht MSGFLAG_UNMODIFIED, um anzuzeigen, dass die Nachricht geändert wurde. 
    
- **PR_MESSAGE_SIZE** ([Pidtagmessagesize (](pidtagmessagesize-canonical-property.md)) enthält die aktuelle Größe der Nachricht.
    
- **PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md)) ermöglicht den Zugriff auf die Attachment-Tabelle.
    
- **PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) ermöglicht den Zugriff auf die Empfängertabelle.
    
Einige Nachrichteneigenschaften werden in der Regel von Clients oder Dienstanbietern bereitgestellt, wenn eine Nachricht erstellt wird. Wenn ein Client diese Einstellung vernachlässigt, muss der Nachrichtenspeicher Anbieter Sie zu dem Zeitpunkt aktualisieren, zu dem SaveChanges aufgerufen **** wird. Wenn beispielsweise die Eigenschaften **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) einer Nachricht beim Erstellen der Nachricht festgelegt wurden, müssen Sie nicht zu einem bestimmten Zeitpunkt geändert werden. Nachrichtenspeicher Anbieter, die Sie bei der Nachrichtenerstellung nicht festlegen, müssen Sie jedoch beim ersten Aufruf von **SaveChanges** festlegen. 
  
Wenn **SaveChanges** MAPI_E_CORRUPT_DATA zurückgibt, gehen Sie davon aus, dass die gespeicherten Daten jetzt verloren gehen. Nachrichtenspeicher Anbieter, die ein Client-Server-Modell für Ihre Implementierung verwenden, können diesen Wert zurückgeben, wenn eine Netzwerkverbindung verloren geht oder der Server nicht aktiv ist. Bevor Sie einen Fehler an den Benutzer zurückgeben, versuchen Sie, die Daten ein zweites Mal zu schreiben und zu speichern **** , indem Sie SetProps gefolgt von einem weiteren Aufruf von **SaveChanges**aufrufen. Wenn die Daten lokal zwischengespeichert werden, sollte dies kein Problem darstellen. Wenn jedoch kein lokaler Cache vorhanden ist oder wenn der zweite **SaveChanges** -Aufruf fehlschlägt, wird ein Fehler angezeigt, um den Benutzer auf das Problem hinzuweisen. 
  

