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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282824"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLCOMBOBOX](dtblcombobox.md) -Struktur zur Beschreibung eines Kombinationsfeld-Steuerelements und die maximale Anzahl von Zeichen enthält, die im zugeordneten Bearbeitungssteuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Die Anzahl der Zeichen, die im Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedDtblComboBox** -Makro können Sie ein Kombinationsfeld definieren, wenn die Länge der aktivierten Zeichenfolge bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblComboBox** -Makro als **DTBLCOMBOBOX** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

