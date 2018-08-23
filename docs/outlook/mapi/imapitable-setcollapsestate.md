---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567902"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erstellt den aktuellen erweiterten oder reduzierten den Status einer kategorisierten Tabelle mit Daten, die durch einen vorherigen Aufruf der [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) -Methode gespeichert wurde neu. 
  
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
  
> Reserviert. NULL muss sein.
    
 _cbCollapseState_
  
> [in] Die Anzahl der Bytes in der Struktur auf den durch den Parameter _PbCollapseState_ verwiesen. 
    
 _pbCollapseState_
  
> [in] Zeiger auf die Strukturen, die mit den Daten, die Tabellenansicht neu erstellen.
    
 _lpbkLocation_
  
> [out] Zeiger auf eine Textmarke, identifiziert der Zeile in der Tabelle, an der der reduzierte oder erweiterte Zustand neu erstellt werden soll. Dieses Lesezeichen und im _LpbInstanceKey_ -Parameter im Aufruf [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) übergebenen Instanz Taste identifizieren die gleiche Zeile. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Zustand der kategorisierten Tabelle wurden erfolgreich neu erstellt.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang gestartet wird dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Die Tabelle konnte nicht fertig gestellt Neuerstellen der Ansicht reduzierten oder erweiterten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::SetCollapseState** -Methode wird den Zustand erweiterten oder reduzierten die Tabellenansicht. **SetCollapseState** und **GetCollapseState** arbeiten wie folgt zusammen: 
  
1. Wenn der Zustand einer kategorisierten Tabelle zu ändern, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten für den Zustand vor der Änderung zu speichern. 
    
2. **SetCollapseState** wird aufgerufen, um die Ansicht der Tabelle auf den gespeicherten Zustand wiederherzustellen. Die Daten, die **GetCollapseState** gespeichert werden an **SetCollapseState**übergeben. **SetCollapseState** ist berechtigt, diese Daten verwenden, um den Zustand wiederherzustellen. 
    
3. **SetCollapseState** gibt als Ausgabeparameter eine Textmarke, die die gleiche Zeile als Instanzschlüssel übergeben als Eingabe in **GetCollapseState**identifiziert.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie sind verantwortlich für das Überprüfen, dass die Sortierreihenfolge und Einschränkungen identisch sind, wie sie zum Zeitpunkt des Anrufs **GetCollapseState** waren. Wenn eine Änderung vorgenommen wurde, sollte **SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar können. Dies kann vorkommen, wenn beispielsweise ein Client **GetCollapseState** und dann **SortTable** , um den Sortierschlüssel zu ändern, vor dem Aufruf von **SetCollapseState**aufruft. Aus Sicherheitsgründen sicher, dass die gespeicherten Daten noch gültig ist, bevor Sie mit der Wiederherstellung. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **SetCollapseState**anrufen möchten, müssen Sie zuvor **GetCollapseState**aufgerufen. Die Sortierreihenfolge zur Festlegung der Kategorien sollten für beide Methoden identisch sein. Wenn die Sortierreihenfolgen unterscheiden, sind die Ergebnisse des Vorgangs **SetCollapseState** unvorhersehbar. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

