---
title: Anzeigen einer Ordnerinhaltstabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 16b238d28ac059fc3fa5f1e172beba3a077cc96d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596591"
---
# <a name="displaying-a-folder-contents-table"></a>Anzeigen einer Ordnerinhaltstabelle

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Inhaltsverzeichnis eines Ordners enthält Zusammenfassende Informationen zu allen Nachrichten. Zusammenfassungsinformationen zu neuen eingehenden Nachrichten werden im Inhaltsverzeichnis des Empfangsordners für die Nachrichtenklasse angezeigt. Um diese Informationen benutzern zur Verfügung zu stellen, rufen Sie die Tabelle ab, und zeigen Sie die Spalten und Zeilen nach Bedarf an.
  
**So zeigen Sie ein Ordnerinhaltsverzeichnis an**
  
1. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Ordners, der die Tabelle enthält.
    
2. Rufen Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners auf, um das Inhaltsverzeichnis zu öffnen. 
    
3. Beschränken Sie die Ansicht der Inhaltstabelle, wenn gewünscht, indem Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Tabelle aufrufen, um bestimmte Spalten anzugeben. 
    
4. Beschränken Sie die Ansicht des Inhaltsverzeichnisses, wenn gewünscht, indem Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) der Tabelle aufrufen, um bestimmte Zeilen zu filtern. Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen möchten, die noch nicht gelesen werden müssen: 
    
    1. Erstellen Sie eine Eigenschaftseinschränkung in einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) die der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft mit der gewünschten Nachrichtenklasse entspricht. 
        
    2. Erstellen Sie eine Bitmaskeneinschränkung in einer [SBitMaskRestriction-Struktur,](sbitmaskrestriction.md) die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als Eigenschaftstag und den MSGFLAG_UNREAD-Wert als Maske verwendet.
        
    3. Erstellen Sie eine Einschränkung in einer [SAndRestriction-Struktur,](sandrestriction.md) die die Eigenschafts- und Bitmaskeneinschränkungen verknüpft. 
    
5. Sortieren Sie das Inhaltsverzeichnis, wenn gewünscht, indem Sie die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) der Tabelle aufrufen. 
    
6. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) auf, um alle Zeilen aus dem Inhaltsverzeichnis zur Verarbeitung abzurufen. 
    

