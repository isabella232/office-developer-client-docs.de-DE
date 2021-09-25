---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5794df4df73d199bf7b0acfc91cc111b0d783b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578641"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLBUTTON-Struktur](dtblbutton.md) zum Beschreiben einer Schaltfläche und einer Beschriftung einer angegebenen Länge enthält. 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die neue Struktur wird mit den folgenden Elementen erstellt:
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Siehe auch



[DTBLBUTTON](dtblbutton.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

