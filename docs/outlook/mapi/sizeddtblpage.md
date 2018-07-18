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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795546"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

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

