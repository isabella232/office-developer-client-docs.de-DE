---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aec93300a567ddb9ba946ef6bd646fdd21001f3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566423"
---
# <a name="ssortorder"></a>SSortOrder
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert, wie die Zeilen einer Tabelle sortiert werden, welche Spalte als Sortierschlüssel verwendet werden soll und in welcher Richtung sortiert werden soll. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Eigenschaftstag, das den Sortierschlüssel oder für eine kategorisierte Sortierung die Kategoriespalte identifiziert.
    
**ulOrder**
  
> Die Reihenfolge, in der die Daten sortiert werden sollen. Die folgenden Werte sind möglich:
    
  - TABLE_SORT_ASCEND: Die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_COMBINE: Der Sortiervorgang sollte eine Kategorie erstellen, die die Als Sortierschlüsselspalte im **ulPropTag-Element** identifizierte Eigenschaft mit der in der vorherigen **SSortOrder-Struktur** angegebenen Sortierschlüsselspalte kombiniert. 
      
    TABLE_SORT_COMBINE kann nur verwendet werden, wenn die **SSortOrder-Struktur** als Eintrag in einer [SSortOrderSet-Struktur](ssortorderset.md) verwendet wird, um mehrere Sortierreihenfolgen für eine kategorisierte Sortierung anzugeben. TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder-Struktur** in einer **SSortOrderSet-Struktur** verwendet werden. 
      
  - TABLE_SORT_DESCEND: Die Tabelle sollte in absteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_CATEG_MAX: Die Tabelle sollte nach dem Maximalwert des **ulPropTag-Elements** für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der **SSortOrderSet-Struktur** angegeben wurden. 
      
  - TABLE_SORT_CATEG_MIN: Die Tabelle sollte nach dem Minimalwert des **ulPropTag-Elements** für die Datenzeilen in den Kategorien sortiert werden, die durch die vorherige Sortierreihenfolge in der Struktur "in **SSortOrderSet"** angegeben wurden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **SSortOrder-Struktur** wird verwendet, um zu beschreiben, wie ein Standardsortiervorgang oder ein kategorisierter Sortiervorgang ausgeführt wird. **SSortOrder-Strukturen** werden in der Regel in einer **SSortOrderSet-Struktur** kombiniert, um mehrere Sortierschlüssel und Wegbeschreibungen zu beschreiben. **SSortOrderSet-Strukturen** werden in den folgenden Funktionen und Schnittstellenmethoden verwendet: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Der Bereich der zulässigen Spalten in einer Tabelle, die als Sortierschlüssel verwendet werden kann, hängt vom Anbieter ab. Spalten, die Teil des aktuellen Spaltensatzes sind, können immer als Sortierschlüssel verwendet werden. Jeder Anbieter bestimmt jedoch, ob Sortierschlüssel mithilfe verfügbarer Spalten definiert werden können, die nicht im aktuellen Spaltensatz enthalten sind. Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable::QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn das TBL_ALL_COLUMNS-Flag festgelegt ist. 
  
Der **ulOrder-Member** gibt sowohl direktionale Reihenfolge als auch Kategorisierungsinformationen an, z. B. nach Unterhaltung ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), d. h. Unterhaltungsthread, bei dem es sich um eine Reihe von Nachrichten und Antworten handelt. Zeilen können in aufsteigender oder absteigender Reihenfolge sortiert werden, wobei alle NULL-Einträge zuletzt positioniert sind. 
  
Der wert TABLE_SORT_COMBINE gibt an, dass die in **ulPropTag** angegebene Spalte mit der vorherigen Kategoriespalte kombiniert werden soll, um eine zusammengesetzte Kategorie zu bilden. Das heißt, anstatt eindeutige Werte einzelner Spalten zu kategorisieren, ermöglicht TABLE_SORT_COMBINE die Kategorisierung eindeutiger Werte einer Kombination von Spalten. Beispielsweise kann eine einzelne Kategorie definiert werden, um Nachrichten zu gruppieren, die von einem bestimmten Absender für einen bestimmten Betreff empfangen wurden. Durch Festlegen des Werts auf TABLE_SORT_COMBINE wird die Anzahl der angezeigten Kategoriezeilen reduziert. 
  
Das Sortieren nach mehrwertigen Spalten wird nicht von allen Tabellenimplementierungen universell unterstützt. Wenn dies unterstützt wird, wenden Sie die MV_FLAG mithilfe des makros MVI_PROP auf das Eigenschaftentag im **ulPropTag-Element** an, um den Sortierschlüssel als mehrwertige Spalte zu identifizieren. Die Sortierung nach einer mehrwertigen Spalte basiert auf der Verwendung der einzelnen Werte. 
  
> [!IMPORTANT]
> Die **ulOrder-Memberwerte** TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mit den folgenden Werten hinzufügen: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Weitere Informationen zur standard- und kategorisierten Sortierung finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md) 
  
## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [MAPI-Strukturen](mapi-structures.md)

