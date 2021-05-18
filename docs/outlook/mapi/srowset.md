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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407256"
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

## <a name="members"></a>Elemente

 **cRows**
  
> Anzahl der **SRow-Strukturen** im **aRow-Element.** 
    
 **aRow**
  
> Array von **SRow-Strukturen.** Es gibt eine Struktur für jede Zeile in der Tabelle. 
    
## <a name="remarks"></a>Hinweise

Eine **SRowSet-Struktur** wird verwendet, um mehrere Datenzeilen aus einer Tabelle zu beschreiben. **SRowSet-Strukturen** werden zusätzlich zu den folgenden Funktionen in den [Schnittstellenmethoden IAddrBook,](iaddrbookimapiprop.md) [ITableData](itabledataiunknown.md)und [IMAPITable](imapitableiunknown.md) verwendet: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **SRowSet-Strukturen** sind identisch mit [ADRLIST-Strukturen](adrlist.md) definiert, damit die Zeilen einer Empfängertabelle und die Einträge in einer Adressliste gleich behandelt werden können. **Sowohl SRowSet-Strukturen** als auch **ADRLIST-Strukturen** können an Methoden wie [IMessage::ModifyRecipients](imessage-modifyrecipients.md) und [IAddrBook::Address übergeben werden.](iaddrbook-address.md) 
  
Außerdem sind die Regeln für die Speicherzuweisung für **SRowSet-Strukturen** mit den Regeln für **ADRLIST-Strukturen** identisch. Zusammenfassend muss jede [SPropValue-Struktur](spropvalue.md) im Array, auf die das **lpProps-Mitglied** jeder Zeile im Zeilensatz verweist, mithilfe von [MAPIAllocateBuffer](mapiallocatebuffer.md)separat zugeordnet werden. Jede Eigenschaftswertstruktur muss auch mit [MAPIFreeBuffer](mapifreebuffer.md) vor der Deallocation der **SRowSet-Struktur** zugeordnet werden, damit Zeiger auf die zugewiesenen **SPropValue-Strukturen** nicht verloren gehen. Der zugewiesene Speicher einer Zeile kann dann außerhalb des Kontexts der **SRowSet-Struktur beibehalten und wiederverwendet** werden. 
  
Weitere Informationen dazu, wie der Arbeitsspeicher für **SRowSet-Strukturen** zugewiesen werden soll, finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

