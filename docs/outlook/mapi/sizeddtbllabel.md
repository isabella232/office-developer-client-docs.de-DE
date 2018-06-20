---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795560"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Betrifft**: Outlook 
  
Erstellt eine benannte Struktur, die eine [DTBLLABEL](dtbllabel.md) -Struktur für die Beschreibung ein Label-Steuerelement und das zugeordnete Beschriftung an einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|In der Headerdatei angegeben:  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung. Dazu gehört das letzte Zeichen NULL. 
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Das Makro **SizedDtblLabel** können Sie eine Beschriftung anzeigen Tabelle definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblLabel** als Zeiger Struktur **DTBLLABEL** die folgende Umwandlung: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Siehe auch

- [DTBLLABEL](dtbllabel.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

