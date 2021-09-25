---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d80bbded22016de0410a50d1beddf4d5f504001
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566661"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLLABEL-Struktur](dtbllabel.md) zum Beschreiben eines Bezeichnungssteuerelements und der zugeordneten Bezeichnung einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Angegeben in der Headerdatei:  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung. Dies schließt das endende NULL-Zeichen ein. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeDtblLabel** können Sie eine Anzeigetabellenbeschriftung definieren, wenn die Anzahl der Zeichen in der Beschriftung bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro SizeDtblLabel** als **DTBLLABEL-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Siehe auch

- [DTBLLABEL](dtbllabel.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

