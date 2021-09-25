---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e1d1f759989ae7c241317b7488ce0d8f53180e9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609635"
---
# <a name="prop_tag"></a>PROP_TAG

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Eigenschaftstag zurück, das durch Kombinieren eines angegebenen Eigenschaftstyps und bezeichners erstellt wurde. 
  
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
  
> Eigenschaftsbezeichner für das neue Eigenschaftstag.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das **PROP \_ TAG-Makro** erstellt ein Eigenschaftentag für eine Eigenschaft vom Typ  _ulPropType_ und den Bezeichner, der in  _ulPropID_ angegeben ist. Beispielsweise kann ein Eigenschaftstag für einen Eintragsbezeichner mithilfe des **Makros PROP_TAG** wie folgt erstellt werden: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Die 16 Bits in niedriger Reihenfolge des zurückgegebenen Eigenschaftstags enthalten den Eigenschaftentyp, PT_BINARY und die 16 Bit in hoher Reihenfolge enthalten den Eigenschaftsbezeichner 0xFFFF.
  
Weitere Informationen zu Eigenschaftstags finden Sie unter [MAPI Property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

