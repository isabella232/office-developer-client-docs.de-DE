---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407445"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLPAGE-Struktur](dtblpage.md) zum Beschreiben eines Seitensteuerelements mit Registerkarten, eine Bezeichnung einer angegebenen Länge und einen Hilfedateieintrag mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung für die Seitenregisterkarte.
    
_n1_
  
> Länge des Eintrags, der in der Datei Mapisvc.inf angezeigt wird und die Hilfedatei identifiziert, die mit dem Seitensteuerelement mit Registerkarten verwendet wird.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Hinweise

Mit **dem Makro SizedDtblPage** können Sie ein Seitensteuerelement mit Registerkarten definieren, wenn die Anzahl der Zeichen in der zugeordneten Bezeichnung und dem Hilfedateieintrag bekannt ist. Die neue Struktur wird mit den folgenden Mitgliedern erstellt: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblPage-Makros** als **DTBLPAGE-Strukturzeiger** zu verwenden: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Siehe auch

- [DTBLPAGE](dtblpage.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

