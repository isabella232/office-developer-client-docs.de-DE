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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583939"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SRowSet](srowset.md) -Struktur, die eine angegebene Anzahl von Zeilen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parameter

__crow_
  
> Anzahl der Anzahl von Zeilen, die in die neue Struktur eingeschlossen werden.
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Um die neue Struktur verwenden, die als Zeiger auf eine **SRowSet** -Struktur aus dem Makro **SizedSRowSet** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Siehe auch

- [SRowSet](srowset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

