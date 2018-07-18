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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795305"
---
# <a name="proptag"></a>PROP_TAG

**Betrifft**: Outlook 
  
Gibt eine Eigenschaftentag erstellt durch die Kombination einer angegebenen Eigenschaftentyp und Bezeichner zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parameter

_ulPropType_
  
> Der Eigenschaftentyp für die neue Eigenschaftentag.
    
_ulPropID_
  
> Der Bezeichner für die neue Eigenschaftentag.
    
## <a name="remarks"></a>Bemerkungen

Die **Eigenschaft\_TAG** Makro erstellt eine Eigenschaftentag für eine Eigenschaft vom Typ _UlPropType_ und die Kennung, die in _UlPropID_angegeben ist. Beispielsweise kann eine Eigenschaftentag für eine Eintrags-ID mit dem Makro **PROP_TAG** wie folgt erstellt werden: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Die niederwertige 16 Bit des Tags zurückgegebene Eigenschaft enthalten den Eigenschaftentyp PT_BINARY, und die obere 16 Bit der Eigenschaftenbezeichner 0xFFFF.
  
Weitere Informationen zu Eigenschaftentags finden Sie unter [MAPI-Eigenschaftentags](mapi-property-tags.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

