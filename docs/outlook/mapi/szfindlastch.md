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
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421256"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach dem letzten Vorkommen eines Zeichens in einer mit Null beendeten Zeichenfolge. 
  
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
  
> [in] Zeiger auf die zu durchsuchende Zeichenfolge, die mit Nullen beendet werden soll. 
    
 _ch_
  
> [in] Das zu durchsuchende Zeichen.
    
## <a name="return-value"></a>Rückgabewert

 **SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge zurück. Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt, oder wenn der  _lpsz-Parameter_ NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Hinweise

Die **SzFindLastCh-Funktion** sucht nur nach einer genauen Übereinstimmung. es ist sensibel auf Fall- und diakritische Unterschiede. Suchen im Unicode- und DBCS-Format werden unterstützt. 
  

