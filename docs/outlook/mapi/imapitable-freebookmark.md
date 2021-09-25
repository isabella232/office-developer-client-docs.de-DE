---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb8c31f399c32b3e5ddeb16aa67efb94e2bcadce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600918"
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
  
> [in] Die freizugebende Textmarke, die durch Aufrufen der [IMAPITable::CreateBookmark-Methode](imapitable-createbookmark.md) erstellt wird. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Lesezeichen wurde erfolgreich freigegeben.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die angegebene Textmarke ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::FreeBookmark-Methode** gibt ein Lesezeichen frei, das nicht mehr benötigt wird. Das Lesezeichen ist nach diesem Aufruf nicht mehr gültig. Wenn eine Tabelle aus dem Arbeitsspeicher freigegeben wird, werden auch alle zugehörigen Lesezeichen freigegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Aufrufer eine der drei vordefinierten Textmarken im  _bkPosition-Parameter_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

