---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 241441c1aa516b366fdecd6c17f5d12cf12a2206
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630929"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft alle Tabellenzeilen, die in einem Satz von Tabellenzeilen enthalten sind.
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Parameter

 _lpRowSet_
  
> [in] Zeiger auf eine [SRowSet-Struktur,](srowset.md) die den zu überprüfenden Zeilensatz identifiziert. Wenn der Zeiger NULL ist, ist die Struktur ungültig. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Eine Zeile des angegebenen Zeilensatzes ist ungültig, oder der Zeilensatz selbst ist ungültig. 
    
FALSE 
  
> Die Zeilen des angegebenen Zeilensatzes und der Zeilensatz selbst sind alle gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRow](fbadrow.md)

