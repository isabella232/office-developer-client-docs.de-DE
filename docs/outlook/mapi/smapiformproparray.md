---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579312"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIFormProp](smapiformprop.md) -Strukturen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandte Makro:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>Elemente

 **cProps**
  
> Anzahl der benannten Eigenschaften im Array in der **aFormProp** Member. 
    
 **ulPad**
  
>  Acht Bytes an Füllzeichen verwendet, um die richtige Ausrichtung zu gewährleisten. 
    
 **aFormProp**
  
> Array von Formulareigenschaften.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **SMAPIFormPropArray** wird als Parameter an die folgenden Methoden übergeben: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Siehe auch



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI-Strukturen](mapi-structures.md)

