---
title: Veröffentlichen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429768"
---
# <a name="posting-a-message"></a>Veröffentlichen einer Nachricht

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Veröffentlichen einer Nachricht ähnelt dem Senden einer Nachricht. Der Hauptunterschied ist das Ziel. Anstatt über ein oder mehrere Messagingsysteme an einen oder mehrere Empfänger geleitet zu werden, verbleibt eine gepostete Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.
  
### <a name="to-post-a-message"></a>So posten Sie eine Nachricht
  
1. Öffnen Sie den Zielordner, indem Sie [IMsgStore::OpenEntry aufrufen.](imsgstore-openentry.md) Wenn der Zielordner der Posteingang ist, suchen Sie den Eintragsbezeichner, der an **OpenEntry** übergeben werden soll, indem Sie [IMsgStore::GetReceiveFolder aufrufen.](imsgstore-getreceivefolder.md) 
    
2. Rufen [Sie IMAPIFolder::CreateMessage auf,](imapifolder-createmessage.md) um die Nachricht zu erstellen. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Nachricht auf, um dies zu festlegen: 
    
   - Das MSGFLAG_READ in der **PidTagMessageFlags** ( PR_MESSAGE_FLAGS ) [-Eigenschaft.](pidtagmessageflags-canonical-property.md)
    
   - Die **PR_SENDER** Eigenschaften. 
    
   - Die **PR_SENT_REPRESENTING** Eigenschaften. 
    
   - Die **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) -Eigenschaft.
    
   - Die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft.
    
   - Die **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) -Eigenschaft.
    
   - Die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft.
    
   - Alle eigenschaften, die für die Nachrichtenklasse erforderlich sind.
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode der](imapiprop-savechanges.md) Nachricht auf, um die Nachricht zu speichern. 
    
5. Erstellen Sie bei Bedarf eine Anlage, legen Sie ihre Eigenschaften und speichern Sie sie. Weitere Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Rufen **Sie IMessage::SaveChanges auf,** um die Nachricht zu speichern. An diesem Punkt wird sie im Inhaltsverzeichnis des Zielordners angezeigt. 
    
Beachten Sie, dass Sie keine Empfängerliste erstellen. Stattdessen legen Sie mehrere Eigenschaften fest, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt werden. 
  
Wenn Sie eine Nachricht zeitweise speichern möchten, bevor sie im Inhaltsverzeichnis des sichtbaren Ordners angezeigt wird, erstellen Sie sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie sie dann in den Zielordner. 
  

