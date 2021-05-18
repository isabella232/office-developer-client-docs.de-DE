---
title: Anzeigen einer Ordnerinhaltstabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412394"
---
# <a name="displaying-a-folder-contents-table"></a>Anzeigen einer Ordnerinhaltstabelle

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Inhaltsverzeichnis eines Ordners enthält Zusammenfassende Informationen zu allen nachrichten. Zusammenfassungsinformationen zu neuen eingehenden Nachrichten werden im Inhaltsverzeichnis des Empfangsordners für die Nachrichtenklasse angezeigt. Um diese Informationen benutzern zur Verfügung zu stellen, rufen Sie die Tabelle ab, und zeigen Sie die Spalten und Zeilen entsprechend an.
  
**So zeigen Sie eine Ordnerinhaltstabelle an**
  
1. Rufen [Sie IMsgStore::OpenEntry](imsgstore-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Ordners, der die Tabelle enthält.
    
2. Rufen Sie die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners auf, um die Inhaltstabelle zu öffnen. 
    
3. Beschränken Sie die Ansicht der Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Tabelle aufrufen, um bestimmte Spalten anzugeben. 
    
4. Beschränken Sie die Ansicht der Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) der Tabelle aufrufen, um bestimmte Zeilen zu filtern. Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen möchten, die noch gelesen werden müssen: 
    
    1. Erstellen Sie eine Eigenschaftseinschränkung in einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) die der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft mit der gewünschten Nachrichtenklasse entspricht. 
        
    2. Erstellen Sie eine Bitmaskeneinschränkung in einer [SBitMaskRestriction-Struktur,](sbitmaskrestriction.md) die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als Eigenschaftstag und den MSGFLAG_UNREAD-Wert als Maske verwendet.
        
    3. Erstellen Sie eine Einschränkung in einer [SAndRestriction-Struktur,](sandrestriction.md) die der Eigenschaft und den Bitmaskeneinschränkungen beitritt. 
    
5. Sortieren Sie die Inhaltstabelle bei Bedarf, indem Sie die [IMAPITable::SortTable-Methode der Tabelle](imapitable-sorttable.md) aufrufen. 
    
6. Rufen [Sie IMAPITable::QueryRows auf,](imapitable-queryrows.md) um alle Zeilen aus der Inhaltstabelle zur Verarbeitung abzurufen. 
    

