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
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595419"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Beschränkung der Größe der verwendet wird, um die Größe der Wert einer Eigenschaft zu testen. 
  
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

 **RelOp-Element**
  
> Relationale Operator, der in der Größenvergleich verwendet wird. Mögliche Werte sind wie folgt: 
    
RELOP_GE 
  
> Der Vergleich wird basierend auf der ersten Wert größer oder gleich vorgenommen.
    
RELOP_GT 
  
> Der Vergleich wird basierend auf einen höheren Wert für die erste vorgenommen.
    
RELOP_LE 
  
> Der Vergleich wird basierend auf dem ersten Wert kleiner oder gleich vorgenommen.
    
RELOP_LT 
  
> Der Vergleich wird basierend auf einen kleineren Wert des ersten vorgenommen.
    
RELOP_NE 
  
> Der Vergleich wird basierend auf Werten mit ungleicher vorgenommen.
    
RELOP_RE 
  
> Der Vergleich basierend auf wie Werte (reguläre Ausdrücke) erfolgt.
    
RELOP_EQ 
  
> Der Vergleich wird basierend auf gleich große Werte vorgenommen.
    
 **ulPropTag**
  
> Eigenschafts-Tag, die zu überprüfenden Eigenschaft identifiziert.
    
 **cb**
  
> Anzahl der Bytes in der Eigenschaftswert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

