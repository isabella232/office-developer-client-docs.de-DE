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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408614"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLLABEL](dtbllabel.md) -Struktur zur Beschreibung eines Label-Steuerelements und der zugeordneten Beschriftung einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Angegeben in der Headerdatei:  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Bezeichnung. Dazu gehört das endGÜLTIGes NULL-Zeichen. 
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedDtblLabel** -Makro können Sie eine Anzeige Tabellenbeschriftung definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblLabel** -Makro als **DTBLLABEL** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus: 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Siehe auch

- [DTBLLABEL](dtbllabel.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

