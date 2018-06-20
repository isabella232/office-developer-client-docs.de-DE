---
title: Speichern einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e61a72691309b2ac632b764c0607f5b1e36b291b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795423"
---
# <a name="saving-a-message"></a>Speichern einer Nachricht

  
  
**Betrifft**: Outlook 
  
Vor dem Speichern einer Nachricht call-Clients in der Regel die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um einige Eigenschaften neben der Nachricht Texteigenschaften, Eigenschaften für Dateianlage, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und Eigenschaften festzulegen die Empfängerliste zugeordnet sind.
  
Legen Sie die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft auf eine Zeichenfolge wie IPM. Beachten Sie, die die Klasse der ausgehenden Nachricht beschreibt. Obwohl Clients **PR_MESSAGE_CLASS** für alle ausgehenden Nachrichten festgelegt werden soll, ist ein Standardwert von der Nachricht Informationsdienst bereitgestellt, wenn sie nicht festgelegt. Die Standardnachrichtenklasse für ausgehende Nachrichten ist IPM. 
  
Legen Sie das MSGFLAG_UNSENT-Flag in der Eigenschaft **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Legen Sie bei Bedarf auch die Flags MSGFLAG_READ und MSGFLAG_UNMODIFIED. Festlegen der MSGFLAG_UNMODIFIED ermöglicht eine Nachricht verfasst simuliert eine gesendete Nachricht. MSGFLAG_UNMODIFIED kann nur von Clients festgelegt werden, bevor eine Meldung zum ersten Mal gespeichert wurde. 
  
Wenn Sie eine dauerhafte Kopie einer Nachricht nicht gesendeten stellen möchten, rufen Sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) auf die Nachricht und alle zugehörigen Anlagen. Wenn Sie die Nachricht sofort senden möchten, müssen Sie nicht **SaveChanges**aufrufen. Der Aufruf von **SubmitMessage** speichert intern die Nachricht als Teil der Verarbeitung. 
  
Beim Aufruf von **SaveChanges**, ist es ratsam, die Kennzeichen KEEP_OPEN_READWRITE angeben, die sodass Sie die Nachricht zu einem späteren Zeitpunkt geändert werden können. Andere einstellbare Flags enthalten FORCE_SAVE, die angibt, dass die Nachricht oder Anlage geschlossen werden soll, nachdem Änderungen ein Commit ausgeführt werden, KEEP_OPEN_READONLY, gibt an, dass keine weiteren Änderungen vorgenommen werden soll, und das Kennzeichen aus, um der Nachricht Informationsdienst ermöglichen Batch-Clientanforderungen, MAPI_DEFERRED_ERRORS.
  
Es ist wichtig, dass Sie vor dem Aufruf von **SaveChanges** für die Nachricht **SaveChanges** für jede Anlage der Nachricht aufrufen. Wenn Sie nicht zum Speichern einer Anlage, werden die Anlage nicht in der Nachricht enthalten, wenn sie gesendet und wird nicht in der Nachricht Anlagentabelle angezeigt werden. Wenn Sie nicht die Nachricht nach dem Speichern aller Anlagen speichern, werden die Nachricht und die Anlagen verloren. 
  
Wenn **SaveChanges** aufgerufen wird, aktualisiert der Anbieter für die Nachricht Anmelden die folgenden Eigenschaften: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) werden alle primären Empfänger aufgelistet.
    
- **PR_DISPLAY_TO** Listet alle Cc-Empfänger. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) Listet alle Bcc-Empfänger.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** MSGFLAG_HASATTACH festgelegt, wenn eine oder mehrere Anlagen gespeichert wurden und löscht MSGFLAG_UNMODIFIED, um anzuzeigen, dass die Nachricht geändert wurde. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) enthält die aktuelle Größe der Nachricht.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) bietet Zugriff auf die Anlagentabelle.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) bietet Zugriff auf die Empfänger Tabelle.
    
Einige Nachrichteneigenschaften werden in der Regel von Clients oder -Dienstanbieter bereitgestellt, wenn eine Nachricht erstellt wird. Wenn ein Client nicht festgelegt, ist es bis zu der Nachricht Informationsdienst zur Zeit aktualisieren, wenn **SaveChanges** aufgerufen wird. Beispielsweise, wenn einer Nachricht **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Eigenschaften festgelegt wurden, wenn eine Nachricht erstellt wurde, müssen sie nicht am sparen Sie Zeit geändert werden. Jedoch müssen Nachricht-Anbieter, die sie bei der Erstellung der Nachricht festgelegt nicht sie beim ersten festlegen, die **SaveChanges** aufgerufen wird. 
  
Wenn **SaveChanges** MAPI_E_CORRUPT_DATA zurückgibt, wird davon ausgegangen Sie, dass die Daten gespeichert werden jetzt verloren. Nachricht-Anbieter, die für die Implementierung einer Client-Server-Objektmodell verwenden können diese-Wert zurück, bei eine-Verbindung oder der Server nicht ausgeführt wird. Versuchen Sie vor der Rückgabe eines Fehlers für den Benutzer, schreiben und speichern die Daten ein zweites Mal durch einen Aufruf **SetProps** gefolgt von einem anderen Aufruf von **SaveChanges**. Wenn die Daten lokal zwischengespeichert werden, sollte dies nicht auf ein Problem sein. Jedoch keine lokaler Cache vorhanden ist oder der zweite **SaveChanges** -Aufruf fehlschlägt, um den Benutzer auf das Problem ein Fehler angezeigt. 
  

