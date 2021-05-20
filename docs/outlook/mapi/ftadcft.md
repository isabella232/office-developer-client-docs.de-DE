---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429705"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einer anderen einen nicht signierten ganzzahligen 64-Bit-Wert hinzu, optional mit einem Carry-Flag.
  
|||
|:-----|:-----|
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parameter

 _ft1_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
 _ft2_
  
> [in] Eine FILETIME-Struktur, die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.
    
 _pwCarry_
  
> [in, out, optional] Bei der Eingabe ein Zeiger auf das eingehende Carry-Flag. Bei der Ausgabe ein Zeiger auf das Carry-Ergebnis für die Addition. Dieser Parameter kann NULL sein, wenn das Carry-Ergebnis nicht erforderlich ist.
    
## <a name="return-value"></a>Rückgabewert

Die **FtAdcFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die die Summe der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. Wenn **pwCarry** nicht NULL ist, enthält es das Carry-Ergebnis für die Summe, entweder 0 oder 1. 
  
## <a name="remarks"></a>Hinweise

Die **FtAdcFt-Funktion** ist mit **FtAddFt** identisch, wenn  _pwCarry_ NULL ist. Wenn _pwCarry_ nicht NULL ist und auf 0 zeigt, gibt **FtAdcFt** denselben **FILETIME-Wert** zurück, den **FtAddFt zurückgibt.** 
  
## <a name="see-also"></a>Siehe auch



[FtAddFt](ftaddft.md)

