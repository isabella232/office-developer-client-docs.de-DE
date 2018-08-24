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
ms.openlocfilehash: 36d1518764985c4783d967e263ca5c05d63f935f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588482"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::FreeBookmark** -Methode gibt eine Textmarke, die nicht mehr benötigt wird. Die Textmarke ist nach diesem Aufruf nicht mehr gültig. Wenn eine Tabelle aus dem Speicher freigegeben wird, werden dessen zugehörige Lesezeichen ebenfalls freigegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Aufrufer eine der drei vordefinierten Textmarken im Parameter _BkPosition_ übergibt, ignorieren Sie die Anforderung, und geben Sie S_OK zurück. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

