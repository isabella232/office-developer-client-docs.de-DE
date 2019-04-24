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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328007"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine unsignierte 64-Bit-Ganzzahl zu einem anderen hinzu.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parameter

 _Addend1_
  
> in Eine [FILETIME](filetime.md) -Struktur, die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
 _Addend2_
  
> in Eine **FILETIME** -Struktur, die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtAddFt** -Funktion gibt **** eine FILETIME-Struktur zurück, die die Summe der beiden ganzen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

