---
title: Auswählen eines Empfangsordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5935a559b15cbb0b5149de8b4bed8834cf707f30
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599004"
---
# <a name="selecting-a-receive-folder"></a>Auswählen eines Empfangsordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Empfangsordner ist der Ort, an dem eingehende Nachrichten einer bestimmten Klasse platziert werden. Für IPM- und zugehörige Berichtsnachrichten weist MAPI den Posteingang als Standard-Empfangsordner zu. Für IPC- und zugehörige Berichtsnachrichten weist MAPI den Stammordner des Nachrichtenspeichers als Standard-Empfangsordner zu. Sie können diese Zuordnungen ändern oder zusätzliche Zuordnungen für andere Nachrichtenklassen vornehmen. Explizite Zuweisungen von Empfangsordnern für die vom Client unterstützten Nachrichtenklassen sind optional.
  
Wenn einer Klasse für eingehende Nachrichten kein Empfangsordner zugewiesen ist, verwendet der Nachrichtenspeicheranbieter automatisch den Empfangsordner für die Klasse, die dem längsten möglichen Präfix der eingehenden Klasse entspricht. Wenn Ihr Client beispielsweise eine Nachricht der Klasse "IPM" empfängt. Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM. Note.MyDocument wird von der Basisklasse IPM abgeleitet.
  
Wenn Sie einen Empfangsordner für IPC-Nachrichten zuweisen, verwenden Sie niemals einen Ordner aus der IPM-Unterstruktur. Diese Ordner sollten nur für IPM-Nachrichten reserviert sein. Verwenden Sie stattdessen einen Ordner, der im Stammordner des Nachrichtenspeichers enthalten ist. 
  
 **So erstellen Sie einen Empfangsordner für eine IPM-Nachrichtenklasse**
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Nachrichtenspeichers auf, um die **eigenschaft PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) abzurufen. 
    
2. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als Eintragsbezeichner auf, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen. 
    
3. Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen. 
    
4. Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner Ihrer IPM-Nachrichtenklasse zuzuordnen. 
    
 **So erstellen Sie einen Empfangsordner für eine IPC-Nachrichtenklasse**
  
1. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit einem NULL-Eintragsbezeichner auf, um den Stammordner des Nachrichtenspeichers zu öffnen. 
    
2. Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen. 
    
3. Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner Ihrer IPC-Nachrichtenklasse zuzuordnen. 
    
Weisen Sie den Empfangsordner zu, den Sie für Nachrichten für verwandte Berichtsnachrichten verwenden. Beispielsweise, wenn Ihr Client IPM empfängt. Beachten Sie Nachrichten, richten Sie einen Empfangsordner für zukünftige IPM ein. Notieren Sie Nachrichten und den gleichen Empfangsordner für zukünftige Report.IPM.Note-Nachrichten.
  

