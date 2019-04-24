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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345136"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach dem letzten Vorkommen eines Zeichens in einer null-terminierten Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameter

 _lpsz_
  
> in Zeiger auf die zu durchsuchende NULL-terminierte Zeichenfolge. 
    
 _ch_
  
> in Das Zeichen, nach dem gesucht werden soll.
    
## <a name="return-value"></a>Rückgabewert

 **SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge zurück. Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der _lpsz_ -Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **SzFindLastCh** -Funktion sucht nur nach einer genauen Übereinstimmung. Sie ist anfällig für Groß-/Kleinschreibung und diakritische Unterschiede. Die Suche im Unicode-und im DBCS-Format wird unterstützt. 
  

