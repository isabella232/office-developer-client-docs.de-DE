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
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795627"
---
# <a name="srow"></a>SRow

**Betrifft**: Outlook 
  
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
  
> Abstand Bytes, um die Eigenschaftswerte ordnungsgemäß ausrichten auf das durch die **LpProps** Mitglied. 
    
**cValues**
  
> Anzahl der Eigenschaftswerte, die auf die **LpProps**zeigt. 
    
**lpProps**
  
> Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die die Eigenschaftswerte für die Spalten in der Zeile zu beschreiben. 
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **SRow** beschreibt eine Zeile in einer Tabelle. Es ist in der Struktur [TABLE_NOTIFICATION](table_notification.md) enthalten, die eine Benachrichtigung über eine Tabelle begleitet. 
  
**SRow** Strukturen werden in den folgenden Methoden verwendet: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md) (viele Methoden) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Wenn mehr als eine Zeile werden beschrieben muss, wird eine [SRowSet](srowset.md) -Struktur verwendet. Eine **SRowSet** -Struktur enthält ein Array von **SRow** Strukturen und Anzahl der Strukturen im Array. 
  
Die folgende Abbildung zeigt die Beziehung zwischen einem **SRow** und eine **SRowSet** -Datenstruktur. 
  
**Beziehung zwischen SRow und SRowSet**
  
![Beziehung zwischen SRow und SRowSet] (media/amapi_17.gif "Beziehung zwischen SRow und SRowSet")
  
**SRow** Strukturen definiert sind identisch mit [ADRENTRY](adrentry.md) Strukturen. Aus diesem Grund kann eine Zeile mit einem Empfänger Tabelle und einen Eintrag in einer Adressliste die gleiche Weise behandelt. 
  
Informationen dazu, wie der Speicher für **SRow** Strukturen zugewiesen werden sollten finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [MAPI-Strukturen](mapi-structures.md)
- [Verwalten von Speicher für ADRLIST- und SRowSet-Strukturen](managing-memory-for-adrlist-and-srowset-structures.md)

