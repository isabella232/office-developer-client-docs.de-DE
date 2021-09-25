---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 79ef39504d118ac7577fed789360a08bca043d3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624174"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Attribute für Eigenschaften eines Objekts. 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Eigenschaftsattribute im **aPropAttr-Element.** 
    
 **aPropAttr**
  
> Ein Array von Eigenschaftsattributen. Gültige Werte für Attribute sind:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Bemerkungen

Die **SPropAttrArray-Struktur** wird von Eigenschaftsdatenobjekten verwendet, die die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) implementieren. Es wird auch von der MAPI-Implementierung von [IMAPIMessageSite : IUnknown verwendet,](imapimessagesiteiunknown.md) die auf strukturiertem Speicher basiert. 
  
## <a name="see-also"></a>Siehe auch



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI-Strukturen](mapi-structures.md)

