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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350750"
---
# <a name="posting-a-message"></a>Veröffentlichen einer Nachricht

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Veröffentlichen einer Nachricht ähnelt dem Senden einer Nachricht. Der Hauptunterschied ist das Ziel. Anstatt an einen oder mehrere Empfänger über ein oder mehrere Messagingsysteme umgeleitet zu werden, verbleibt eine bereitgestellte Nachricht in einem Ordner im aktuellen Nachrichtenspeicher.
  
### <a name="to-post-a-message"></a>So veröffentlichen Sie eine Nachricht
  
1. Öffnen Sie den Zielordner, indem Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)aufrufen. Wenn der Zielordner der Posteingang ist, suchen Sie nach der Eintrags **** -ID, die an OpenEntry durch Aufrufen von [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Rufen Sie [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) auf, um die Nachricht zu erstellen. 
    
3. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Nachricht auf, um Folgendes festzulegen: 
    
   - Das MSGFLAG_READ-flag in der **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md))-Eigenschaft.
    
   - Die **PR_SENDER** -Eigenschaften. 
    
   - Die **PR_SENT_REPRESENTING** -Eigenschaften. 
    
   - Die **PR_RECEIPT_TIME** ([pidtagreceipttime (](pidtagreceipttime-canonical-property.md))-Eigenschaft.
    
   - Die **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft.
    
   - Die **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft.
    
   - Die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft.
    
   - Alle Eigenschaften, die für die Nachrichtenklasse erforderlich sind.
    
4. Rufen Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode der Nachricht auf, um die Nachricht zu speichern. 
    
5. Erstellen Sie bei Bedarf eine Anlage, legen Sie Ihre Eigenschaften fest, und speichern Sie Sie. Weitere Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Rufen Sie **IMessage:: SaveChanges** auf, um die Nachricht zu speichern. An dieser Stelle wird Sie in der Tabelle Inhalt des Zielordners angezeigt. 
    
Beachten Sie, dass Sie keine Empfängerliste erstellen. Stattdessen legen Sie mehrere Eigenschaften fest, die normalerweise von einem Transportanbieter für eine gesendete Nachricht festgelegt werden. 
  
Wenn Sie eine Nachricht zeitweise speichern möchten, bevor Sie in der Tabelle Inhalt des sichtbaren Ordners angezeigt wird, erstellen Sie Sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie Sie dann in den Zielordner. 
  

