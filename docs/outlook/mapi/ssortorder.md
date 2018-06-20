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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7cb511c7a021c4e65214acc7efa785be0e02ffc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795622"
---
# <a name="ssortorder"></a>SSortOrder
 
**Betrifft**: Outlook 
  
Definiert, wie die Zeilen einer Tabelle, nach welcher Spalte die Sortierschlüssel und die Richtung der Sortierung als verwendet zu sortieren. 
  
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
  
> Eigenschafts-Tag, die die Sortierung wichtige oder für eine kategorisierte Sortierung die Kategorie-Spalte identifiziert.
    
**ulOrder**
  
> Die Reihenfolge, in der die Daten sortiert werden sollen. Mögliche Werte sind wie folgt:
    
  - TABLE_SORT_ASCEND: Die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_COMBINE: Der Sortiervorgang sollte eine Kategorie erstellen, die die Eigenschaft als die Sortierung Schlüsselspalte im **UlPropTag** -Member mit die Sortierung Schlüsselspalte angegeben, in der vorherigen **SSortOrder** Struktur identifiziert kombiniert. 
      
    TABLE_SORT_COMBINE kann nur verwendet werden, wenn die Struktur **SSortOrder** an mehrere Sortierreihenfolgen für eine kategorisierte Sortierung als Einstiegspunkt in einer [SSortOrderSet](ssortorderset.md) Struktur verwendet wird. TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder** Struktur in einer **SSortOrderSet** Struktur verwendet werden. 
      
  - TABLE_SORT_DESCEND: Die Tabelle sollte in absteigender Reihenfolge sortiert werden.
      
  - TABLE_SORT_CATEG_MAX: Die Tabelle sollten auf den maximalen Wert des Elements **UlPropTag** für Datenzeilen in den durch die vorherigen Sortierreihenfolge in der Struktur **SSortOrderSet** angegebenen Kategorien sortiert werden. 
      
  - TABLE_SORT_CATEG_MIN: Die Tabelle sollten auf den minimalen Wert des Elements **UlPropTag** für Datenzeilen in den durch die vorherigen Sortierreihenfolge in der Struktur der in **SSortOrderSet** angegebenen Kategorien sortiert werden. 
    
## <a name="remarks"></a>Hinweise

Eine **SSortOrder** -Struktur wird verwendet, um wird beschrieben, wie Sie einen standard Sortiervorgang oder ein kategorisierten Sortiervorgang durchführen. **SSortOrder** Strukturen werden in eine **SSortOrderSet** -Struktur, die mehrere Sortierschlüsseln und erfahren Sie, wie beschrieben in der Regel zusammengefasst. **SSortOrderSet** Strukturen werden in die folgenden Funktionen und Interface-Methoden verwendet: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Der Bereich der zulässigen Spalten in einer Tabelle, die als Sortierschlüssel verwendet werden kann, hängt von den Anbieter ab. Spalten, die Teil der aktuellen Spalte sind können immer als Sortierschlüssel verwendet werden. Jedoch bestimmt jeder Anbieter, ob Sortierschlüssel definiert werden können, mithilfe von Verfügbare Spalten, die nicht in der aktuellen Spalte festgelegt sind. Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable::QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn das Flag TBL_ALL_COLUMNS festgelegt ist. 
  
Die **UlOrder** Datenmember gibt Richtungspfeile Reihenfolge und Kategorisierungsinformationen, beispielsweise nach Unterhaltungen ([Eigenschaftpidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), d. h., gesprochene Thread, der eine Reihe von Nachrichten und Antworten ist. Zeilen können in ein aufsteigender oder absteigender Reihenfolge mit zuletzt positioniert alle NULL-Einträge sortiert werden. 
  
Der Wert TABLE_SORT_COMBINE gibt an, dass in **UlPropTag** angegebene Spalte mit der vorherigen Kategoriespalte zu eine zusammengesetzte Kategorie bilden kombiniert werden soll. D. h., können Sie statt auf eindeutige Werte der einzelnen Spalten kategorisieren, TABLE_SORT_COMBINE zur Kategorisierung auf eindeutige Werte aus einer Kombination von Spalten. Beispielsweise könnte eine einzelne Kategorie auf Gruppennachrichten aus einem bestimmten Absender auf ein bestimmtes Thema definiert werden. Festlegen des Werts auf TABLE_SORT_COMBINE Reduzierung der Anzahl von Kategorien in Zeilen, die angezeigt werden. 
  
Mehrwertige Spalten sortieren wird universell von allen Implementierungen der Tabelle nicht unterstützt. Unterstützt, wenden Sie die MV_FLAG verwenden das Makro MVI_PROP das Eigenschafts-Tag im **UlPropTag** -Member zum Identifizieren des Sortierschlüssels als mehrwertige Spalte. Sortieren nach einer Spalte mit mehreren Werten basiert auf die einzelnen Werte verwenden. 
  
> [!IMPORTANT]
> Die **UlOrder** Memberwerte TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN möglicherweise nicht in der herunterladbaren Headerdatei definiert werden derzeit ist, in diesem Fall können Sie diesen Code mithilfe der folgenden Werte hinzufügen: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Weitere Informationen zu Standard- und kategorisierten Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [MAPI-Strukturen](mapi-structures.md)

