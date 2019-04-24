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
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309513"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [SMAPIFormProp](smapiformprop.md) -Strukturen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Zugehöriges Makro:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
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
  
> Die Anzahl benannter Eigenschaften im Array im **aFormProp** -Element. 
    
 **ulPad**
  
>  Acht Byte Leerraum, die verwendet werden, um eine korrekte Ausrichtung zu gewährleisten. 
    
 **aFormProp**
  
> Array von Formulareigenschaften.
    
## <a name="remarks"></a>Bemerkungen

Die **SMAPIFormPropArray** -Struktur wird als Parameter an die folgenden Methoden übergeben: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Siehe auch



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[MAPI-Strukturen](mapi-structures.md)

