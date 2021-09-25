---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5da768e4d26ad76e17a1c7271405739b52a2c028
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592522"
---
# <a name="currency"></a>CURRENCY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine signierte 64-Bit-Ganzzahl, die einen Währungswert darstellt. 
  
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
  
> 32 Bit des Währungswerts in niedriger Reihenfolge. 
    
 **Hallo**
  
> 32 Bits des Währungswerts in hoher Reihenfolge.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **CURRENCY-Struktur** ist eine skalierte ganzzahlige Darstellung einer Dezimalzahl mit vier Ziffern rechts vom Dezimalkomma. Beispielsweise ist ein gespeicherter Wert von 327500 so auszulegen, dass er einen Währungswert von 32,7500 darstellt. 
  
Die **CURRENCY-Struktur** wird verwendet, um eine Eigenschaft vom Typ PT_CURRENCY zu beschreiben. Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

