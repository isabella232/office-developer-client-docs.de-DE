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
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791690"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Betrifft**: Outlook 
  
Überprüft alle Tabellenzeilen in einer Tabellenzeilen enthalten.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Parameter

 _lpRowSet_
  
> [in] Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den zu überprüfenden Rowset identifiziert. Wenn der Zeiger NULL ist, ist die Struktur ungültig. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Eine Zeile mit der angegebenen Zeile Set ist ungültig, oder die Rowset selbst ist ungültig. 
    
FALSE 
  
> Die Zeilen der angegebenen Zeile Menge und die Zeile selbst festgelegt sind gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRow](fbadrow.md)

