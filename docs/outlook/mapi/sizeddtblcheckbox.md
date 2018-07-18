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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795538"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Betrifft**: Outlook 
  
Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX](dtblcheckbox.md) -Struktur für die Beschreibung ein Kontrollkästchen-Steuerelement und ein Label mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Das Makro **SizedDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Zeichen Bezeichnung bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblCheckBox** als Zeiger Struktur **DTBLCHECKBOX** die folgende Umwandlung: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Siehe auch

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

