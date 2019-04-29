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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413857"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [FLATENTRY](flatentry.md) -Strukturen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verwandte Makros:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**Zentriert**
  
> Die Anzahl der **FLATENTRY** -Strukturen in dem vom **abEntries** -Element beschriebenen Array. 
    
**cbEntries**
  
> Die Anzahl der Bytes im von **abEntries**beschriebenen Array. 
    
**abEntries**
  
> Bytearray, das eine oder mehrere **FLATENTRY** -Strukturen enthält, die bis zum Ende angeordnet sind. 
    
## <a name="remarks"></a>Bemerkungen

Im **abEntries** -Array wird jede **FLATENTRY** -Struktur an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Padding enthalten, um eine natürliche Ausrichtung zwischen zwei **FLATENTRY** -Strukturen sicherzustellen. Die erste **FLATENTRY** -Struktur im Array wird immer korrekt ausgerichtet, da der Offset des **abEntries** -Elements 8 ist. Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, aufgerundet auf das nächste Vielfache von 4. Verwenden Sie das [CbFLATENTRY](cbflatentry.md) -Makro, um die Größe einer **FLATENTRY** -Struktur zu berechnen. 
  
Beispielsweise beginnt die zweite **FLATENTRY** -Struktur mit einem Offset, der aus dem Offset des ersten Eintrags und der Länge des ersten Eintrags besteht, gerundet auf die nächsten vier Bytes. Die Länge des ersten Eintrags entspricht der Länge des **CB** -Elements sowie der Länge des **abEntry** -Elements. 
  
Das folgende Codebeispiel gibt an, wie Offsets in einer **FLATENTRYLIST** -Struktur berechnet werden. Gehen Sie davon aus, dass _lpFlatEntry_ ein Zeiger auf die erste Struktur in der Liste ist. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Siehe auch

- [FLATENTRY](flatentry.md)
- [Kanonische Pidtagreplyrecipiententries (-Eigenschaft](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI-Strukturen](mapi-structures.md)

