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
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577681"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Liste der Attribute für die Eigenschaften eines Objekts. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
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
  
> Anzahl der Attribute im **aPropAttr** -Member. 
    
 **aPropAttr**
  
> Ein Array von Eigenschaftsattribute. Gültige Werte für Attribute sind wie folgt:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **SPropAttrArray** wird vom Daten Property-Objekten, die implementiert werden die [IPropData: IMAPIProp](ipropdataimapiprop.md) Schnittstelle. Darüber hinaus wird von der MAPI-Implementierung der [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) also basierend auf strukturierter Speicher. 
  
## <a name="see-also"></a>Siehe auch



[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[MAPI-Strukturen](mapi-structures.md)

