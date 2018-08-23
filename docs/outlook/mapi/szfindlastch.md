---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570877"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Sucht das letzte Vorkommen eines Zeichens in eine mit Null endende Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge. Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der Parameter _Lpsz_ NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion **SzFindLastCh** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede. Sucht in den Formaten Unicode und DBCS werden unterstützt. 
  

