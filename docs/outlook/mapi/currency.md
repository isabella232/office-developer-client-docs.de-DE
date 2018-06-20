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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791499"
---
# <a name="currency"></a>CURRENCY

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **Lo**
  
> Niederwertige 32 Bit der Währungswert. 
    
 **Hallo**
  
> Obere 32 Bit der Währungswert.
    
## <a name="remarks"></a>Hinweise

Die **Währung** -Struktur ist eine skalierte Ganzzahl Darstellung einer ganzen Zahl mit vier Stellen rechts vom Dezimalkomma. Beispielsweise ist der gespeicherter Wert 327500, ausgelegt werden als einen Währungswert des 32.7500 darstellt. 
  
Die **Währung** Struktur wird verwendet, um eine Eigenschaft vom Typ PT_CURRENCY beschrieben. Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

