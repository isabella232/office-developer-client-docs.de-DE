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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358114"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Attribute für die Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
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
  
> Die Anzahl der Eigenschaftsattribute im **aPropAttr** -Element. 
    
 **aPropAttr**
  
> Ein Array von Eigenschaftsattributen. Gültige Werte für Attribute lauten wie folgt:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Bemerkungen

Die **SPropAttrArray** -Struktur wird von Eigenschaftendaten Objekten verwendet, die die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle implementieren. Sie wird auch von der MAPI-Implementierung von [IMAPIMessageSite verwendet: IUnknown](imapimessagesiteiunknown.md) , die auf strukturiertem Speicher basiert. 
  
## <a name="see-also"></a>Siehe auch



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI-Strukturen](mapi-structures.md)

