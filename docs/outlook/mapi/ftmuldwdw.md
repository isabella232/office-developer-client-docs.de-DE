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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592024"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  

