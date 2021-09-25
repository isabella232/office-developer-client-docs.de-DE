---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9282562032279ab11a36d0ed1687ccd1d1ae8365
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586726"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX-Struktur](dtblcheckbox.md) zum Beschreiben eines Kontrollkästchen-Steuerelements und einer Beschriftung einer angegebenen Länge enthält. 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Beschriftungszeichen bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro "SizedDtblCheckBox"** als **DTBLCHECKBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Siehe auch

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

