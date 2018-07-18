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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791763"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Betrifft**: Outlook 
  
Multipliziert einer 32-Bit-Ganzzahl ohne Vorzeichen mit einer anderen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameter

 _Multiplikand_
  
> [in] Double Wort enthält, die 32-Bit-Ganzzahl ohne Vorzeichen durch den Wert im Parameter _Multiplikator_ multipliziert werden soll. 
    
 _Multiplikator_
  
> [in] Ein Wort, Double-Wert, der den 32-Bit-Ganzzahl ohne Vorzeichen Multiplikator enthält.
    
## <a name="return-value"></a>R�ckgabewert

Die **FtMulDwDw** -Funktion gibt eine [FILETIME](filetime.md) -Struktur, die das Produkt von zwei Ganzzahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

