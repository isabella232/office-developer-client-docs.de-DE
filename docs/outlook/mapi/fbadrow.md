---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6edefa72e7410bbea1474c948c016f06c30d5f64
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576303"
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

