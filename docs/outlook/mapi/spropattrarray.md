---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405513"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste von Attributen für Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Eigenschaftenattribute im **aPropAttr-Element.** 
    
 **aPropAttr**
  
> Ein Array von Eigenschaftenattributen. Gültige Werte für Attribute sind wie folgt:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Hinweise

Die **SPropAttrArray-Struktur** wird von Eigenschaftsdatenobjekten verwendet, die die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) implementieren. Sie wird auch von der MAPI-Implementierung von [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) verwendet, die auf strukturiertem Speicher basiert. 
  
## <a name="see-also"></a>Siehe auch



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI-Strukturen](mapi-structures.md)

