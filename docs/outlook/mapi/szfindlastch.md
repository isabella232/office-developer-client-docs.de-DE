---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0c8d18b39b417e7cf2b0df6e0e271dd432ba9348
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566339"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach dem letzten Vorkommen eines Zeichens in einer Zeichenfolge mit NULL-Terminierung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge zurück. Wenn das Zeichen an keiner Stelle in der Zeichenfolge auftritt oder wenn der  _Lpsz-Parameter_ NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **SzFindLastCh-Funktion** sucht nur nach einer genauen Übereinstimmung; Dabei wird auf Groß-/Kleinschreibung und diakritische Unterschiede unterschieden. Suchvorgänge im Unicode- und DBCS-Format werden unterstützt. 
  

