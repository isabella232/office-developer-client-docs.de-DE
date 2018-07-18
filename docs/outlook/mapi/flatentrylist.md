---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791694"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Betrifft**: Outlook 
  
Enthält ein Array von [FLATENTRY](flatentry.md) -Strukturen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Elemente

**cEntries**
  
> Anzahl der **FLATENTRY** Strukturen in das Array von **AbEntries** -Elements beschrieben. 
    
**cbEntries**
  
> Die Anzahl von Bytes im Array von **AbEntries**beschrieben. 
    
**abEntries**
  
> Byte-Array, das ein oder mehrere **FLATENTRY** Strukturen enthält angeordnete Ende zu Ende. 
    
## <a name="remarks"></a>Bemerkungen

Im Array **AbEntries** wird jede **FLATENTRY** Struktur auf einer vertrauten ausgerichtete Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand, stellen Sie sicher, dass natürlichen Ausrichtung alle zweier **FLATENTRY** Strukturen enthalten. Die erste **FLATENTRY** Struktur im Array ist immer ordnungsgemäß ausgerichtet werden, da der Versatz des Elements **AbEntries** 8 ist. Berechnen Sie den Offset der nächsten Struktur, verwenden Sie die Größe des ersten Eintrags aufgerundet auf das nächste Vielfache von 4. Verwenden Sie das Makro [CbFLATENTRY](cbflatentry.md) , um die Größe einer **FLATENTRY** -Struktur zu berechnen. 
  
Die zweite **FLATENTRY** -Struktur beginnt mit einem Offset, der den Offset des ersten Eintrags plus die Länge des ersten Eintrags gerundet auf die nächsten vier Bytes besteht. Die Länge des ersten Eintrags beträgt die Länge der **Cb** Mitglied plus die Länge des **AbEntry** Mitglied. 
  
Im folgenden Codebeispiel gibt an, wie Offsets in einer **FLATENTRYLIST** -Struktur zu berechnen. Wird davon ausgegangen Sie, dass diese _LpFlatEntry_ einen Zeiger auf die erste Struktur in der Liste ist. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Siehe auch

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries (kanonische Eigenschaft)](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI-Strukturen](mapi-structures.md)

