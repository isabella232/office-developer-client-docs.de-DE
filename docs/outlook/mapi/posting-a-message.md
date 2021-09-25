---
title: Veröffentlichen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44137ffcab25ace7e93d92a735bca4a1c1186c24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609621"
---
# <a name="posting-a-message"></a>Veröffentlichen einer Nachricht

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Posten einer Nachricht ähnelt dem Senden einer Nachricht. Der Hauptunterschied ist das Ziel. Anstatt an einen oder mehrere Empfänger in einem oder mehreren Messagingsystemen weitergeleitet zu werden, verbleibt eine gepostete Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.
  
### <a name="to-post-a-message"></a>So posten Sie eine Nachricht
  
1. Öffnen Sie den Zielordner, indem [Sie IMsgStore::OpenEntry](imsgstore-openentry.md)aufrufen. Wenn der Zielordner der Posteingang ist, suchen Sie den Eintragsbezeichner, der an **OpenEntry** übergeben werden soll, indem [Sie IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)aufrufen. 
    
2. Rufen Sie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf, um die Nachricht zu erstellen. 
    
3. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Nachricht auf, um Folgendes festzulegen: 
    
   - Das flag MSGFLAG_READ in der **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)) -Eigenschaft.
    
   - Die **PR_SENDER** Eigenschaften. 
    
   - Die **PR_SENT_REPRESENTING** Eigenschaften. 
    
   - The **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)) property.
    
   - Die **eigenschaft PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Die **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) -Eigenschaft.
    
   - Die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft.
    
   - Alle für die Nachrichtenklasse erforderlichen Eigenschaften.
    
4. Rufen Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) der Nachricht auf, um die Nachricht zu speichern. 
    
5. Erstellen Sie bei Bedarf eine Anlage, legen Sie deren Eigenschaften fest, und speichern Sie sie. Weitere Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Erstellen einer Nachrichtenanlage.](creating-a-message-attachment.md)
    
6. Rufen Sie **IMessage::SaveChanges** auf, um die Nachricht zu speichern. An diesem Punkt wird es im Inhaltsverzeichnis des Zielordners angezeigt. 
    
Beachten Sie, dass Sie keine Empfängerliste erstellen. Stattdessen legen Sie mehrere Eigenschaften fest, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt werden. 
  
Wenn Sie eine Nachricht zeitweise speichern möchten, bevor sie im Inhaltsverzeichnis des sichtbaren Ordners angezeigt wird, erstellen Sie sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie sie dann in den Zielordner. 
  

