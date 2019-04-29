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
  
Sucht das erste Vorkommen einer null-terminierten Teilzeichenfolge in einer null-terminierten Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> in Zeiger auf die zu durchsuchende NULL-terminierte Zeichenfolge. Der _lpsz_ -parameter darf 65536 Zeichen nicht überschreiten. 
    
 _lpszKey_
  
> in Zeiger auf die mit NULL endende Teilzeichenfolge, nach der gesucht werden soll. Der _lpszKey_ -parameter darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge zurück. Wenn die Teilzeichenfolge an keiner beliebigen Stelle in der Zeichenfolge auftritt, wenn _lpszKey_ größer als _lpsz_ist oder wenn einer der Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **SzFindSz** -Funktion sucht nur nach einer genauen Übereinstimmung. Sie ist anfällig für Groß-/Kleinschreibung und diakritische Unterschiede. Suchvorgänge in Unicode-und DBCS-Formaten werden unterstützt. Die Längenbeschränkung für beide Parameter ist in Zeichen, nicht unbedingt in Bytes. 
  

