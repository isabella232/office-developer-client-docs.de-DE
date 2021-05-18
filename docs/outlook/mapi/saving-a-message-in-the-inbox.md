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
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407893"
---
# <a name="saving-a-message-in-the-inbox"></a>Speichern einer Nachricht im Posteingang

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So speichern Sie eine Nachricht im Posteingang ohne Empfänger**
  
1. Rufen [Sie IMsgStore::GetReceiveFolder auf,](imsgstore-getreceivefolder.md) um die Eintrags-ID des Posteingangs abzurufen. 
    
2. Rufen [Sie IMsgStore::OpenEntry auf,](imsgstore-openentry.md) um den Posteingang zu öffnen und einen Zeiger auf den Posteingang abzurufen. 
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) des Posteingangs auf, um die Nachricht zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Nachricht auf, um die **Eigenschaften PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) hinzuzufügen. 
    
5. Erstellen Sie jede Anlage, legen Sie ihre Eigenschaften und speichern Sie sie. Ausführliche Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Rufen **Sie IMessage::SaveChanges auf,** um die Nachricht zu speichern. An diesem Punkt wird sie im Inhaltsverzeichnis des Posteingangs angezeigt. 
    
Wenn Sie eine Nachricht intermittant speichern möchten, bevor sie im Inhaltsverzeichnis des Posteingangs angezeigt wird, erstellen Sie sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie sie dann in den Posteingang. 
  

