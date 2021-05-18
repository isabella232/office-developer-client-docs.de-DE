---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409132"
---
# <a name="prop_id"></a>PROP_ID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eigenschaftenbezeichner eines angegebenen Eigenschaftstags zurück.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> Eigenschaftstag, das den zurück zu verwendende Bezeichner enthält.
    
## <a name="remarks"></a>Hinweise

Jedes Eigenschaftstag enthält den Eigenschaftentyp im Wort mit niedriger Reihenfolge (Bits 0 bis 15) und den Eigenschaftenbezeichner im Wort mit hoher Ordnung (Bits 16 bis 31). Das **PROP_ID** extrahiert den Eigenschaftsbezeichner und legt ihn in die Bits 0 bis 15 der zurück zu verwendenden ganzen Zahl. Die verbleibenden Bits des Rückgabewerts werden auf Nullen festgelegt. 
  
Das **PROP_ID** kann z. B. verwendet werden, um einen Bezeichner abzurufen, der [an IMAPIProp::GetNamesFromIDs übergeben werden soll.](imapiprop-getnamesfromids.md) **GetNamesFromIDs** ruft den Eigenschaftennamen ab, der einem Bezeichner für eine benannte Eigenschaft zugeordnet ist. 
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

