---
title: Anzeigen einer Tabelle der Ordner-Inhalt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791567"
---
# <a name="displaying-a-folder-contents-table"></a>Anzeigen einer Tabelle der Ordner-Inhalt

**Betrifft**: Outlook 
  
Inhaltstabelle eines Ordners enthält zusammenfassende Informationen zu allen Nachrichten. Zusammenfassende Informationen zu neuen eingehenden Nachrichten in der Inhaltstabelle des Ordners "empfangen" für die Nachrichtenklasse wird angezeigt. Um diese Informationen für Benutzer verfügbar machen, Abrufen der Tabelle und die Spalten und Zeilen nach Bedarf angezeigt.
  
**Zum Anzeigen einer Tabelle der Ordner-Inhalt**
  
1. Rufen Sie [IMsgStore::OpenEntry](imsgstore-openentry.md), die Eintrags-ID des Ordners mit der Tabelle übergeben.
    
2. Rufen Sie den Ordner [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode, um seine Inhaltstabelle zu öffnen. 
    
3. Beschränken Sie Ihre Ansicht der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode bestimmte Spalten angegeben werden. 
    
4. Beschränken Sie Ihre Ansicht der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, um bestimmte Zeilen zu filtern. Wenn Sie beispielsweise nur Nachrichten mit einer bestimmten Nachrichtenklasse anzeigen, die noch nicht gelesen werden möchten: 
    
    1. Erstellen Sie eine eigenschaftseinschränkung in eine [SPropertyRestriction](spropertyrestriction.md) -Struktur, die die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) mit der gewünschten Nachrichtenklasse entspricht. 
        
    2. Erstellen Sie eine Bitmaske Beschränkung in eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur, die **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) als das Eigenschafts-Tag und den Wert MSGFLAG_UNREAD als Maske verwendet wird.
        
    3. Erstellen Sie eine Einschränkung in eine [SAndRestriction](sandrestriction.md) -Struktur, die die Einschränkungen-Eigenschaft und Bitmaske teilnimmt. 
    
5. Sortieren der Inhaltstabelle bei Bedarf durch Aufrufen der Tabelle [SortTable](imapitable-sorttable.md) -Methode. 
    
6. Rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) , um alle Zeilen aus der Inhaltstabelle für die Verarbeitung abzurufen. 
    

