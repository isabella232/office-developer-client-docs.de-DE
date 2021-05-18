---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411792"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft alle Tabellenzeilen, die in einer Reihe von Tabellenzeilen enthalten sind.
  
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
  
> Eine Zeile des angegebenen Zeilensatzs ist ungültig, oder der Zeilensatz selbst ist ungültig. 
    
FALSE 
  
> Die Zeilen des angegebenen Zeilensatzs und der Zeilensatz selbst sind alle gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRow](fbadrow.md)

