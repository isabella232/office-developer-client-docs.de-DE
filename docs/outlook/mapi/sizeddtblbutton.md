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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a7d62d29638ae234667eb33a8103fb3a716afc32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421914"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLBUTTON-Struktur](dtblbutton.md) zum Beschreiben einer Schaltfläche und einer Bezeichnung mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Parameter

 _n_
  
> Länge der Bezeichnung, die in die neue Struktur eingeschlossen werden soll.
    
 _u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Die neue Struktur wird mit den folgenden Mitgliedern erstellt:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Siehe auch



[DTBLBUTTON](dtblbutton.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

