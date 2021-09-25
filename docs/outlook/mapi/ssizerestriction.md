---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d96ab1a4bb8e56bd055af05054f5a8f16448a96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566451"
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

## <a name="members"></a>Members

 **relop**
  
> Relationaler Operator, der im Größenvergleich verwendet wird. Mögliche Werte sind: 
    
RELOP_GE 
  
> Der Vergleich erfolgt basierend auf einem größeren oder gleichen ersten Wert.
    
RELOP_GT 
  
> Der Vergleich erfolgt basierend auf einem größeren ersten Wert.
    
RELOP_LE 
  
> Der Vergleich erfolgt basierend auf einem kleineren oder gleichen ersten Wert.
    
RELOP_LT 
  
> Der Vergleich basiert auf einem geringeren ersten Wert.
    
RELOP_NE 
  
> Der Vergleich erfolgt basierend auf Denkwerten.
    
RELOP_RE 
  
> Der Vergleich basiert auf LIKE-Werten (regulärer Ausdruck).
    
RELOP_EQ 
  
> Der Vergleich erfolgt basierend auf gleichen Werten.
    
 **ulPropTag**
  
> Eigenschaftstag, das die zu testende Eigenschaft identifiziert.
    
 **cb**
  
> Anzahl der Bytes im Eigenschaftswert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

