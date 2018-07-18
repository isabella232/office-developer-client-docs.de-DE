---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795568"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Betrifft**: Outlook 
  
Erstellt eine benannte [SSortOrderSet](ssortorderset.md) -Struktur, die eine angegebene Anzahl von Sortierreihenfolgen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parameter

__csort_
  
> Anzahl der Sortierreihenfolgen, die in die neue Struktur eingeschlossen werden.
    
__Namen_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Verwenden Sie das Makro **SizedSSortOrderSet** , erstellen Sie eine Sortierreihenfolge mit expliziten Grenzen festgelegt. 
  
Um die neue Struktur verwenden, die als Zeiger auf eine **SSortOrderSet** -Struktur aus dem Makro **SizedSSortOrderSet** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

