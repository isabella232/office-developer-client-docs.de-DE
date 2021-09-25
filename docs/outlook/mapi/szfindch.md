---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 78614af6a9f00fb5e4e0904f9774dc3c5b8494da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578529"
---
# <a name="szfindch"></a>SzFindCh
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach dem ersten Vorkommen eines Zeichens in einer Zeichenfolge mit NULL-Terminierung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameter

_lpsz_
  
> [in] Zeiger auf die zeichenfolge mit NULL-Termin, die durchsucht werden soll. 
    
_Ch_
  
> [in] Das Zeichen, nach dem gesucht werden soll.
    
## <a name="return-value"></a>Rückgabewert

**SzFindCh** gibt einen Zeiger auf das erste Vorkommen des Zeichens in der Zeichenfolge zurück. Wenn das Zeichen an keiner Stelle in der Zeichenfolge auftritt oder wenn der  _Lpsz-Parameter_ NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **SzFindCh-Funktion** sucht nur nach einer genauen Übereinstimmung. Dabei wird auf Groß-/Kleinschreibung und diakritische Unterschiede unterschieden. Suchvorgänge im Unicode- und DBCS-Format werden unterstützt. 
  

