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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590162"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

