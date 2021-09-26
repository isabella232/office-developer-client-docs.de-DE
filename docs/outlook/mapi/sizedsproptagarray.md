---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8ea830c9a198c7483459b6c96087f7c8529f9bf5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591108"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropTagArray-Struktur,](sproptagarray.md) die eine angegebene Anzahl von Eigenschaftstags enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parameter

_ _ctag_
  
> Anzahl der Eigenschaftstags, die in die neue Struktur eingeschlossen werden sollen.
    
_ _Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Makro **"SizedSPropTagArray",** um ein Eigenschaftentagarray mit expliziten Begrenzungen zu erstellen. 
  
Führen Sie die folgende Umwandlung aus, um die neue Struktur zu verwenden, die aus dem Makro **SizeSPropTagArray** als Zeiger auf eine **SPropTagArray-Struktur** resultiert: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Siehe auch

- [SPropTagArray](sproptagarray.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

