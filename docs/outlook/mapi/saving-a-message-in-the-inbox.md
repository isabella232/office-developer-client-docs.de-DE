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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357533"
---
# <a name="saving-a-message-in-the-inbox"></a>Speichern einer Nachricht im Posteingang

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So speichern Sie eine Nachricht im Posteingang ohne Empfänger**
  
1. Rufen Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner des Posteingangs abzurufen. 
    
2. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) auf, um den Posteingang zu öffnen und einen Zeiger darauf abzurufen. 
    
3. Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode des Posteingangs auf, um die Nachricht zu erstellen. 
    
4. Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Nachricht auf, um die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)), **PR_HTML** ([pidtaghtml (](pidtaghtml-canonical-property.md)) oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) und **PR_Subject** ([ PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaften. 
    
5. Erstellen Sie jede Anlage, legen Sie Ihre Eigenschaften fest, und speichern Sie Sie. Ausführliche Informationen zum Hinzufügen von Anlagen zu Nachrichten finden Sie unter [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Rufen Sie **IMessage:: SaveChanges** auf, um die Nachricht zu speichern. An dieser Stelle wird es in der Inhaltstabelle des Posteingangs angezeigt. 
    
Wenn Sie eine Nachrichten erkennt speichern möchten, bevor Sie in der Tabelle Inhalt des Posteingangs angezeigt wird, erstellen Sie Sie stattdessen in einem ausgeblendeten Ordner wie dem Stammordner der IPM-Unterstruktur, und verschieben Sie Sie dann in den Posteingang. 
  

