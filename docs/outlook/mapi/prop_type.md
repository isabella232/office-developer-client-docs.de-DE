---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5c31622e99079dc7c27d28d95aa26ecd5ac5689f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550183"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftstyp eines angegebenen Eigenschaftstags zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschaftstag, das den zurückzugebenden Eigenschaftstyp enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das **PROP_TYPE** Makro kann verwendet werden, um den Typ einer Eigenschaft zu bestimmen. Wenn Sie beispielsweise PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) aufrufen, wird der Wert zurückgegeben PT_BINARY.
  
Jedes Eigenschaftstag enthält den Eigenschaftstyp im Wort in niedriger Reihenfolge (Bits 0 bis 15) und den Eigenschaftsbezeichner im Hochkomma (Bits 16 bis 31). Das **PROP_TYPE** Makro extrahiert den Eigenschaftentyp und legt ihn in bits 0 bis 15 der ganzen Zahl, die zurückgegeben werden soll. Die verbleibenden Bits des Rückgabewerts werden auf Nullen festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

