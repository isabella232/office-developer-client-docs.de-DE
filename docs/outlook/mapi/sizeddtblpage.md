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
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584968"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLPAGE](dtblpage.md) -Struktur für die Beschreibung eines Steuerelements mit Registerkarten, ein Label mit einer angegebenen Länge und einen Eintrag Hilfe Datei mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Beschriftung für die Registerkarte Seite.
    
_N1_
  
> Die Länge des Eintrags angezeigt wird, in der Datei "Mapisvc.inf", identifiziert der Hilfedatei, die mit der mit Registerkarten-Seitensteuerelement verwendet werden.
    
_u_
  
> Der Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **SizedDtblPage** können Sie eine mit Registerkarten-Seitensteuerelement zu definieren, wenn die Anzahl der Zeichen in der zugeordneten Label und Hilfe Protokolldateieintrag bekannt ist. Die neue Struktur wird mit der folgenden Elemente erstellt: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblPage** als Zeiger Struktur **DTBLPAGE** die folgende Umwandlung: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Siehe auch

- [DTBLPAGE](dtblpage.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

