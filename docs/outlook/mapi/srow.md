---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410434"
---
# <a name="srow"></a>SRow

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Zeile aus einer Tabelle, die ausgewählte Eigenschaften für ein bestimmtes Objekt enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Elemente

**ulAdrEntryPad**
  
> Padding bytes to properly align the property values pointed to the **lpProps** member. 
    
**cValues**
  
> Anzahl der Eigenschaftswerte, auf die **von lpProps verwiesen wird.** 
    
**lpProps**
  
> Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die Eigenschaftswerte für die Spalten in der Zeile beschreiben. 
    
## <a name="remarks"></a>Hinweise

Eine **SRow-Struktur** beschreibt eine Zeile in einer Tabelle. Sie ist in der [TABLE_NOTIFICATION](table_notification.md) enthalten, die eine Tabellenbenachrichtigung begleitet. 
  
**SRow-Strukturen** werden in den folgenden Methoden verwendet: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (viele Methoden) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Wenn mehrere Zeilen beschrieben werden müssen, wird eine [SRowSet-Struktur](srowset.md) verwendet. Eine **SRowSet-Struktur** enthält ein Array von **SRow-Strukturen** und eine Anzahl von Strukturen im Array. 
  
Die folgende Abbildung zeigt die Beziehung zwischen **einem SRow** und einer **SRowSet-Datenstruktur.** 
  
**Beziehung zwischen SRow und SRowSet**
  
![Beziehung zwischen SRow und SRowSet Beziehung](media/amapi_17.gif "zwischen SRow und SRowSet")
  
**SRow-Strukturen** sind identisch mit [ADRENTRY-Strukturen.](adrentry.md) Daher können eine Zeile einer Empfängertabelle und ein Eintrag in einer Adressliste gleich behandelt werden. 
  
Informationen dazu, wie der Arbeitsspeicher für **SRow-Strukturen** zugewiesen werden soll, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)
- [Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

