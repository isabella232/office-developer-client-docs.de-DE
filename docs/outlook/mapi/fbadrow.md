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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420619"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft eine Zeile in einer Tabelle.
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Parameter

 _lprow_
  
> [in] Zeiger auf eine [SRow-Struktur,](srow.md) die die zu überprüfende Zeile identifiziert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Zeile ist ungültig.
    
FALSE 
  
> Die angegebene Zeile ist gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRowSet](fbadrowset.md)

