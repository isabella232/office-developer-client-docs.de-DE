---
title: Speichern eine Nachricht im Posteingang
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795414"
---
# <a name="saving-a-message-in-the-inbox"></a>Speichern eine Nachricht im Posteingang

  
  
**Betrifft**: Outlook 
  
 **Eine Nachricht im Posteingang ohne Empfänger speichern**
  
1. Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , um die Eintrags-ID des Posteingangs abzurufen. 
    
2. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) zum Öffnen des Posteingangs und einen Zeiger darauf abrufen. 
    
3. Rufen Sie den Posteingang [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode, um die Nachricht zu erstellen. 
    
4. Rufen Sie die Nachricht [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_SUBJECT** ([ hinzuzufügen. PidTagSubject](pidtagsubject-canonical-property.md)) Eigenschaften. 
    
5. Erstellen Sie jede Anlage, legen Sie dessen Eigenschaften, und speichern Sie es. Ausführliche Informationen zum Hinzufügen von Anlagen von Nachrichten finden Sie unter [Erstellen von E-Mail-Anlagen](creating-a-message-attachment.md).
    
6. Rufen Sie **IMessage::SaveChanges** , um die Nachricht zu speichern. Zu diesem Zeitpunkt wird sie in der Inhaltstabelle des Posteingangs angezeigt. 
    
Wenn eine Nachricht abwechselnd zu speichern, bevor er in der Inhaltstabelle des Posteingangs angezeigt werden soll, stattdessen in einem ausgeblendeten Ordner wie den Stammordner der IPM-Unterstruktur erstellen, und klicken Sie dann in den Posteingang verschieben. 
  

