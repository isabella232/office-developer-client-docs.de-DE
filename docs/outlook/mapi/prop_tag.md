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
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570989"
---
# <a name="proptag"></a>PROP_TAG

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **Eigenschaft\_TAG** Makro erstellt eine Eigenschaftentag für eine Eigenschaft vom Typ _UlPropType_ und die Kennung, die in _UlPropID_angegeben ist. Beispielsweise kann eine Eigenschaftentag für eine Eintrags-ID mit dem Makro **PROP_TAG** wie folgt erstellt werden: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Die niederwertige 16 Bit des Tags zurückgegebene Eigenschaft enthalten den Eigenschaftentyp PT_BINARY, und die obere 16 Bit der Eigenschaftenbezeichner 0xFFFF.
  
Weitere Informationen zu Eigenschaftentags finden Sie unter [MAPI-Eigenschaftentags](mapi-property-tags.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

