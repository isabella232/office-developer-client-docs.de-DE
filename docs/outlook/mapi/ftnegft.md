---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c812cb081c1e4d86c0b3160066b6d953022560f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614171"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Berechnet die beiden Komplemente einer unsignierten 64-Bit-Ganzzahl. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parameter

 _Ft_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die nicht signierte 64-Bit-Ganzzahl enthält, für die die beiden Komplemente berechnet werden sollen. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtNegFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die die beiden Ergänzungen der ganzen Zahl enthält. Der Eingabeparameter bleibt unverändert. 
  

