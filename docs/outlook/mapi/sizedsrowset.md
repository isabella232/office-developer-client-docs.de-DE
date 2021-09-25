---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19f607e1dcf705ea57abee43c49c989fea3f21e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619743"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [SRowSet-Struktur,](srowset.md) die eine angegebene Anzahl von Zeilen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parameter

_ _verstrichen_
  
> Anzahl der Zeilen, die in die neue Struktur eingeschlossen werden sollen.
    
_ _Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Führen Sie die folgende Umwandlung aus, um die neue Struktur zu verwenden, die aus dem **Makro SizeSRowSet** als Zeiger auf eine **SRowSet-Struktur** resultiert: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Siehe auch

- [SRowSet](srowset.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

