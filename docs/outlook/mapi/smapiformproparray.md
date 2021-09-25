---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 471e2accdd925e81c951e195349bf00691dea100
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624181"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIFormProp-Strukturen.](smapiformprop.md) 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verwandtes Makro:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
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
  
> Anzahl der benannten Eigenschaften im Array im **aFormProp-Element.** 
    
 **ulPad**
  
>  Acht Bytes Abstand, die verwendet werden, um eine korrekte Ausrichtung zu gewährleisten. 
    
 **aFormProp**
  
> Array von Formulareigenschaften.
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIFormPropArray-Struktur** wird als Parameter an die folgenden Methoden übergeben: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Siehe auch



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI-Strukturen](mapi-structures.md)

