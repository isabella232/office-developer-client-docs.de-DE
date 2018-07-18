---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791683"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Betrifft**: Outlook 
  
Überprüft eine Zeile in einer Tabelle an.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Parameter

 _lprow_
  
> [in] Zeiger auf eine [SRow](srow.md) -Struktur, die die Zeile zu überprüfenden identifiziert. 
    
## <a name="return-value"></a>R�ckgabewert

TRUE 
  
> Die angegebene Zeile ist ungültig.
    
FALSE 
  
> Die angegebene Zeile ist ungültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRowSet](fbadrowset.md)

