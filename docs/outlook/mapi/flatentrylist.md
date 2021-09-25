---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1d8e86b62c2ea7fc2ee004192f05643e1c26042
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561810"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [FLATENTRY-Strukturen.](flatentry.md) 
  
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

## <a name="members"></a>Members

**cEntries**
  
> Anzahl der **FLATENTRY-Strukturen** im Array, das vom **abEntries-Element** beschrieben wird. 
    
**cbEntries**
  
> Anzahl der Bytes in dem durch **abEntries** beschriebenen Array. 
    
**abEntries**
  
> Bytearray, das eine oder mehrere **FLATENTRY-Strukturen** enthält, die End-to-End angeordnet sind. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Im **array abEntries** wird jede **FLATENTRY-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **FLATENTRY-Strukturen** sicherzustellen. Die erste **FLATENTRY-Struktur** im Array wird immer korrekt ausgerichtet, da der Offset des **Elements "abEntries"** 8 ist. Um den Offset der nächsten Struktur zu berechnen, verwenden Sie die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wird. Verwenden Sie das [CbFLATENTRY-Makro,](cbflatentry.md) um die Größe einer **FLATENTRY-Struktur** zu berechnen. 
  
Beispielsweise beginnt die zweite **FLATENTRY-Struktur** mit einem Offset, der aus dem Offset des ersten Eintrags plus der Länge des ersten Eintrags besteht, der auf die nächsten vier Bytes gerundet wird. Die Länge des ersten Eintrags ist die Länge des **cb-Elements** plus der Länge des **abEntry-Elements.** 
  
Das folgende Codebeispiel gibt an, wie Offsets in einer **FLATENTRYLIST-Struktur** berechnet werden. Angenommen,  _lpFlatEntry_ ist ein Zeiger auf die erste Struktur in der Liste. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Siehe auch

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries (kanonische Eigenschaft)](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI-Strukturen](mapi-structures.md)

