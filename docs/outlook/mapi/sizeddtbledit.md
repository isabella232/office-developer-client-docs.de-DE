---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795543"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Betrifft**: Outlook 
  
Erstellt eine benannte Struktur, die enthält eine [DTBLEDIT](dtbledit.md) -Struktur für die Beschreibung ein Edit-Steuerelement und die maximale Anzahl von Zeichen, die im Steuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Das Makro **SizedDtblEdit** können Sie ein Edit-Steuerelement zu definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblEdit** als Zeiger Struktur **DTBLEDIT** die folgende Umwandlung: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Siehe auch

- [DTBLEDIT](dtbledit.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

