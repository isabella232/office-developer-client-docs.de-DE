---
title: Sortieren und Kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 12668cb87f21b56cd398a7b5375f6a4b40c65829
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581531"
---
# <a name="sorting-and-categorization"></a>Sortieren und Kategorisieren

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Sortieren einer Tabelle platziert Zeilen in einer Bestellung, die für den Viewer sinnvoll sind. Angenommen, möchten ein Betrachter finden in der Inhaltstabelle eines Ordners sortiert nach Betreff der Nachricht, damit alle Threads einer Unterhaltung beieinander während einer anderen Viewer die Nachrichten, die nach dem Namen des Absenders sortiert sollten. Eine Tabelle neu instanziierte ist nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Es gibt zwei Arten von sortieren:
  
- Standard-Sortierung
    
- Kategorisiert sortieren 
    
Mit standard sortieren, werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Mit kategorisierten sortieren, werden die Zeilen mit einer oder mehreren Spalten als Sortierschlüssel hierarchisch angezeigt. Innerhalb jeder Kategorie ist eine spezielle Überschriftenzeile, die die folgenden Spalten enthält.
  
- Die Spalte oder Spalten, die den Sortierschlüssel bilden
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Unter der Überschriftszeile eingezogen werden alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit den Sortierschlüssel übereinstimmen. Diese Zeilen werden die Zeilen Endknoten bezeichnet. Endknoten Zeilen enthalten alle Spalten in der Spalte minus Sortierschlüsselspalten festgelegt. 
  
In den Tabellen Inhalt von Ordnern unterstützen häufig kategorisierte Sortierung zusätzlich zum standard sortieren. In den Tabellen Inhalt der Address Book Container unterstützen in der Regel nur standard sortieren. 
  
Eine Kategorie kann zwei Zustände haben: reduziert und erweitert. Wenn eine Kategorie im reduzierten Zustand befindet, wird nur die Kopfzeile von [IMAPITable::QueryRows](imapitable-queryrows.md)zurückgegeben. Wenn eine Kategorie im erweiterten Zustand befindet, werden alle Zeilen im Zusammenhang mit der Kategorie zurückgegeben. Dazu gehören die Kopfzeile und die untergeordneten Zeilen. 
  
Jeder Kategorie in einer Tabellenansicht kann erweitert oder reduziert unabhängig voneinander. D. h., müssen nicht alle Kategorien in dem Zustand zur selben Zeit sein. Einige Kategorien können reduziert werden, während andere erweitert werden. 
  
Der Benutzer einer kategorisierten Tabelle entscheidet, wie es angezeigt wird. Option für eine gemeinsame ist die Verwendung ein Steuerelements im Windows SDK bezeichnet das Treeview-Steuerelement bereitgestellt. TreeView-Steuerelemente sind Listenfelder, die Informationen in einer Baumstruktur unterstützen. Überschriftenzeilen für Kategorien im erweiterten Zustand werden mit einem Minuszeichen gekennzeichnet, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen (+) markiert sind. Mit den Endknoten Zeilen unter der Überschriftenzeilen eingezogen werden erweiterte Kategorien angezeigt. 
  
Um zu reduzieren und erweitern eine Kategorie, eine Clientanwendung oder Service Provider verwendet die folgenden [IMAPITable: IUnknown](imapitableiunknown.md) Methoden: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie unter den folgenden Themen:
  
- [SSortOrder](ssortorder.md)
    
- [PidTagSubject (kanonische Eigenschaft)](pidtagsubject-canonical-property.md)
    
- [PidTagSubjectPrefix (kanonische Eigenschaft)](pidtagsubjectprefix-canonical-property.md)
    
- [PidTagNormalizedSubject (kanonische Eigenschaft)](pidtagnormalizedsubject-canonical-property.md)
    
- [PidTagConversationTopic (kanonische Eigenschaft)](pidtagconversationtopic-canonical-property.md)
    
- [PidTagConversationIndex (kanonische Eigenschaft)](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Sortieren von Tabellen nach dem Festlegen der Spalten und Einschränkungen](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

