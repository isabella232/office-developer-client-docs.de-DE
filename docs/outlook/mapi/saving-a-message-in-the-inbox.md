---
title: Speichern einer Nachricht im Posteingang
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e79133ed4928495dcf75b59877a82d3228773883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586284"
---
# <a name="saving-a-message-in-the-inbox"></a>Speichern einer Nachricht im Posteingang

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **Eine Nachricht im Posteingang ohne Empfänger speichern**
  
1. Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um die Eintrags-ID des Posteingangs abzurufen. 
    
2. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen des Posteingangs und einen Zeiger darauf abrufen. 
    
3. Rufen Sie den Posteingang [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Nachricht zu erstellen. 
    
4. Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_SUBJECT** ([ hinzuzufügen. PidTagSubject](pidtagsubject-canonical-property.md)) Eigenschaften. 
    
5. Erstellen Sie jede Anlage, legen Sie dessen Eigenschaften, und speichern Sie es. Ausführliche Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).
    
6. Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern. Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Posteingangs angezeigt. 
    
Wenn eine Nachricht abwechselnd zu speichern, bevor er in der Inhaltstabelle des Posteingangs angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen, und klicken Sie dann in den Posteingang verschieben. 
  

