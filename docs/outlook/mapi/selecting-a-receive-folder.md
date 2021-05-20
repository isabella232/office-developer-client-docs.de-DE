---
title: Auswählen eines Empfangsordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428417"
---
# <a name="selecting-a-receive-folder"></a>Auswählen eines Empfangsordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einem Empfangsordner werden eingehende Nachrichten einer bestimmten Klasse platziert. Für IPM- und zugehörige Berichtsnachrichten weist MAPI den Posteingang als Standard-Empfangsordner zu. Für IPC- und zugehörige Berichtsnachrichten weist MAPI den Stammordner des Nachrichtenspeichers als Standard-Empfangsordner zu. Sie können diese Zuordnungen ändern oder zusätzliche Zuordnungen für andere Nachrichtenklassen erstellen. Die explizite Zuweisung von Empfangsordnern für die unterstützten Nachrichtenklassen Ihres Clients ist optional.
  
Wenn einer eingehenden Nachrichtenklasse kein Empfangsordner zugewiesen ist, verwendet der Nachrichtenspeicheranbieter automatisch den Empfangsordner für die Klasse, die dem längsten möglichen Präfix der eingehenden Klasse entspricht. Wenn Ihr Client z. B. eine Nachricht der Klasse IPM empfängt. Note.MyDocument und der einzige Empfangsordner, der eingerichtet wurde, ist der Posteingang für IPM-Nachrichten, diese Nachricht wird im Posteingang platziert, da IPM. Note.MyDocument leitet sich von der Basisklasse IPM ab.
  
Wenn Sie einen Empfangsordner für IPC-Nachrichten zuweisen, verwenden Sie niemals einen Ordner aus der IPM-Unterstruktur. Diese Ordner sollten nur für IPM-Nachrichten reserviert werden. Verwenden Sie stattdessen einen Ordner, der im Stammordner des Nachrichtenspeichers enthalten ist. 
  
 **So erstellen Sie einen Empfangsordner für eine IPM-Nachrichtenklasse**
  
1. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des **Nachrichtenspeichers** auf, um die PR_IPM_SUBTREE_ENTRYID ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) -Eigenschaft abzurufen. 
    
2. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als Eintrags-ID auf, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen. 
    
3. Rufen [Sie IMAPIFolder::CreateFolder auf,](imapifolder-createfolder.md) um den Empfangsordner zu erstellen. 
    
4. Rufen [Sie IMsgStore::SetReceiveFolder auf,](imsgstore-setreceivefolder.md) um den neuen Ordner Ihrer IPM-Nachrichtenklasse zu zuordnungen. 
    
 **So erstellen Sie einen Empfangsordner für eine IPC-Nachrichtenklasse**
  
1. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md) mit einem Nulleintragsbezeichner auf, um den Stammordner des Nachrichtenspeichers zu öffnen. 
    
2. Rufen [Sie IMAPIFolder::CreateFolder auf,](imapifolder-createfolder.md) um den Empfangsordner zu erstellen. 
    
3. Rufen [Sie IMsgStore::SetReceiveFolder auf,](imsgstore-setreceivefolder.md) um den neuen Ordner Ihrer IPC-Nachrichtenklasse zu zuordnungen. 
    
Weisen Sie den Empfangsordner zu, den Sie für Nachrichten für verwandte Berichtsnachrichten verwenden. Beispiel: Wenn Ihr Client IPM empfängt. Notieren Sie Nachrichten, richten Sie einen Empfangsordner für zukünftige IPM ein. Notieren Sie Nachrichten und denselben Empfangsordner für zukünftige Report.IPM.Note-Nachrichten.
  

