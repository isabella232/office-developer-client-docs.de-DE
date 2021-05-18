---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412912"
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

 _Multiplikation_
  
> [in] Ein Doppeltes Wort, das die nicht signierte ganzzahlige 32-Bit-Zahl enthält, die mit dem Wert im  _Multiplikatorparameter multipliziert werden_ soll. 
    
 _Multiplikator_
  
> [in] Ein Doppelwort, das den nicht signierten 32-Bit-Ganzzahlmultiplikator enthält.
    
## <a name="return-value"></a>Rückgabewert

Die **FtMulDwDw-Funktion** gibt eine [FILETIME-Struktur](filetime.md) zurück, die das Produkt der beiden ganzzahligen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

