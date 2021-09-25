---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af523723a4a835ed4585cc9001522d087c5f2cab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578739"
---
# <a name="sbinary"></a>SBinary

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Eigenschaft vom Typ PT_BINARY.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> Anzahl der Bytes im **lpb-Element.** 
    
 **lpb**
  
> Zeiger auf den wert der PT_BINARY-Eigenschaft.
    
## <a name="remarks"></a>HinwBemerkungeneise

Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

