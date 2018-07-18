---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795551"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Betrifft**: Outlook 
  
Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX](dtblgroupbox.md) -Struktur für die Beschreibung ein Gruppenfeld-Steuerelement und ein Label mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der im Gruppenfeld Bezeichnung. 
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Das Makro **SizedDtblGroupBox** können Sie ein Gruppenfeld definieren, wenn die Länge des Bezeichnungsfelds bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblGroupBox** als Zeiger Struktur **DTBLGROUPBOX** die folgende Umwandlung: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

