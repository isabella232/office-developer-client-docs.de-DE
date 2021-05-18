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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412835"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftentyp eines angegebenen Eigenschaftstags zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschaftstag, das den zurückgegebenen Eigenschaftentyp enthält.
    
## <a name="remarks"></a>Hinweise

Das **PROP_TYPE** kann verwendet werden, um den Typ einer Eigenschaft zu bestimmen. Wenn Sie z. B. PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) aufrufen, wird der Wert PT_BINARY zurückgegeben.
  
Jedes Eigenschaftstag enthält den Eigenschaftentyp im Wort mit niedriger Reihenfolge (Bits 0 bis 15) und den Eigenschaftenbezeichner im Wort mit hoher Ordnung (Bits 16 bis 31). Das **PROP_TYPE** extrahiert den Eigenschaftentyp und legt ihn in bits 0 bis 15 der ganzen Zahl, die zurückgegeben werden soll. Die verbleibenden Bits des Rückgabewerts werden auf Nullen festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

