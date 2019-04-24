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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341020"
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
  
> in Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den zu überprüfenden Zeilensatz identifiziert. Wenn der Zeiger NULL ist, ist die Struktur ungültig. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Eine Zeile des angegebenen Zeilen Satzes ist ungültig, oder der Zeilensatz selbst ist ungültig. 
    
FALSE 
  
> Die Zeilen des angegebenen Zeilen Satzes und des Zeilen Satzes selbst sind gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRow](fbadrow.md)

