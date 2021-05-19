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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419317"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX-Struktur](dtblgroupbox.md) zum Beschreiben eines Gruppenfeldsteuerelements und einer Bezeichnung mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Bezeichnung des Gruppenfelds. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedDtblGroupBox** können Sie ein Gruppenfeldsteuerelement definieren, wenn die Länge der Bezeichnung bekannt ist. Die neue Struktur wird mit den folgenden Mitgliedern erstellt: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblGroupBox-Makros** als **DTBLGROUPBOX-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Siehe auch

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

