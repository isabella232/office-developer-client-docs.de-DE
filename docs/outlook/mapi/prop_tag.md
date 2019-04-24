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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328567"
---
# <a name="proptag"></a>PROP_TAG

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Eigenschaftentag zurück, das durch Kombinieren eines angegebenen Eigenschaftentyps und Bezeichners erstellt wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parameter

_ulPropType_
  
> Eigenschafts für das neue Property-Tag.
    
_ulPropID_
  
> Eigenschaftenbezeichner für das neue Property-Tag.
    
## <a name="remarks"></a>Bemerkungen

Das **Prop\_-Tag** -Makro erstellt ein Property-Tag für eine Eigenschaft vom Typ _ulPropType_ und den in _ulPropID_angegebenen Bezeichner. Beispielsweise kann ein Property-Tag für eine Eintrags-ID wie folgt mithilfe des **PROP_TAG** -Makros erstellt werden: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Die niedrigwertigen 16 Bits des zurückgegebenen Property-Tags enthalten den Eigenschaftentyp PT_BINARY, und die hochwertigen 16 Bits enthalten den Eigenschaftenbezeichner 0xFFFF.
  
Weitere Informationen zu Eigenschaftstags finden Sie unter [MAPI property Tags](mapi-property-tags.md).
  
## <a name="see-also"></a>Siehe auch

- [SPropValue](spropvalue.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

