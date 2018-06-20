---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792465"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Betrifft**: Outlook 
  
Ruft die aktuelle Sortierreihenfolge für eine Tabelle an.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parameter

 _lppSortCriteria_
  
> [out] Zeiger auf einen Zeiger auf die [SSortOrderSet](ssortorderset.md) -Struktur, die die aktuelle Sortierreihenfolge. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Reihenfolge sortieren nicht gestartet dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::QuerySortOrder** -Methode ruft die aktuelle Sortierreihenfolge für eine Tabelle. Sortierreihenfolgen werden mit einer [SSortOrderSet](ssortorderset.md) Struktur beschrieben. 
  
- Der **cSorts** Member der Struktur **SSortOrderSet** kann wenn auf 0 (null) festgelegt werden: 
    
- Die Tabelle ist nicht sortiert.
    
- Es gibt keine Informationen darüber, wie die Tabelle sortiert ist.
    
- Die Struktur **SSortOrderSet** eignet sich nicht für die Beschreibung der Sortierreihenfolge. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn Ihre [SortTable](imapitable-sorttable.md) -Methode mit einer **SSortOrderSet** Struktur, enthält keine Spalten in der Sortierschlüssel aufgerufen wird, entfernen Sie die aktuelle Sortierreihenfolge und wenden Sie die Standardreihenfolge an, sofern vorhanden. Bei nachfolgenden Aufrufen von **QuerySortOrder**können Sie auswählen, ob NULL oder mehr Spalten für den Sortierschlüssel zurückzugeben. Sie können weitere Spalten als in der Ansicht vorhanden sind zurückgeben.
  
Weitere Informationen zum Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

