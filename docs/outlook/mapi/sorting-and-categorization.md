---
title: Sortieren und Kategorisieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418484"
---
# <a name="sorting-and-categorization"></a>Sortieren und Kategorisieren

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Sortieren einer Tabelle werden Zeilen in einer Reihenfolge platziert, die für den Viewer sinnvoll ist. Ein Betrachter möchte beispielsweise das Inhaltsverzeichnis eines Ordners nach Nachrichtenbe betreff sortiert sehen, sodass alle Threads einer Unterhaltung zusammengef?ndet werden, während ein anderer Benutzer die Nachrichten nach dem Namen des Absenders sortieren möchte. Eine neu instanziierte Tabelle ist nicht unbedingt in einer bestimmten Reihenfolge sortiert. 
  
Es gibt zwei Arten von Sortierung:
  
- Standardsortierung
    
- Kategorisierte Sortierung 
    
Bei der Standardsortierung werden alle Zeilen in einer flachen Liste mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. Bei der kategorisierten Sortierung werden die Zeilen hierarchisch mit einer oder mehreren Spalten als Sortierschlüssel angezeigt. In jeder Kategorie befindet sich eine spezielle Überschriftenzeile, die die folgenden Spalten enthält.
  
- Die Spalte oder Spalten, aus der der Sortierschlüssel ist
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Eingerückt unter der Überschriftenzeile sind alle Zeilen aus der Tabelle, die Spalten mit Werten enthalten, die mit dem Sortierschlüssel übereinstimmen. Diese Zeilen werden als Blattzeilen bezeichnet. Blattzeilen enthalten alle Spalten im Spaltensatz minus der Sortierschlüsselspalten. 
  
Die Inhaltstabellen von Ordnern unterstützen häufig die kategorisierte Sortierung zusätzlich zur Standardsortierung. Die Inhaltstabellen von Adressbuchcontainern unterstützen in der Regel nur die Standardsortierung. 
  
Eine Kategorie kann zwei Zustände haben: reduziert und erweitert. Wenn sich eine Kategorie im reduzierten Zustand befindet, wird nur die Überschriftenzeile von [IMAPITable::QueryRows zurückgegeben.](imapitable-queryrows.md) Wenn sich eine Kategorie im erweiterten Zustand befindet, werden alle zeilen im Zusammenhang mit der Kategorie zurückgegeben. Dies umfasst die Überschriftenzeile und die Blattzeilen. 
  
Jede Kategorie in einer Tabellenansicht kann unabhängig voneinander erweitert oder reduziert werden. Das heißt, nicht alle Kategorien müssen gleichzeitig denselben Status haben. Einige Kategorien können reduziert werden, während andere erweitert werden. 
  
Der Benutzer einer kategorisierten Tabelle entscheidet, wie sie angezeigt wird. Eine gängige Option ist die Verwendung eines Steuerelements, das im Windows SDK als Strukturansichtssteuerelement bezeichnet wird. Strukturansichtssteuerelemente sind Listenfelder, die Informationen in einer struktur like structure unterstützen. Überschriftenzeilen für Kategorien im erweiterten Zustand werden mit einem Minuszeichen markiert, während Überschriftenzeilen für Kategorien im reduzierten Zustand mit einem Pluszeichen markiert sind. Erweiterte Kategorien werden angezeigt, wenn die Blattzeilen unter den Überschriftenzeilen eingezogen sind. 
  
Um eine Kategorie zu reduzieren und zu erweitern, verwendet eine Clientanwendung oder ein Dienstanbieter die folgenden [IMAPITable-Methoden: IUnknown-Methoden:](imapitableiunknown.md) 
  
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
    
- [PidTagConversationIndex (kanonische Eigenschaft)](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Sortieren von Tabellen nach dem Festlegen von Spalten und Einschränkungen](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

