---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af518be23c8bd192ca9fd2b8d987cd64c4562287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592333"
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
  
> [out] Zeiger auf einen Zeiger auf die [SSortOrderSet-Struktur,](ssortorderset.md) die die aktuelle Sortierreihenfolge enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortierreihenfolge-Abrufvorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::QuerySortOrder-Methode** ruft die aktuelle Sortierreihenfolge für eine Tabelle ab. Sortierreihenfolgen werden mit einer [SSortOrderSet-Struktur](ssortorderset.md) beschrieben. 
  
- Das **cSorts-Element** der **SSortOrderSet-Struktur** kann auf Null festgelegt werden, wenn: 
    
- Die Tabelle ist unsortiert.
    
- Es gibt keine Informationen darüber, wie die Tabelle sortiert wird.
    
- Die **SSortOrderSet-Struktur** ist nicht geeignet, um die Sortierreihenfolge zu beschreiben. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) mit einer **SSortOrderSet-Struktur** aufgerufen wird, die keine Spalten in der Sortiertaste enthält, entfernen Sie die aktuelle Sortierreihenfolge, und wenden Sie die Standardreihenfolge an, falls vorhanden. In nachfolgenden Aufrufen von **QuerySortOrder** können Sie auswählen, ob null oder mehr Spalten für den Sortierschlüssel zurückgegeben werden sollen. Sie können mehr Spalten zurückgeben, als in der aktuellen Ansicht vorhanden sind.
  
Weitere Informationen zum Sortieren finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::SortTable](imapitable-sorttable.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

