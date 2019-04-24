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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339935"
---
# <a name="displaying-a-folder-contents-table"></a>Anzeigen einer Ordnerinhaltstabelle

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Inhaltstabelle eines Ordners enthält zusammenfassende Informationen zu allen Nachrichten. Zusammenfassende Informationen zu neuen eingehenden Nachrichten werden in der Tabelle Inhalt des Empfänger Ordners für die Nachrichtenklasse angezeigt. Um diese Informationen Benutzern zur Verfügung zu stellen, rufen Sie die Tabelle ab, und zeigen Sie die Spalten und Zeilen entsprechend an.
  
**So zeigen Sie eine Ordnerinhaltstabelle an**
  
1. Rufen Sie [IMsgStore:: OpenEntry](imsgstore-openentry.md)auf, und übergeben Sie den Eintragsbezeichner des Ordners, der die Tabelle enthält.
    
2. Rufen Sie die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode des Ordners auf, um die Inhaltstabelle zu öffnen. 
    
3. Schränken Sie die Ansicht der Inhaltstabelle auf Wunsch ein, indem Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Tabelle aufrufen, um bestimmte Spalten anzugeben. 
    
4. Begrenzen Sie die Ansicht der Inhaltstabelle auf Wunsch, indem Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode der Tabelle zum Filtern bestimmter Zeilen aufrufen. Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen möchten, die noch nicht gelesen werden müssen: 
    
    1. Erstellen Sie eine Eigenschaftseinschränkung in einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, die mit der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft mit der gewünschten Nachrichtenklasse übereinstimmt. 
        
    2. Erstellen Sie eine Bitmasken Einschränkung in einer [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur, die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als Property-Tag und den MSGFLAG_UNREAD-Wert als Maske verwendet.
        
    3. Erstellen Sie eine Einschränkung in einer [SAndRestriction](sandrestriction.md) -Struktur, die die Eigenschaften-und Bitmasken Einschränkungen verknüpft. 
    
5. Sortieren Sie die Inhaltstabelle nach Bedarf, indem Sie die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode der Tabelle aufrufen. 
    
6. Rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) auf, um alle Zeilen aus der Tabelle Contents zur Verarbeitung abzurufen. 
    

