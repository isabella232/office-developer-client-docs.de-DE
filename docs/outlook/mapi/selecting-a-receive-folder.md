---
title: Auswählen eines Empfangs Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339725"
---
# <a name="selecting-a-receive-folder"></a>Auswählen eines Empfangs Ordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Empfangsordner ist der Speicherort eingehender Nachrichten einer bestimmten Klasse. Bei IPM-und verwandten Berichtnachrichten weist MAPI den Posteingang als standardmäßigen Empfangsordner zu. Für IPC und zugehörige Berichtnachrichten weist MAPI den Stammordner des Nachrichtenspeichers als standardmäßigen Empfangsordner zu. Sie können diese Zuordnungen ändern oder zusätzliche Zuordnungen für andere Nachrichtenklassen vornehmen. Die explizite Zuweisung von Empfangs Ordnern für die unterstützten Nachrichtenklassen des Clients ist optional.
  
Wenn für eine Klasse für eingehende Nachrichten kein Empfangsordner zugewiesen ist, verwendet der Nachrichtenspeicher Anbieter automatisch den Ordner Receive für die Klasse, die mit dem längsten möglichen Präfix der eingehenden Klasse übereinstimmt. Wenn Ihr Client beispielsweise eine Nachricht der Klasse IPM erhält. Hinweis. myDocument und der einzige empfangene Ordner, der eingerichtet wurde, ist der Posteingang für IPM-Nachrichten, diese Nachricht wird im Posteingang abgelegt, da IPM. Hinweis. myDocument wird von der Basisklasse IPM abgeleitet.
  
Wenn Sie einen Empfangsordner für IPC-Nachrichten zuweisen, verwenden Sie niemals einen Ordner aus der IPM-Unterstruktur. Diese Ordner sollten nur für IPM-Nachrichten reserviert werden. Verwenden Sie stattdessen einen Ordner, der im Stammordner des Nachrichtenspeichers enthalten ist. 
  
 **So erstellen Sie einen Empfangsordner für eine IPM-Nachrichtenklasse**
  
1. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Nachrichtenspeichers auf, um die **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft abzurufen. 
    
2. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als Eintragsbezeichner auf, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen. 
    
3. Rufen Sie [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen. 
    
4. Rufen Sie [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner der IPM-Nachrichtenklasse zuzuordnen. 
    
 **So erstellen Sie einen Empfangsordner für eine IPC-Nachrichtenklasse**
  
1. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md) mit einer NULL-Eintrags-ID auf, um den Stammordner des Nachrichtenspeichers zu öffnen. 
    
2. Rufen Sie [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) auf, um den Empfangsordner zu erstellen. 
    
3. Rufen Sie [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) auf, um den neuen Ordner der IPC-Nachrichtenklasse zuzuordnen. 
    
Weisen Sie den empfangenen Ordner, den Sie für Nachrichten verwenden, für Verwandte Berichtnachrichten zu. Wenn Ihr Client beispielsweise IPM. Hinweis Nachrichten, Einrichten eines Empfangs Ordners für zukünftige IPM. Hinweis Nachrichten und derselbe Empfänger Ordner für zukünftige Berichte. IPM. Note-Nachrichten.
  

