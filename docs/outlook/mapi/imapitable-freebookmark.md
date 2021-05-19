---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409454"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Speicher frei, der einer Textmarke zugeordnet ist.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameter

 _bkPosition_
  
> [in] Das zu entfernende Lesezeichen, das durch Aufrufen der [IMAPITable::CreateBookmark-Methode erstellt](imapitable-createbookmark.md) wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Textmarke wurde erfolgreich frei.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die angegebene Textmarke ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::FreeBookmark-Methode** gibt ein Lesezeichen frei, das nicht mehr benötigt wird. Das Lesezeichen ist nach diesem Aufruf nicht mehr gültig. Wenn eine Tabelle aus dem Arbeitsspeicher freigegeben wird, werden auch alle zugehörigen Lesezeichen freigegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Aufrufer eine der drei vordefinierten Lesezeichen im  _bkPosition-Parameter_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

