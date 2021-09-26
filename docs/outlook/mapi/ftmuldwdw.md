---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed3ad2249ccc9246febfed74217ae75b8f2daa47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610923"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Multipliziert eine nicht signierte 32-Bit-Ganzzahl mit einer anderen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameter

 _Multiplicand_
  
> [in] Ein Doppelwort, das die nicht signierte 32-Bit-Ganzzahl enthält, die mit dem Wert im  _Parameter "Multiplier"_ multipliziert werden soll. 
    
 _Multiplikator_
  
> [in] Ein Doppelwort, das den 32-Bit-Ganzzahl-Multiplizierer ohne Vorzeichen enthält.
    
## <a name="return-value"></a>Rückgabewert

Die **FtMulDwDw-Funktion** gibt eine [FILETIME-Struktur](filetime.md) zurück, die das Produkt der beiden ganzzahligen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

