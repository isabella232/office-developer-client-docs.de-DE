---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82fa1b0af504cc4774b1dc077a6ef48378740d26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580677"
---
# <a name="srowset"></a>SRowSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SRow](srow.md) -Strukturen. Jede **SRow** Struktur beschreibt eine Zeile aus einer Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Elemente

 **cRows**
  
> Anzahl der **SRow** Strukturen im **aRow** -Member. 
    
 **aRow**
  
> Array von Strukturen **SRow** . Es ist eine Struktur für jede Zeile in der Tabelle. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Struktur **' srowset '** wird verwendet, um mehrere Zeilen von Daten aus einer Tabelle zu beschreiben. **SRowSet** Strukturen werden in der [IAddrBook](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)und [IMAPITable](imapitableiunknown.md) -Schnittstellenmethoden, zusätzlich zu den folgenden Funktionen verwendet: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **SRowSet** Strukturen definiert sind identisch mit [ADRLIST](adrlist.md) -Strukturen, die die Zeilen einer Tabelle Empfänger und die Einträge in einer Adressliste sein dürfen die gleiche behandelt. **SRowSet** Strukturen und **ADRLIST** Strukturen können an Methoden wie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook::Address](iaddrbook-address.md)übergeben werden. 
  
Darüber hinaus sind die Regeln für die Zuweisung von virtuellem Speicher für **SRowSet** Strukturen die gleichen wie bei **ADRLIST** -Strukturen. Zusammenfassend lässt sich sagen, muss jede [SPropValue](spropvalue.md) Struktur im Array zum Festlegen von der **LpProps** Mitglied jede Zeile in der Zeile gezeigt separat mithilfe [MAPIAllocateBuffer](mapiallocatebuffer.md)zugeordnet werden. Jede Eigenschaft Wert Struktur muss auch using [MAPIFreeBuffer](mapifreebuffer.md) vor der Freigabe der **SRowSet** -Struktur, sodass keine Verweise auf die zugewiesenen **SPropValue** Strukturen verloren freigegeben werden. Eine Zeile werden reservierte Speicher kann dann beibehalten und außerhalb des Kontexts der Struktur **SRowSet** wiederverwendet. 
  
Weitere Informationen dazu, wie der Speicher für **SRowSet** Strukturen zugewiesen werden sollen finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

