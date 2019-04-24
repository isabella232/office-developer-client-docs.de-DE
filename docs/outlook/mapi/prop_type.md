---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332760"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftentyp eines angegebenen Property-Tags zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Property-Tag, das den zurückzugebenden Eigenschaftentyp enthält.
    
## <a name="remarks"></a>Bemerkungen

Das **PROP_TYPE** -Makro kann verwendet werden, um den Typ einer Eigenschaft zu bestimmen. Beispielsweise führt das Aufrufen von PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) dazu, dass der Wert PT_BINARY zurückgegeben wird.
  
Jedes Property-Tag enthält den Eigenschaftentyp im niedrigwertigen Wort (Bits 0 bis 15) und den Eigenschaftenbezeichner im hochwertigen Wort (Bits 16 bis 31). Das **PROP_TYPE** -Makro extrahiert den Eigenschaftentyp und fügt ihn in die Bits 0 bis 15 der zurückzugebenden Ganzzahl ein. Die restlichen Bits des Rückgabewerts werden auf Nullen festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

