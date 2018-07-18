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
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791761"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Betrifft**: Outlook 
  
Fügt einer 64-Bit-Ganzzahl ohne Vorzeichen in eine andere, optional mit einem Flag ausführen.
  
|||
|:-----|:-----|
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parameter

 _FT1_
  
> [in] Ein [FILETIME](filetime.md) -Struktur, die enthält die erste 64-Bit-Ganzzahl hinzugefügt werden soll. 
    
 _ft2_
  
> [in] Ein FILETIME-Struktur, die enthält die zweite 64-Bit-Ganzzahl hinzugefügt werden soll.
    
 _pwCarry_
  
> [eingehend, ausgehend, optional] Führen bei der Eingabe ein Zeiger auf die eingehenden Kennzeichnung. Bei der Ausgabe einen Zeiger auf das Ergebnis sind für das Hinzufügen. Dieser Parameter kann NULL sein, wenn das Ergebnis sind nicht erforderlich ist.
    
## <a name="return-value"></a>R�ckgabewert

Die **FtAdcFt** -Funktion gibt eine **FILETIME** -Struktur, die die Summe der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. Wenn **PwCarry** ungleich NULL ist, werden für die Summe das Ergebnis ausführen enthält 0 oder 1. 
  
## <a name="remarks"></a>Bemerkungen

Die **FtAdcFt** -Funktion ist identisch mit **FtAddFt** , wenn _PwCarry_ NULL ist. Wenn _PwCarry_ nicht NULL ist, und zeigt auf 0, **FtAdcFt** gibt den gleichen **FILETIME** -Wert, den **FtAddFt** zurückgibt. 
  
## <a name="see-also"></a>Siehe auch



[FtAddFt](ftaddft.md)

