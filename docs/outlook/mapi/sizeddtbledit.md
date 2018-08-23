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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591660"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

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

