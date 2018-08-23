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
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590960"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

