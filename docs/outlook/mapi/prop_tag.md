---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425883"
---
# <a name="prop_tag"></a>PROP_TAG

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Eigenschaftentag zurück, das durch Kombinieren eines angegebenen Eigenschaftentyps und bezeichners erstellt wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parameter

_ulPropType_
  
> Eigenschaftstyp für das neue Eigenschaftstag.
    
_ulPropID_
  
> Eigenschafts-ID für das neue Eigenschaftstag.
    
## <a name="remarks"></a>Hinweise

Das **PROP \_ TAG-Makro** erstellt ein Eigenschaftentag für eine Eigenschaft vom Typ _ulPropType_ und den bezeichner, der in _ulPropID angegeben ist._ Beispielsweise kann ein Eigenschaftentag für einen Eintragsbezeichner mithilfe des PROP_TAG wie folgt erstellt werden:  
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Die 16 Bit niedriger Reihenfolge des zurückgegebenen Eigenschaftstags enthalten den Eigenschaftentyp PT_BINARY, und die 16 Bit in hoher Reihenfolge enthalten den Eigenschaftenbezeichner 0xFFFF.
  
Weitere Informationen zu Eigenschaftstags finden Sie unter [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

