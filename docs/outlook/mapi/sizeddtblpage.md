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
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282657"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte Struktur, die eine [DTBLPAGE](dtblpage.md) -Struktur zur Beschreibung eines Steuerelements mit Registerkarten, eine Beschriftung einer angegebenen Länge und einen Hilfedatei Eintrag mit einer angegebenen Länge enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Parameter

_n_
  
> Länge der Bezeichnung für die Registerkarte Seite.
    
_N1_
  
> Die Länge des Eintrags, der in der Datei MAPISVC. inf angezeigt wird und die die Hilfedatei identifiziert, die mit dem Steuerelement für die Registerkartenseite verwendet wird.
    
_u_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedDtblPage** -Makro können Sie ein Seitensteuerelement mit RegisterkartenDefinieren, wenn die Anzahl der Zeichen in der zugeordneten Bezeichnung und dem Hilfedatei Eintrag bekannt ist. Die neue Struktur wird mit den folgenden Elementen erstellt: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblPage** -Makro als **DTBLPAGE** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Siehe auch

- [DTBLPAGE](dtblpage.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

