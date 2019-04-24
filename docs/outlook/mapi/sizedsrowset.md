---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282642"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SRowSet](srowset.md) -Struktur, die eine angegebene Anzahl von Zeilen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parameter

__Crow_
  
> Die Anzahl der Zeilen, die in die neue Struktur eingeschlossen werden sollen.
    
__Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Um die neue Struktur zu verwenden, die aus dem **SizedSRowSet** -Makro als Zeiger auf eine **SRowSet** -Struktur resultiert, führen Sie die folgenden Schritte aus: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Siehe auch

- [SRowSet](srowset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

