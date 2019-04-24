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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328861"
---
# <a name="imapitablequerysortorder"></a>IMAPITable::QuerySortOrder

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a>Parameter

 _lppSortCriteria_
  
> Out Zeiger auf einen Zeiger auf die [SSortOrderSet](ssortorderset.md) -Struktur, die die aktuelle Sortierreihenfolge aufweist. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Abrufvorgang für die Sortierreihenfolge gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: QuerySortOrder** -Methode ruft die aktuelle Sortierreihenfolge für eine Tabelle ab. Sortierreihenfolgen werden mit einer [SSortOrderSet](ssortorderset.md) -Struktur beschrieben. 
  
- Das **cSorts** -Element der **SSortOrderSet** -Struktur kann auf 0 (null) festgelegt werden, wenn: 
    
- Die Tabelle ist unsortiert.
    
- Es gibt keine Informationen dazu, wie die Tabelle sortiert wird.
    
- Die **SSortOrderSet** -Struktur ist nicht geeignet, um die Sortierreihenfolge zu beschreiben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Aufruf an Ihre [IMAPITable:: sortable](imapitable-sorttable.md) -Methode mit einer **SSortOrderSet** -Struktur mit NULL-Spalten im Sortierschlüssel erfolgt, entfernen Sie die aktuelle Sortierreihenfolge, und übernehmen Sie die Standardreihenfolge, sofern vorhanden. In nachfolgenden Aufrufen von **QuerySortOrder**können Sie auswählen, ob NULL oder mehr Spalten für den Sortierschlüssel zurückgegeben werden sollen. Sie können mehr Spalten als in der aktuellen Ansicht zurückgeben.
  
Weitere Informationen zum Sortieren finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

