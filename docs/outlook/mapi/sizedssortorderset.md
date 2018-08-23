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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572564"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das Makro **SizedSSortOrderSet** , erstellen Sie eine Sortierreihenfolge mit expliziten Grenzen festgelegt. 
  
Um die neue Struktur verwenden, die als Zeiger auf eine **SSortOrderSet** -Struktur aus dem Makro **SizedSSortOrderSet** erzeugt, führen Sie die folgende Umwandlung: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

