---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583995"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
64-Bit-Ganzzahl ohne Vorzeichen durch eine 32-Bit-Ganzzahl ohne Vorzeichen multipliziert.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parameter

 _Multiplikator_
  
> [in] Ein Wort, Double-Wert, der den 32-Bit-Ganzzahl ohne Vorzeichen Multiplikator enthält. 
    
 _Multiplikand_
  
> [in] Ein [FILETIME](filetime.md) -Struktur, die 64-Bit-Ganzzahl ohne Vorzeichen, mit dem im Parameter _Multiplikator_ multipliziert werden enthält. 
    
## <a name="return-value"></a>R�ckgabewert

Die **FtMulDw** -Funktion gibt eine **FILETIME** -Struktur, die das Produkt von zwei Ganzzahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

