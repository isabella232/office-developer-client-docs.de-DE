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

## <a name="members"></a>Elemente

**cEntries**
  
> Anzahl der **FLATENTRY-Strukturen** im Array, das vom **abEntries-Element beschrieben** wird. 
    
**cbEntries**
  
> Anzahl der Byte im array, das von **abEntries beschrieben wird.** 
    
**abEntries**
  
> Bytearray, das eine oder mehrere **FLATENTRY-Strukturen** enthält, zwischen Ende und Ende angeordnet. 
    
## <a name="remarks"></a>Hinweise

Im **abEntries-Array** wird jede **FLATENTRY-Struktur** an einer natürlich ausgerichteten Grenze ausgerichtet. Zusätzliche Bytes sind als Abstand enthalten, um die natürliche Ausrichtung zwischen zwei **FLATENTRY-Strukturen sicherzustellen.** Die erste **FLATENTRY-Struktur** im Array wird immer richtig ausgerichtet, da der Offset des **abEntries-Mitglieds** 8 ist. Verwenden Sie zum Berechnen des Offsets der nächsten Struktur die Größe des ersten Eintrags, der auf das nächste Vielfache von 4 aufgerundet wurde. Verwenden Sie das [CbFLATENTRY-Makro,](cbflatentry.md) um die Größe einer **FLATENTRY-Struktur zu** berechnen. 
  
Die zweite **FLATENTRY-Struktur** beginnt beispielsweise bei einem Offset, der aus dem Offset des ersten Eintrags plus der Länge des ersten Eintrags besteht, der auf die nächsten vier Bytes gerundet wird. Die Länge des ersten Eintrags ist die Länge des **cb-Mitglieds** plus die Länge des **abEntry-Mitglieds.** 
  
Das folgende Codebeispiel zeigt, wie Offsets in einer **FLATENTRYLIST-Struktur berechnet** werden. Angenommen,  _lpFlatEntry_ ist ein Zeiger auf die erste Struktur in der Liste. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Siehe auch

- [FLATENTRY](flatentry.md)
- [PidTagReplyRecipientEntries (kanonische Eigenschaft)](pidtagreplyrecipiententries-canonical-property.md)
- [MAPI-Strukturen](mapi-structures.md)

