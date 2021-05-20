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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437644"
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
  
> Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedDtblEdit** können Sie ein Bearbeitungssteuerelement definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist. Die neue Struktur wird mit den folgenden Mitgliedern erstellt: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizeDtblEdit-Makros** als **DTBLEDIT-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Siehe auch

- [DTBLEDIT](dtbledit.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

