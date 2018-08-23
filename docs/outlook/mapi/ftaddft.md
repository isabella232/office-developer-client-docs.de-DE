---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b02fc316001ae11d64988cc29d0e62e9adde55e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585584"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Fügt einer 64-Bit-Ganzzahl ohne Vorzeichen in eine andere.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parameter

 _Addend1_
  
> [in] Ein [FILETIME](filetime.md) -Struktur, die enthält die erste 64-Bit-Ganzzahl hinzugefügt werden soll. 
    
 _Addend2_
  
> [in] Ein **FILETIME** -Struktur, die enthält die zweite 64-Bit-Ganzzahl hinzugefügt werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

Die **FtAddFt** -Funktion gibt eine **FILETIME** -Struktur, die die Summe der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

