---
title: Sortieren und Kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: f7431bf9b6212ebda0a590962a7a74b2945ae6f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578564"
---
# <a name="sorting-and-categorization"></a>Sortieren und Kategorisieren

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Sortieren einer Tabelle werden Zeilen in einer Reihenfolge platziert, die für den Betrachter sinnvoll ist. Ein Betrachter möchte z. B. das Inhaltsverzeichnis eines Ordners nach Nachrichtenbetreff sortiert anzeigen, sodass alle Threads einer Unterhaltung zusammen sind, während ein anderer Betrachter die Nachrichten nach dem Namen des Absenders sortieren möchte. Eine neu instanziierte Tabelle wird nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Es gibt zwei Arten der Sortierung:
  
- Standardsortierung
    
- Kategorisierte Sortierung 
    
Bei der Standardsortierung werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Bei der kategorisierten Sortierung werden die Zeilen hierarchisch mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Innerhalb jeder Kategorie gibt es eine spezielle Überschriftenzeile, die die folgenden Spalten enthält.
  
- Die Spalten, aus denen die Sortiertasten bestehen
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Eingezogen unter der Überschriftenzeile sind alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die der Sortiertaste entsprechen. Diese Zeilen werden als Blattzeilen bezeichnet. Blattzeilen enthalten alle Spalten in der Spaltengruppe ohne die Spalten mit Sortierschlüsseln. 
  
Die Inhaltsverzeichnisse von Ordnern unterstützen häufig die kategorisierte Sortierung zusätzlich zur Standardsortierung. Die Inhaltsverzeichnisse von Adressbuchcontainern unterstützen in der Regel nur die Standardsortierung. 
  
Eine Kategorie kann zwei Zustände aufweisen: reduziert und erweitert. Wenn sich eine Kategorie im reduzierten Zustand befindet, wird nur die Überschriftenzeile von [IMAPITable::QueryRows](imapitable-queryrows.md)zurückgegeben. Wenn sich eine Kategorie im erweiterten Zustand befindet, werden alle Zeilen im Zusammenhang mit der Kategorie zurückgegeben. Dies schließt die Überschriftenzeile und die Blattzeilen ein. 
  
Jede Kategorie in einer Tabellenansicht kann unabhängig voneinander erweitert oder reduziert werden. Das heißt, nicht alle Kategorien müssen sich gleichzeitig im selben Zustand befinden; Einige Kategorien können reduziert werden, während andere erweitert werden. 
  
Der Benutzer einer kategorisierten Tabelle entscheidet, wie sie angezeigt wird. Eine gängige Option ist die Verwendung eines Steuerelements, das im Windows SDK bereitgestellt wird, das als Strukturansichtssteuerelement bezeichnet wird. Strukturansichtssteuerelemente sind Listenfelder, die Informationen in einer strukturähnlichen Struktur unterstützen. Überschriftenzeilen für Kategorien im erweiterten Zustand werden mit einem Minuszeichen markiert, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen gekennzeichnet sind. Erweiterte Kategorien werden angezeigt, wobei die Blattzeilen unter den Überschriftenzeilen eingezogen sind. 
  
Zum Reduzieren und Erweitern einer Kategorie verwendet eine Clientanwendung oder ein Dienstanbieter die folgenden [IMAPITable: IUnknown-Methoden:](imapitableiunknown.md) 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Weitere Informationen zum Sortieren der Threads einer Unterhaltung finden Sie in den folgenden Themen:
  
- [SSortOrder](ssortorder.md)
    
- [PidTagSubject (kanonische Eigenschaft)](pidtagsubject-canonical-property.md)
    
- [PidTagSubjectPrefix (kanonische Eigenschaft)](pidtagsubjectprefix-canonical-property.md)
    
- [PidTagNormalizedSubject (kanonische Eigenschaft)](pidtagnormalizedsubject-canonical-property.md)
    
- [PidTagConversationTopic (kanonische Eigenschaft)](pidtagconversationtopic-canonical-property.md)
    
- [Kanonische PidTagConversationIndex-Eigenschaft](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

