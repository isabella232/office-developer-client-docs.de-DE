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
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795552"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Betrifft**: Outlook 
  
Erstellt eine benannte [SRowSet](srowset.md) -Struktur, die eine angegebene Anzahl von Zeilen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**' Srowset '** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parameter

__crow_
  
> Anzahl der Anzahl von Zeilen, die in die neue Struktur eingeschlossen werden.
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Um die neue Struktur verwenden, die als Zeiger auf eine **SRowSet** -Struktur aus dem Makro **SizedSRowSet** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Siehe auch

- [' Srowset '](srowset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

