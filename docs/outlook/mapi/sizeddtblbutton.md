---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795536"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Betrifft**: Outlook 
  
Erstellt eine benannte Struktur, die eine [DTBLBUTTON](dtblbutton.md) -Struktur für die Beschreibung einer Schaltfläche und ein Label mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Parameter

 _n_
  
> Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.
    
 _u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Die neue Struktur wird mit der folgenden Elemente erstellt:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Siehe auch



[DTBLBUTTON](dtblbutton.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

