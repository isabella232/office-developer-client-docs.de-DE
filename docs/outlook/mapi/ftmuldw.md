---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 430eff9b19f4052a77d3792ceb4f9b3412ee79ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630852"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Multipliziert eine 64-Bit-Ganzzahl ohne Vorzeichen mit einer nicht signierten 32-Bit-Ganzzahl.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parameter

 _Multiplikator_
  
> [in] Ein Doppelwort, das den 32-Bit-Ganzzahl-Multiplizierer ohne Vorzeichen enthält. 
    
 _Multiplicand_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die nicht signierte 64-Bit-Ganzzahl enthält, die mit dem Wert im  _Multiplier-Parameter_ multipliziert werden soll. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtMulDw-Funktion** gibt eine **FILETIME-Struktur** zurück, die das Produkt der beiden ganzzahligen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

