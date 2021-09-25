---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 691df04d46b8f211f6befd367cc63a388298090e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586705"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SPropProblemArray-Struktur,](spropproblemarray.md) die eine angegebene Anzahl von [SPropProblem-Strukturen](spropproblem.md) enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameter

_ _cprob_
  
> Anzahl der **SPropProblem-Strukturen,** die in die neue Struktur eingeschlossen werden sollen. 
    
_ _Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Makro **"SizedSPropProblemArray",** um ein Eigenschaftsproblemarray mit expliziten Grenzen zu erstellen. Führen Sie die folgende Umwandlung aus, um die neue Struktur zu verwenden, die aus dem Makro **"SizedSPropProblemArray"** als Zeiger auf eine **SPropProblemArray-Struktur** resultiert: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Siehe auch

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

