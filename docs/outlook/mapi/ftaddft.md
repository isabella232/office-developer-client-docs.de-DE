---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 36b5a8754d1cf111a84e9b0e442ca5ab3c4afcf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576247"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt eine unsignierte 64-Bit-Ganzzahl zu einer anderen hinzu.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parameter

 _Addend1_
  
> [in] Eine [FILETIME-Struktur,](filetime.md) die die erste nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
 _Addend2_
  
> [in] Eine **FILETIME-Struktur,** die die zweite nicht signierte 64-Bit-Ganzzahl enthält, die hinzugefügt werden soll. 
    
## <a name="return-value"></a>Rückgabewert

Die **FtAddFt-Funktion** gibt eine **FILETIME-Struktur** zurück, die die Summe der beiden ganzzahligen Zahlen enthält. Die beiden Eingabeparameter bleiben unverändert. 
  

