---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795553"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Betrifft**: Outlook 
  
Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Eigenschaftentags enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parameter

__ctag_
  
> Anzahl der Eigenschaftentags in die neue Struktur enthalten sein.
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das Makro **SizedSPropTagArray** , um ein Array Tag-Eigenschaft mit expliziten Grenzen zu erstellen. 
  
Um die neue Struktur verwenden, die als Zeiger auf eine **SPropTagArray** -Struktur aus dem Makro **SizedSPropTagArray** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Siehe auch

- [SPropTagArray](sproptagarray.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

