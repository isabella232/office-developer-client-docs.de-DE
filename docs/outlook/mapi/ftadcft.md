---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328021"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine unsignierte 64-Bit-Ganzzahl zu einem anderen hinzu, optional mit einem Carry-Flag.
  
|||
|:-----|:-----|
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parameter

 _FT1_
  
> in Eine [FILETIME](filetime.md) -Struktur, die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
 _ft2_
  
> in Eine fileTIME-Struktur, die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll.
    
 _pwCarry_
  
> [in, out, optional] Bei Eingabe ein Zeiger auf die eingehende Carry-Kennzeichnung. Bei Ausgabe ein Zeiger auf das Carry-Ergebnis für den Zusatz. Dieser Parameter kann NULL sein, wenn das Carry-Ergebnis nicht erforderlich ist.
    
## <a name="return-value"></a>Rückgabewert

Die **FtAdcFt** -Funktion gibt **** eine FILETIME-Struktur zurück, die die Summe der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. Wenn **pwCarry** ungleich NULL ist, enthält es das Carry-Ergebnis für die Summe, entweder 0 oder 1. 
  
## <a name="remarks"></a>Bemerkungen

Die **FtAdcFt** -Funktion ist identisch mit **FtAddFt** , wenn _pwCarry_ NULL ist. Wenn _pwCarry_ nicht NULL ist und auf 0 zeigt, gibt **FtAdcFt** den gleichen **FILETIME** -Wert zurück, der **FtAddFt** zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[FtAddFt](ftaddft.md)

