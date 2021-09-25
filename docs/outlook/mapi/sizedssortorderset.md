---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a441320c2efeac68982e01c7a0a366b47aa46676
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578613"
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
  
> Anzahl der Sortierreihenfolgen, die in die neue Struktur einbezogen werden sollen.
    
_ _Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das **Makro SizeSSortOrderSet,** um einen Sortierreihenfolgesatz mit expliziten Grenzen zu erstellen. 
  
Führen Sie die folgende Umwandlung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizedSSortOrderSet** als Zeiger auf eine **SSortOrderSet-Struktur** resultiert: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Siehe auch

- [SSortOrderSet](ssortorderset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

