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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340957"
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
  
> in Zeiger auf eine [SRow](srow.md) -Struktur, die die zu überprüfende Zeile identifiziert. 
    
## <a name="return-value"></a>Rückgabewert

TRUE 
  
> Die angegebene Zeile ist ungültig.
    
FALSE 
  
> Die angegebene Zeile ist gültig.
    
## <a name="see-also"></a>Siehe auch



[FBadRowSet](fbadrowset.md)

