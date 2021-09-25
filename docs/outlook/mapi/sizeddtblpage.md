---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 344403fa1dd4301ab6dee0118d30d23df8c3b1bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566626"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLPAGE-Struktur](dtblpage.md) zum Beschreiben eines Seitensteuerelements mit Registerkarten, einer Beschriftung einer angegebenen Länge und eines Hilfedateieintrags mit einer bestimmten Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung für die Registerkarte "Seite".
    
_n1_
  
> Die Länge des Eintrags, der in der Datei Mapisvc.inf angezeigt wird und die Hilfedatei identifiziert, die mit dem Seitensteuerelement im Registerkartenformat verwendet wird.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeDtblPage** können Sie ein Seitensteuerelement mit Registerkarten definieren, wenn die Anzahl der Zeichen in der zugeordneten Beschriftung und dem Eintrag in der Hilfedatei bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Führen Sie die folgende Umwandlung aus, um einen Zeiger auf die resultierende Struktur aus dem **Makro "SizedDtblPage"** als **DTBLPAGE-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Siehe auch

- [DTBLPAGE](dtblpage.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

