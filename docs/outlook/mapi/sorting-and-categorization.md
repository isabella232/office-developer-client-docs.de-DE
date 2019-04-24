---
title: Sortieren und kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344506"
---
# <a name="sorting-and-categorization"></a>Sortieren und kategorisieren

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Sortieren einer Tabelle werden Zeilen in einer Reihenfolge platziert, die für den Betrachter sinnvoll ist. Beispielsweise könnte ein Betrachter die Inhaltstabelle eines Ordners nach Nachrichtenbetreff sortiert anzeigen, sodass alle Threads einer Unterhaltung zusammen sind, während ein anderer Betrachter die Nachrichten nach dem Namen des Absenders sortieren kann. Eine neu instanziierte Tabelle ist nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Es gibt zwei Arten der Sortierung:
  
- Standard Sortierung
    
- Kategorisierte Sortierung 
    
Bei der Standardsortierung werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Bei der kategorisierten Sortierung werden die Zeilen hierarchisch mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Innerhalb jeder Kategorie gibt es eine spezielle Überschriftenzeile mit den folgenden Spalten.
  
- Die Spalten, aus denen der Sortierschlüssel besteht
    
- **PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([Pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([Pidtagrowtype (](pidtagrowtype-canonical-property.md)) 
    
Eingerückt unter der Überschriftenzeile befinden sich alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit dem Sortierschlüssel übereinstimmen. Diese Zeilen werden als Blattzeilen bezeichnet. Blattzeilen enthalten alle Spalten in der Spaltengruppe minus der Sortierschlüsselspalten. 
  
Die Inhaltsordner Verzeichnisse unterstützen häufig kategorisierte Sortierungen zusätzlich zur Standardsortierung. Die Inhaltstabellen der Adressbuchcontainer unterstützen in der Regel nur die Standardsortierung. 
  
Eine Kategorie kann zwei Zustände aufweisen: reduziert und erweitert. Wenn sich eine Kategorie im reduzierten Zustand befindet, wird nur die Überschriftenzeile von [IMAPITable:: QueryRows](imapitable-queryrows.md)zurückgegeben. Wenn sich eine Kategorie im erweiterten Zustand befindet, werden alle mit der Kategorie verknüpften Zeilen zurückgegeben. Dazu gehören die Überschriftenzeile und die Blattzeilen. 
  
Jede Kategorie in einer Tabellenansicht kann unabhängig voneinander erweitert oder reduziert werden. Das heißt, nicht alle Kategorien müssen gleichzeitig in demselben Zustand sein; Einige Kategorien können reduziert werden, während andere erweitert werden. 
  
Der Benutzer einer kategorisierten Tabelle entscheidet, wie er angezeigt wird. Eine gängige Option ist die Verwendung eines Steuerelements, das im Windows SDK mit dem Namen TreeView-Steuerelement bereitgestellt wird. TreeView-Steuerelemente sind Listenfelder, die Informationen in einer baumartigen Struktur unterstützen. Überschriftenzeilen für Kategorien im erweiterten Zustand sind mit einem Minuszeichen gekennzeichnet, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen gekennzeichnet sind. Erweiterte Kategorien werden mit eingezogenen Blattzeilen unter der Überschriftenzeile angezeigt. 
  
Zum reduzieren und Erweitern einer Kategorie verwendet eine Clientanwendung oder ein Dienstanbieter die folgenden [IMAPITable: IUnknown](imapitableiunknown.md) -Methoden: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie in den folgenden Themen:
  
- [SSortOrder](ssortorder.md)
    
- [Kanonische PidTagSubject-Eigenschaft](pidtagsubject-canonical-property.md)
    
- [Kanonische Pidtagsubjectprefix (-Eigenschaft](pidtagsubjectprefix-canonical-property.md)
    
- [Kanonische PidTagNormalizedSubject-Eigenschaft](pidtagnormalizedsubject-canonical-property.md)
    
- [Kanonische Eigenschaftpidtagconversationtopic-Eigenschaft](pidtagconversationtopic-canonical-property.md)
    
- [Kanonische PidTagConversationIndex-Eigenschaft](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

