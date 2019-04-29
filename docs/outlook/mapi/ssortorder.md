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
  
Definiert, wie die Zeilen einer Tabelle, die Spalte, die als Sortierschlüssel verwendet werden soll, und die Richtung der Sortierung sortiert werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Eigenschaftentag, der den Sortierschlüssel oder für eine kategorisierte Sortierung die Spalte Category identifiziert.
    
**ulOrder**
  
> Die Reihenfolge, in der die Daten sortiert werden sollen. Folgende Werte sind möglich:
    
  - TABLE_SORT_ASCEND: die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_COMBINE: der Sortiervorgang sollte eine Kategorie erstellen, die die Eigenschaft, die als Sortierschlüsselspalte im **ulPropTag** -Element identifiziert wurde, mit der in der vorherigen **SSortOrder** -Struktur angegebenen Sortierschlüsselspalte kombiniert. 
      
    TABLE_SORT_COMBINE kann nur verwendet werden, wenn die **SSortOrder** -Struktur als Eintrag in einer [SSortOrderSet](ssortorderset.md) -Struktur verwendet wird, um mehrere Sortierreihenfolgen für eine kategorisierte Sortierung anzugeben. TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder** -Struktur in einer **SSortOrderSet** -Struktur verwendet werden. 
      
  - TABLE_SORT_DESCEND: die Tabelle sollte in absteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_CATEG_MAX: die Tabelle sollte nach dem Maximalwert des **ulPropTag** -Elements für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der **SSortOrderSet** -Struktur angegeben sind. 
      
  - TABLE_SORT_CATEG_MIN: die Tabelle sollte nach dem Minimalwert des **ulPropTag** -Elements für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der in **SSortOrderSet** -Struktur angegeben sind. 
    
## <a name="remarks"></a>Bemerkungen

Eine **SSortOrder** -Struktur wird verwendet, um die Ausführung eines Standard Sortiervorgangs oder eines kategorisierten Sortiervorgangs zu beschreiben. **SSortOrder** -Strukturen werden in der Regel in einer **SSortOrderSet** -Struktur kombiniert, um mehrere Sortierschlüssel und-Richtungen zu beschreiben. **SSortOrderSet** -Strukturen werden in den folgenden Funktionen und Schnittstellenmethoden verwendet: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Der zulässige Spalten Umfang in einer Tabelle, der als Sortierschlüssel verwendet werden kann, hängt vom Anbieter ab. Spalten, die Teil des aktuellen Spaltensatzes sind, können immer als Sortierschlüssel verwendet werden. Jeder Anbieter bestimmt jedoch, ob Sortierschlüssel mithilfe verfügbarer Spalten definiert werden können, die nicht in der aktuellen Spaltengruppe enthalten sind. Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable:: QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn das TBL_ALL_COLUMNS-Flag festgelegt ist. 
  
Das **ulOrder** -Element gibt sowohl Richtungs Reihenfolge-als auch Kategorisierungsinformationen an, beispielsweise nach Unterhaltung ([eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), also konversationsthread, bei dem es sich um eine Reihe von Nachrichten und Antworten handelt. Zeilen können in aufsteigender oder absteigender Reihenfolge mit allen NULL-Einträgen in der letzten Position sortiert werden. 
  
Der TABLE_SORT_COMBINE-Wert gibt an, dass die in **ulPropTag** angegebene Spalte mit der vorherigen Kategorie-Spalte kombiniert werden soll, um eine zusammengesetzte Kategorie zu bilden. Anstatt jedoch auf eindeutigen Werten einzelner Spalten zu kategorisieren, ermöglicht TABLE_SORT_COMBINE die Kategorisierung von eindeutigen Werten einer Kombination von Spalten. Beispielsweise kann eine einzelne Kategorie definiert werden, um Nachrichten zu gruppieren, die von einem bestimmten Absender zu einem bestimmten Betreff empfangen wurden. Wenn Sie den Wert auf TABLE_SORT_COMBINE festlegen, wird die Anzahl der angezeigten Kategorie-Zeilen reduziert. 
  
Das Sortieren von mehrwertigen Spalten wird von allen Tabellen Implementierungen nicht universell unterstützt. Wenn Sie unterstützt werden, wenden Sie das MV_FLAG mithilfe des MVI_PROP-Makros auf das Property-Tag im **ulPropTag** -Element an, um den Sortierschlüssel als mehrwertige Spalte zu identifizieren. Das Sortieren in einer mehrwertigen Spalte basiert auf der Verwendung der einzelnen Werte. 
  
> [!IMPORTANT]
> Die **ulOrder** -Elementwerte TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie Sie mit den folgenden Werten zu Ihrem Code hinzufügen: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Weitere Informationen zu standardmäßigen und kategorisierten Sortierungen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [MAPI-Strukturen](mapi-structures.md)

