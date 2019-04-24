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
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282698"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropTagArray](sproptagarray.md) -Struktur, die eine angegebene Anzahl von Property-Tags enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parameter

__CTAG_
  
> Die Anzahl der Eigenschaftstags, die in die neue Struktur eingeschlossen werden sollen.
    
__Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **SizedSPropTagArray** -Makro, um ein Property-Tag-Array mit expliziten Begrenzungen zu erstellen. 
  
Um die neue Struktur zu verwenden, die aus dem **SizedSPropTagArray** -Makro als Zeiger auf eine **SPropTagArray** -Struktur resultiert, führen Sie die folgenden Schritte aus: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Siehe auch

- [SPropTagArray](sproptagarray.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

