---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357519"
---
# <a name="sbinary"></a>SBinary

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Eigenschaft vom Typ PT_BINARY.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Elemente

 **cb**
  
> Die Anzahl der Bytes im **LPB** -Element. 
    
 **LPB**
  
> Zeiger auf den Wert der PT_BINARY-Eigenschaft.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

