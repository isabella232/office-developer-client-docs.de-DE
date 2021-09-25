---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a9f5b2d26c4cfaa0232193e1a75ca3a7edca7a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566675"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX-Struktur](dtblgroupbox.md) zum Beschreiben eines Gruppenfeld-Steuerelements und einer Beschriftung einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung des Gruppenfelds. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeDtblGroupBox** können Sie ein Gruppenfeld-Steuerelement definieren, wenn die Länge der Bezeichnung bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro "SizedDtblGroupBox"** als **DTBLGROUPBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

