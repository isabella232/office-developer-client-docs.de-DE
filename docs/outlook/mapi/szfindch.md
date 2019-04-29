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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421942"
---
# <a name="szfindch"></a>SzFindCh
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sucht nach dem ersten Vorkommen eines Zeichens in einer null-terminierten Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
LPSTR SzFindCh(
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

**SzFindCh** gibt einen Zeiger auf das erste Vorkommen des Zeichens in der Zeichenfolge zurück. Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der _lpsz_ -Parameter NULL ist, wird der Wert NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die **SzFindCh** -Funktion sucht nur nach einer genauen Übereinstimmung. Sie ist anfällig für Groß-/Kleinschreibung und diakritische Unterschiede. Die Suche im Unicode-und im DBCS-Format wird unterstützt. 
  

