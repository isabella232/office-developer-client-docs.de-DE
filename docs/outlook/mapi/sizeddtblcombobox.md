---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 463c8e82ab99d3b58f2f506438bd423a44224c65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591122"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLCOMBOBOX-Struktur](dtblcombobox.md) zum Beschreiben eines Kombinationsfeld-Steuerelements und die maximale Anzahl von Zeichen enthält, die in das zugeordnete Bearbeitungssteuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Anzahl der Zeichen, die im Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **"SizedDtblComboBox"** können Sie ein Kombinationsfeld definieren, wenn die Länge der aktivierten Zeichenzeichenfolge bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro "SizedDtblComboBox"** als **DTBLCOMBOBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

