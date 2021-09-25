---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22ff75605b9ab7911f0a270a17631f8261b54ffc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566682"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLEDIT-Struktur](dtbledit.md) zum Beschreiben eines Bearbeitungssteuerelements und die maximale Anzahl von Zeichen enthält, die in das Steuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Maximale Anzahl von Zeichen, die in das Bearbeitungssteuerelement eingegeben werden können.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeDtblEdit** können Sie ein Bearbeitungssteuerelement definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro SizeDtblEdit** als **DTBLEDIT-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Siehe auch

- [DTBLEDIT](dtbledit.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

