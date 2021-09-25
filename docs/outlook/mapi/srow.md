---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c88cb2425e44844de4fc127a1b97ad5dc9ed851a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566493"
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

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> Byte auffüllen, um die Eigenschaftswerte, auf die der **lpProps-Member verweist,** ordnungsgemäß auszurichten. 
    
**cValues**
  
> Anzahl der Eigenschaftswerte, auf die von **lpProps** verwiesen wird. 
    
**lpProps**
  
> Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die die Eigenschaftswerte für die Spalten in der Zeile beschreiben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **SRow-Struktur** beschreibt eine Zeile in einer Tabelle. Sie ist in der [TABLE_NOTIFICATION](table_notification.md) Struktur enthalten, die mit einer Tabellenbenachrichtigung verbunden ist. 
  
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
  
Die folgende Abbildung zeigt die Beziehung zwischen einer **SRow-** und einer **SRowSet-Datenstruktur.** 
  
**Beziehung zwischen SRow und SRowSet**
  
![Beziehung zwischen SRow und SRowSet](media/amapi_17.gif "Beziehung zwischen SRow und SRowSet")
  
**SRow-Strukturen** werden genauso definiert wie [ADRENTRY-Strukturen.](adrentry.md) Daher können eine Zeile einer Empfängertabelle und ein Eintrag in einer Adressliste gleich behandelt werden. 
  
Informationen dazu, wie der Speicher für **SRow-Strukturen** zugewiesen werden soll, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)
- [Verwalten des Arbeitsspeichers für ADRLIST- und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

