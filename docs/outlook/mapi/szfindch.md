---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795697"
---
# <a name="szfindch"></a>SzFindCh
 
**Betrifft**: Outlook 
  
Sucht nach dem ersten Vorkommen eines Zeichens in eine mit Null endende Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameter

_lpsz_
  
> [in] Zeiger auf die Null endende Zeichenfolge, die durchsucht werden soll. 
    
_Kapitel_
  
> [in] Das Zeichen an, nach dem gesucht wird.
    
## <a name="return-value"></a>R�ckgabewert

**SzFindCh** gibt einen Zeiger auf das erste Auftreten des Zeichens in der Zeichenfolge. Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der Parameter _Lpsz_ NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die Funktion **SzFindCh** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede. Sucht in den Formaten Unicode und DBCS werden unterstützt. 
  

