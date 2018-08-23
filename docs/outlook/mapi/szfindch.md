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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573523"
---
# <a name="szfindch"></a>SzFindCh
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion **SzFindCh** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede. Sucht in den Formaten Unicode und DBCS werden unterstützt. 
  

