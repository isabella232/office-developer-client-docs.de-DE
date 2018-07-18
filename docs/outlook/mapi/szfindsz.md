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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795701"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Betrifft**: Outlook 
  
Sucht den ersten Vorkommens einer Teilzeichenfolge mit Null endende in eine mit Null endende Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> [in] Zeiger auf die Null endende Zeichenfolge, die durchsucht werden soll. Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten. 
    
 _lpszKey_
  
> [in] Zeiger auf Null endende Teilzeichenfolge gesucht werden. Der Parameter _LpszKey_ muss 65536 Zeichen nicht überschreiten. 
    
## <a name="return-value"></a>R�ckgabewert

 **SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge. Wenn die Teilzeichenfolge nicht an einer beliebigen Stelle in der Zeichenfolge auftritt, wenn _LpszKey_ größer als _Lpsz_ist oder einer der Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die Funktion **SzFindSz** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede. Suchvorgänge in Unicode und DBCS-Formate werden unterstützt. Die maximale Länge beide Parameter ist in Zeichen, was nicht notwendigerweise Bytes. 
  

