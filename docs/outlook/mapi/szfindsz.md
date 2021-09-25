---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 464c6ed3ce2c56339d38ec21648922618d1a4ad9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619645"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht das erste Vorkommen einer Teilzeichenfolge, die mit NULL beendet wurde, in einer Zeichenfolge, die mit NULL beendet wurde. 
  
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
  
> [in] Zeiger auf die zeichenfolge mit NULL-Termin, die durchsucht werden soll. Der  _lpsz-Parameter_ darf 65536 Zeichen nicht überschreiten. 
    
 _lpszKey_
  
> [in] Zeiger auf die Teilzeichenfolge, die mit NULL beendet wird, nach der gesucht werden soll. Der  _parameter lpszKey_ darf 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>Rückgabewert

 **SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge zurück. Wenn die Teilzeichenfolge an keiner Stelle in der Zeichenfolge auftritt,  _lpszKey_ größer als  _lpsz_ ist oder wenn einer der Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **SzFindSz-Funktion** sucht nur nach einer genauen Übereinstimmung; Dabei wird auf Groß-/Kleinschreibung und diakritische Unterschiede unterschieden. Suchvorgänge im Unicode- und DBCS-Format werden unterstützt. Der Längengrenzwert für beide Parameter ist in Zeichen angegeben, nicht unbedingt in Byte. 
  

