---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420808"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX-Struktur](dtblcheckbox.md) zum Beschreiben eines Kontrollkästchensteuerelements und einer Bezeichnung mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Bezeichnung, die in die neue Struktur eingeschlossen werden soll.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Bezeichnungszeichen bekannt ist. Die neue Struktur wird mit den folgenden Mitgliedern erstellt: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblCheckBox-Makros** als **DTBLCHECKBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Siehe auch

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

