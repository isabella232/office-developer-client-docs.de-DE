---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439723"
---
# <a name="ssortorder"></a>SSortOrder
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert, wie die Zeilen einer Tabelle sortiert werden, welche Spalte als Sortiertaste verwendet werden soll, und die Sortierrichtung. 
  
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

## <a name="members"></a>Elemente

**ulPropTag**
  
> Eigenschaftstag, das den Sortierschlüssel oder für eine kategorisierte Sortierung die Kategoriespalte identifiziert.
    
**ulOrder**
  
> Die Reihenfolge, in der die Daten sortiert werden sollen. Mögliche Werte sind wie folgt:
    
  - TABLE_SORT_ASCEND: Die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_COMBINE: Der Sortiervorgang sollte eine Kategorie erstellen, die die eigenschaft, die als Sortierschlüsselspalte im **ulPropTag-Element** identifiziert ist, mit der Sortierschlüsselspalte kombiniert, die in der vorherigen **SSortOrder-Struktur angegeben** ist. 
      
    TABLE_SORT_COMBINE kann nur verwendet werden, wenn die **SSortOrder-Struktur** als Eintrag in einer [SSortOrderSet-Struktur](ssortorderset.md) verwendet wird, um mehrere Sortierreihenfolgen für eine kategorisierte Sortierung anzugeben. TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder-Struktur** in einer **SSortOrderSet-Struktur verwendet** werden. 
      
  - TABLE_SORT_DESCEND: Die Tabelle sollte in absteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_CATEG_MAX: Die Tabelle sollte nach dem Maximalwert des **ulPropTag-Members** für die Datenzeilen in den Kategorien sortiert werden, die durch die vorherige Sortierreihenfolge in der **SSortOrderSet-Struktur angegeben** wurden. 
      
  - TABLE_SORT_CATEG_MIN: Die Tabelle sollte nach dem Minimalwert des **ulPropTag-Members** für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der **SSortOrderSet-Struktur** angegeben sind. 
    
## <a name="remarks"></a>Hinweise

Eine **SSortOrder-Struktur** wird verwendet, um zu beschreiben, wie sie entweder einen Standardsortierungsvorgang oder einen kategorisierten Sortiervorgang ausführen. **SSortOrder-Strukturen** werden in der Regel in einer **SSortOrderSet-Struktur** kombiniert, um mehrere Sortiertasten und Wegbeschreibungen zu beschreiben. **SSortOrderSet-Strukturen** werden in den folgenden Funktionen und Schnittstellenmethoden verwendet: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Der Bereich der zulässigen Spalten in einer Tabelle, die als Sortierschlüssel verwendet werden können, hängt vom Anbieter ab. Spalten, die Teil des aktuellen Spaltensatzes sind, können immer als Sortiertasten verwendet werden. Jeder Anbieter bestimmt jedoch, ob Sortierschlüssel mithilfe verfügbarer Spalten definiert werden können, die sich nicht im aktuellen Spaltensatz befinden. Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable::QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn TBL_ALL_COLUMNS festgelegt ist. 
  
Das **ulOrder-Element** gibt sowohl Richtungsreihenfolge als auch Kategorisierungsinformationen an, z. B. nach Unterhaltung ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), d. h. Unterhaltungsthread, bei dem es sich um eine Reihe von Nachrichten und Antworten handelt. Zeilen können entweder in aufsteigender oder absteigender Reihenfolge sortiert werden, und alle NULL-Einträge werden zuletzt positioniert. 
  
Der TABLE_SORT_COMBINE gibt an, dass die in **ulPropTag** angegebene Spalte mit der vorherigen Kategoriespalte kombiniert werden soll, um eine zusammengesetzte Kategorie zu bilden. Das heißt, anstatt eindeutige Werte einzelner Spalten zu kategorisieren, TABLE_SORT_COMBINE die Kategorisierung für eindeutige Werte einer Spaltenkombination möglich. Beispielsweise kann eine einzelne Kategorie definiert werden, um Nachrichten zu gruppieren, die von einem bestimmten Absender eines bestimmten Betreffs empfangen werden. Wenn Sie den Wert auf TABLE_SORT_COMBINE reduziert sich die Anzahl der angezeigten Kategoriezeilen. 
  
Das Sortieren nach mehrwertigen Spalten wird nicht von allen Tabellenimplementierungen universell unterstützt. Wenn unterstützt, wenden Sie das MV_FLAG mithilfe des makros MVI_PROP auf das Eigenschaftstag im **ulPropTag-Element** an, um den Sortierschlüssel als mehrwertige Spalte zu identifizieren. Die Sortierung nach einer mehrwertigen Spalte basiert auf der Verwendung der einzelnen Werte. 
  
> [!IMPORTANT]
> Die **ulOrder-Memberwerte** TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Werte hinzufügen: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Weitere Informationen zur standard- und kategorisierten Sortierung finden Sie unter [Sorting and Categorization](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [MAPI-Strukturen](mapi-structures.md)

