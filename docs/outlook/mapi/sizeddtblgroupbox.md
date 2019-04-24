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
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282733"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX](dtblgroupbox.md) -Struktur zur Beschreibung eines Gruppenfeld-Steuerelements und einer Beschriftung einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung des Gruppenfelds. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedDtblGroupBox** -Makro können Sie ein Gruppenfeld-Steuerelement definieren, wenn die Länge der Bezeichnung bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblGroupBox** -Makro als **DTBLGROUPBOX** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

