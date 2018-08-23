---
title: Bereitstellen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577520"
---
# <a name="posting-a-message"></a>Bereitstellen einer Nachricht

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bereitstellen einer Nachricht ähnelt dem Senden einer Nachricht. Der Hauptunterschied ist das Ziel. Statt weitergeleitet werden ein oder mehrere Empfänger über eine oder mehrere von Messagingsystemen, bleibt eine bereitgestellte Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.
  
### <a name="to-post-a-message"></a>Zum Übermitteln einer Nachricht
  
1. Öffnen Sie den Zielordner durch Aufrufen von [IMsgStore::OpenEntry](imsgstore-openentry.md). Wenn der Zielordner des Posteingangs ist, suchen Sie die Eintrags-ID durch Aufrufen von [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)an **OpenEntry** übergeben. 
    
2. Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) , um die Nachricht zu erstellen. 
    
3. Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode festgelegt: 
    
   - Das Flag MSGFLAG_READ in der Eigenschaft **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Die **PR_SENDER** -Eigenschaften. 
    
   - Die **PR_SENT_REPRESENTING** -Eigenschaften. 
    
   - Die Eigenschaft **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - Das **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die Eigenschaft **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Die Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - Die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Alle Eigenschaften, die von der Nachrichtenklasse erforderlich.
    
4. Rufen Sie die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die Nachricht zu speichern. 
    
5. Falls erforderlich, erstellen Sie eine Anlage, legen Sie dessen Eigenschaften und speichern Sie es. Weitere Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).
    
6. Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern. Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Zielordners angezeigt. 
    
Beachten Sie, dass Sie keine Empfängerliste erstellen. Stattdessen legen Sie verschiedene Eigenschaften, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt sind. 
  
Wenn eine Nachricht speichern zeitweise bevor er in der Inhaltstabelle des Ordners "sichtbar" angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen und anschließend in den Zielordner verschieben. 
  

