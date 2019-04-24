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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336516"
---
# <a name="srow"></a>SRow

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Zeile aus einer Tabelle, die ausgewählte Eigenschaften für ein bestimmtes Objekt enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Padding Bytes, um die Eigenschaftswerte, auf die durch das **lpProps** -Element verwiesen wird, ordnungsgemäß auszurichten. 
    
**cValues**
  
> Die Anzahl der Eigenschaftswerte, auf die von **lpProps**verwiesen wird. 
    
**lpProps**
  
> Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte für die Spalten in der Zeile beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Eine **SRow** -Struktur beschreibt eine Zeile in einer Tabelle. Sie ist in der [TABLE_NOTIFICATION](table_notification.md) -Struktur enthalten, die einer Tabellenbenachrichtigung beigefügt ist. 
  
**SRow** -Strukturen werden in den folgenden Methoden verwendet: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md) (viele Methoden) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Wenn mehr als eine Zeile beschrieben werden muss, wird eine [SRowSet](srowset.md) -Struktur verwendet. Eine **SRowSet** -Struktur enthält ein Array von **SRow** -Strukturen und die Anzahl der Strukturen im Array. 
  
Die folgende Abbildung zeigt die Beziehung zwischen einer **SRow** und einer **SRowSet** -Datenstruktur. 
  
**Beziehung zwischen SRow und SRowSet**
  
![Beziehung zwischen SRow und SRowSet] (media/amapi_17.gif "Beziehung zwischen SRow und SRowSet")
  
**SRow** -Strukturen sind identisch mit den [Miet](adrentry.md) Strukturen. Daher kann eine Zeile einer Empfängertabelle und ein Eintrag in einer Adressliste gleich behandelt werden. 
  
Informationen dazu, wie der Speicher für **SRow** -Strukturen zugeordnet werden sollte, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)
- [Verwalten von Speicher für ADRLIST-und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

