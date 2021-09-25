---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 25cd7e09b08e9a7069cef4c718af86b829022015
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625301"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt den aktuellen erweiterten oder reduzierten Status einer kategorisierten Tabelle mithilfe von Daten neu, die durch einen vorherigen Aufruf der [IMAPITable::GetCollapseState-Methode](imapitable-getcollapsestate.md) gespeichert wurden. 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> Reserviert; muss Null sein.
    
 _cbCollapseState_
  
> [in] Anzahl der Bytes in der Struktur, auf die der  _PbCollapseState-Parameter_ verweist. 
    
 _pbCollapseState_
  
> [in] Zeiger auf die Strukturen mit den Daten, die zum Neuerstellen der Tabellenansicht erforderlich sind.
    
 _lpbkLocation_
  
> [out] Zeiger auf eine Textmarke, die die Zeile in der Tabelle identifiziert, in der der reduzierte oder erweiterte Zustand neu erstellt werden soll. Diese Textmarke und der Instanzschlüssel, der im Parameter  _lpbInstanceKey_ im Aufruf von [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) übergeben wird, identifizieren dieselbe Zeile. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der kategorisierten Tabelle wurde erfolgreich neu erstellt.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Die Neuerstellung der reduzierten oder erweiterten Ansicht konnte von der Tabelle nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::SetCollapseState-Methode** legt den erweiterten oder reduzierten Zustand der Tabellenansicht wieder her. **SetCollapseState** und **GetCollapseState** arbeiten wie folgt zusammen: 
  
1. Wenn sich der Status einer kategorisierten Tabelle ändert, wird [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten zu speichern, die vor der Änderung zum Status gehören. 
    
2. Um die Ansicht der Tabelle in den gespeicherten Zustand wiederherzustellen, wird **"SetCollapseState"** aufgerufen. Die von **GetCollapseState** gespeicherten Daten werden an **SetCollapseState** übergeben. **SetCollapseState** kann diese Daten verwenden, um den Zustand wiederherzustellen. 
    
3. **SetCollapseState** gibt als Ausgabeparameter eine Textmarke zurück, die dieselbe Zeile wie der als Eingabe an **GetCollapseState** übergebene Instanzschlüssel identifiziert.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisieren.](sorting-and-categorization.md) 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie sind dafür verantwortlich, zu überprüfen, ob die Sortierreihenfolge und die Einschränkungen genau mit denen zum Zeitpunkt des **GetCollapseState-Aufrufs** übereinstimmen. Wenn eine Änderung vorgenommen wurde, sollte **SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar sein können. Dies kann beispielsweise passieren, wenn ein Client **GetCollapseState** und dann **SortTable** aufruft, um den Sortierschlüssel vor dem Aufrufen von **SetCollapseState** zu ändern. Um sicher zu sein, überprüfen Sie, ob die gespeicherten Daten noch gültig sind, bevor Sie mit der Wiederherstellung fortfahren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um **SetCollapseState** aufzurufen, müssen Sie zuvor **GetCollapseState** aufgerufen haben. Die Sortierreihenfolge, in der die Kategorien festgelegt werden, sollte für beide Methoden identisch sein. Wenn sich die Sortierreihenfolgen unterscheiden, sind die Ergebnisse des **SetCollapseState-Vorgangs** unvorhersehbar. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

