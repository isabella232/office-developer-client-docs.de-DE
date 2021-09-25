---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1e37da677fa38eb83a22db0c170eb6dd45cb8be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561761"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine unsignierte 64-Bit-Ganzzahl zu einer anderen hinzu, optional mithilfe eines Carry-Flags.
  
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
  
> [in, out, optional] Bei der Eingabe ein Zeiger auf das eingehende Carry-Flag. Bei der Ausgabe ein Zeiger auf das Ergebnis "Carry" für den Zusatz. Dieser Parameter kann NULL sein, wenn das Ergebnis nicht erforderlich ist.
    
## <a name="return-value"></a>Rückgabewert

Die **FtAdcFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die die Summe der beiden ganzzahligen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. Wenn **pwCarry** ungleich NULL ist, enthält es das Ergebnis für die Summe, entweder 0 oder 1. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **FtAdcFt-Funktion** ist identisch mit **FtAddFt,** wenn  _pwCarry_ NULL ist. Wenn  _pwCarry_ nicht NULL ist und auf 0 zeigt, gibt **FtAdcFt** denselben **FILETIME-Wert** zurück, den **FtAddFt** zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[FtAddFt](ftaddft.md)

