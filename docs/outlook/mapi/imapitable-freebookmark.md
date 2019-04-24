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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328929"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den mit einer Textmarke verknüpften Arbeitsspeicher frei.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameter

 _bkPosition_
  
> in Die Textmarke, die freigegeben werden soll, wird durch Aufrufen der [IMAPITable:: CreateBookMark](imapitable-createbookmark.md) -Methode erstellt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Textmarke wurde erfolgreich freigegeben.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die angegebene Textmarke ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: FreeBookmark** -Methode gibt eine nicht mehr benötigte Textmarke frei. Die Textmarke ist nach diesem Aufruf nicht mehr gültig. Wenn eine Tabelle aus dem Arbeitsspeicher veröffentlicht wird, werden auch alle zugehörigen Lesezeichen freigegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Aufrufer eine der drei vordefinierten Lesezeichen im _bkPosition_ -Parameter übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

