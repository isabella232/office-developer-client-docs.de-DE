---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435222"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht das erste Vorkommen einer mit Null beendeten Teilzeichenfolge in einer mit Null beendeten Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die zu durchsuchende Zeichenfolge, die mit Nullen beendet werden soll. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
 _lpszKey_
  
> [in] Zeiger auf die mit Null beendete Teilzeichenfolge, nach der gesucht werden soll. Der  _lpszKey-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge zurück. Wenn die Teilzeichenfolge nicht an einer beliebigen Stelle in der Zeichenfolge auftritt,  _wenn lpszKey_ größer als  _lpsz_ ist oder wenn ein Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die **SzFindSz-Funktion** sucht nur nach einer genauen Übereinstimmung. es ist sensibel auf Fall- und diakritische Unterschiede. Suchen in Unicode- und DBCS-Formaten werden unterstützt. Die Längenbeschränkung für beide Parameter beträgt Zeichen, nicht unbedingt Byte. 
  

