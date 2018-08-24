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
ms.openlocfilehash: a4245b5dd1b70d4cf695190c65b447cf92566ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574482"
---
# <a name="selecting-a-receive-folder"></a>Auswählen eines Empfangsordners

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Empfangsordner ist in der eingehende Nachrichten von einer bestimmten Klasse platziert werden. IPM und verwandte Berichtnachrichten weist MAPI Standard Empfangsordner im Posteingang. IPK und verwandte Berichtnachrichten weist MAPI Standard Empfangsordner im Stammordner des Nachrichtenspeichers. Sie können diese Zuordnungen ändern oder zusätzliche Aufgaben für andere Nachrichtenklassen machen. Explizites Ordner Aufgaben empfangen, für der Client des unterstützten Nachricht Klassen ist optional.
  
Wenn eine eingehende Nachrichtenklasse nicht mit einer zugewiesenen Empfangsordner verfügt, verwendet der Speicheranbieter Nachricht automatisch den Empfangsordner für die Klasse, die das längsten mögliche Präfix der eingehenden-Klasse entspricht. Wenn beispielsweise der Client eine Nachricht der Klasse IPM empfängt. Note.MyDocument und die einzige erhalten Ordner, die hergestellt wurde ist der Posteingang für IPM-Nachrichten, diese Meldung wird im Posteingang platziert werden, da IPM. Note.MyDocument wird von der Basisklasse IPM abgeleitet.
  
Wenn Sie eine Empfangsordner für IPK Nachrichten zuordnen möchten, verwenden Sie einen Ordner aus der IPM-Unterstruktur niemals. Diese Ordner sollten für Nachrichten nur IPM reserviert werden. Verwenden Sie stattdessen einen Ordner wie, der ursprüngliche wird im Stammordner der Nachrichtenspeicher. 
  
 **Erstellen eines Ordners empfangen für eine Nachrichtenklasse IPM**
  
1. Rufen Sie den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) mit **PR_IPM_SUBTREE_ENTRYID** als die Eintrags-ID, um den Stammordner der IPM-Unterstruktur im Nachrichtenspeicher zu öffnen. 
    
3. Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) zum Erstellen des Ordners empfangen. 
    
4. Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) , um den neuen Ordner der Nachrichtenklasse IPM zuzuordnen. 
    
 **Erstellen eines Ordners empfangen für eine Nachrichtenklasse IPK**
  
1. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) mit eine null Eintrags-ID, um den Stammordner des Nachrichtenspeichers zu öffnen. 
    
2. Rufen Sie [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) zum Erstellen des Ordners empfangen. 
    
3. Rufen Sie [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) , um den neuen Ordner die Nachrichtenklasse IPK zuzuordnen. 
    
Weisen Sie den Empfangsordner, den Sie für Nachrichten für verwandte Berichtnachrichten verwenden. Wenn beispielsweise Ihr Client IPM empfängt. Hinweis Nachrichten, richten Sie eine Empfangsordner für zukünftige IPM. Hinweis Nachrichten und die gleiche Empfangsordner für zukünftige Report.IPM.Note Nachrichten.
  

