---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a94b5ccf5f5f94d6384202b8499d3b6338d67f8e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566479"
---
# <a name="srowset"></a>SRowSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SRow-Strukturen.](srow.md) Jede **SRow-Struktur** beschreibt eine Zeile aus einer Tabelle. 
  
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

## <a name="members"></a>Members

 **Krähen**
  
> Anzahl der **SRow-Strukturen** im **aRow-Element.** 
    
 **aRow**
  
> Array von **SRow-Strukturen.** Es gibt eine Struktur für jede Zeile in der Tabelle. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **SRowSet-Struktur** wird verwendet, um mehrere Datenzeilen aus einer Tabelle zu beschreiben. **SRowSet-Strukturen** werden in den Methoden [IAddrBook,](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)und [IMAPITable](imapitableiunknown.md) zusätzlich zu den folgenden Funktionen verwendet: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **SRowSet-Strukturen** werden genauso definiert wie [ADRLIST-Strukturen,](adrlist.md) damit die Zeilen einer Empfängertabelle und die Einträge in einer Adressliste gleich behandelt werden können. Sowohl **SRowSet-Strukturen** als auch **ADRLIST-Strukturen** können an Methoden wie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook::Address](iaddrbook-address.md)übergeben werden. 
  
Außerdem sind die Regeln für die Speicherzuweisung für **SRowSet-Strukturen** identisch mit den Regeln für **ADRLIST-Strukturen.** Zusammenfassend lässt sich zusammenfassen, dass jede [SPropValue-Struktur](spropvalue.md) im Array, auf die vom **lpProps-Element** jeder Zeile im Zeilensatz verwiesen wird, separat mit [MAPIAllocateBuffer](mapiallocatebuffer.md)zugeordnet werden muss. Jede Eigenschaftswertstruktur muss auch mit [MAPIFreeBuffer](mapifreebuffer.md) zugeordnet werden, bevor die Zuordnung ihrer **SRowSet-Struktur** erfolgt, damit Zeiger auf die zugeordneten **SPropValue-Strukturen** nicht verloren gehen. Der zugeordnete Speicher einer Zeile kann dann außerhalb des Kontexts der **SRowSet-Struktur** beibehalten und wiederverwendet werden. 
  
Weitere Informationen dazu, wie der Speicher für **SRowSet-Strukturen** zugewiesen werden soll, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

