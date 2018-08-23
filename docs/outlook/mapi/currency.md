---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576463"
---
# <a name="currency"></a>CURRENCY

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine 64-Bit-Ganzzahl, die einen Währungswert darstellt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Elemente

 **Lo**
  
> Niederwertige 32 Bit der Währungswert. 
    
 **Hallo**
  
> Obere 32 Bit der Währungswert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **Währung** -Struktur ist eine skalierte Ganzzahl Darstellung einer ganzen Zahl mit vier Stellen rechts vom Dezimalkomma. Beispielsweise ist der gespeicherter Wert 327500, ausgelegt werden als einen Währungswert des 32.7500 darstellt. 
  
Die **Währung** Struktur wird verwendet, um eine Eigenschaft vom Typ PT_CURRENCY beschrieben. Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

