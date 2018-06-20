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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795579"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **cProps**
  
> Anzahl der benannten Eigenschaften im Array in der **aFormProp** Member. 
    
 **ulPad**
  
>  Acht Bytes an Füllzeichen verwendet, um die richtige Ausrichtung zu gewährleisten. 
    
 **aFormProp**
  
> Array von Formulareigenschaften.
    
## <a name="remarks"></a>Hinweise

Die Struktur **SMAPIFormPropArray** wird als Parameter an die folgenden Methoden übergeben: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Siehe auch



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI-Strukturen](mapi-structures.md)

