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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792461"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Betrifft**: Outlook 
  
Gibt ein Lesezeichen zugeordneten Arbeitsspeicher frei.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameter

 _bkPosition_
  
> [in] Die Textmarke freigegeben werden, werden durch Aufrufen der [IMAPITable::CreateBookmark](imapitable-createbookmark.md) -Methode erstellt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Textmarke wurde erfolgreich freigegeben.
    
MAPI_E_INVALID_BOOKMARK 
  
> Die angegebene Textmarke ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::FreeBookmark** -Methode gibt eine Textmarke, die nicht mehr benötigt wird. Die Textmarke ist nach diesem Aufruf nicht mehr gültig. Wenn eine Tabelle aus dem Speicher freigegeben wird, werden dessen zugehörige Lesezeichen ebenfalls freigegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Aufrufer eine der drei vordefinierten Textmarken im Parameter _BkPosition_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

