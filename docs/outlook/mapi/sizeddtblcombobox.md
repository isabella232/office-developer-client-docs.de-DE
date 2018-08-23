---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593655"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die enthält eine [DTBLCOMBOBOX](dtblcombobox.md) -Struktur für die Beschreibung ein Kombinationsfeld-Steuerelement und die maximale Anzahl von Zeichen, die in der zugehörigen Bearbeitungssteuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Anzahl der Zeichen, die in des Kombinationsfelds eingegeben werden können edit-Steuerelement. 
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **SizedDtblComboBox** können Sie einem Kombinationsfeld definieren, wenn die Länge der Zeichenfolge aktiviert bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblComboBox** als Zeiger Struktur **DTBLCOMBOBOX** die folgende Umwandlung: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

