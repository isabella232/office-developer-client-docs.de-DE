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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439086"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Größeneinschränkung, die zum Testen der Größe eines Eigenschaftswerts verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Elemente

 **relop**
  
> Relationaler Operator, der im Größenvergleich verwendet wird. Mögliche Werte sind: 
    
RELOP_GE 
  
> Der Vergleich basiert auf einem höheren oder gleichen ersten Wert.
    
RELOP_GT 
  
> Der Vergleich basiert auf einem größeren ersten Wert.
    
RELOP_LE 
  
> Der Vergleich basiert auf einem kleineren oder gleichen ersten Wert.
    
RELOP_LT 
  
> Der Vergleich basiert auf einem niedrigeren ersten Wert.
    
RELOP_NE 
  
> Der Vergleich basiert auf ungleichen Werten.
    
RELOP_RE 
  
> Der Vergleich erfolgt basierend auf LIKE -Werten (regulärer Ausdruck).
    
RELOP_EQ 
  
> Der Vergleich basiert auf gleichen Werten.
    
 **ulPropTag**
  
> Eigenschaftstag, das die zu testende Eigenschaft identifiziert.
    
 **cb**
  
> Anzahl der Bytes im Eigenschaftswert.
    
## <a name="remarks"></a>Hinweise

Eine allgemeine Diskussion über die Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

