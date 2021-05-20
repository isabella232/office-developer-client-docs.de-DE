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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428606"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SSortOrderSet-Struktur,](ssortorderset.md) die eine angegebene Anzahl von Sortierreihenfolgen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parameter

_ _csort_
  
> Anzahl der Sortierreihenfolgen, die in die neue Struktur eingeschlossen werden sollen.
    
_ _name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Verwenden Sie **das Makro SizedSSortOrderSet,** um einen Sortierreihenfolgensatz mit expliziten Grenzen zu erstellen. 
  
Führen Sie die folgende Gliederung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSSortOrderSet** als Zeiger auf eine **SSortOrderSet-Struktur** resultiert: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

