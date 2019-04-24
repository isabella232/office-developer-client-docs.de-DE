---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344478"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Größenbeschränkung, die zum Testen der Größe eines Eigenschaftswerts verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Elemente

 **RelOp**
  
> Relationaler Operator, der im Größenvergleich verwendet wird. Folgende Werte sind möglich: 
    
RELOP_GE 
  
> Der Vergleich erfolgt basierend auf einem größer oder gleich dem ersten Wert.
    
RELOP_GT 
  
> Der Vergleich erfolgt basierend auf einem höheren ersten Wert.
    
RELOP_LE 
  
> Der Vergleich erfolgt basierend auf einem niedrigeren oder gleichen ersten Wert.
    
RELOP_LT 
  
> Der Vergleich erfolgt basierend auf einem niedrigeren ersten Wert.
    
RELOP_NE 
  
> Der Vergleich erfolgt basierend auf ungleich Werten.
    
RELOP_RE 
  
> Der Vergleich basiert auf LIKE (Regular Expression)-Werten.
    
RELOP_EQ 
  
> Der Vergleich erfolgt basierend auf gleichen Werten.
    
 **ulPropTag**
  
> Property-Tag, das die zu testende Eigenschaft identifiziert.
    
 **cb**
  
> Die Anzahl der Bytes im Eigenschaftswert.
    
## <a name="remarks"></a>Bemerkungen

Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

