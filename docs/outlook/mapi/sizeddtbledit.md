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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282803"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLEDIT](dtbledit.md) -Struktur zur Beschreibung eines Bearbeitungssteuerelements und die maximale Anzahl von Zeichen enthält, die im Steuerelement eingegeben werden können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedDtblEdit** -Makro können Sie ein Bearbeitungssteuerelement definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblEdit** -Makro als **DTBLEDIT** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Siehe auch

- [DTBLEDIT](dtbledit.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

