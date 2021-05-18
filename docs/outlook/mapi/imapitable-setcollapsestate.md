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
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414067"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt den aktuellen erweiterten oder reduzierten Zustand einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der [IMAPITable::GetCollapseState-Methode gespeichert](imapitable-getcollapsestate.md) wurden. 
  
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
  
> Reserviert; muss null sein.
    
 _cbCollapseState_
  
> [in] Anzahl der Bytes in der Struktur, auf die der  _pbCollapseState-Parameter_ verweist. 
    
 _pbCollapseState_
  
> [in] Zeiger auf die Strukturen, die die Daten enthalten, die zum Neuerstellen der Tabellenansicht erforderlich sind.
    
 _lpbkLocation_
  
> [out] Zeiger auf eine Textmarke, die die Zeile in der Tabelle identifiziert, in der der reduzierte oder erweiterte Zustand neu erstellt werden soll. Diese Textmarke und der Instanzschlüssel, der im  _lpbInstanceKey-Parameter_ im Aufruf von [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) übergeben wurde, identifizieren dieselbe Zeile. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der kategorisierten Tabelle wurde erfolgreich neu erstellt.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Die Tabelle konnte die Neuerstellung der reduzierten oder erweiterten Ansicht nicht beenden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::SetCollapseState-Methode** stellt den erweiterten oder reduzierten Zustand der Tabellenansicht wieder ein. **SetCollapseState und** **GetCollapseState** arbeiten wie folgt zusammen: 
  
1. Wenn sich der Status einer kategorisierten Tabelle ändern soll, wird [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten zu speichern, die sich auf den Status vor der Änderung bezieht. 
    
2. Um die Ansicht der Tabelle in ihrem gespeicherten Zustand wiederherzustellen, **wird SetCollapseState** aufgerufen. Die von **GetCollapseState gespeicherten** Daten werden an **SetCollapseState übergeben.** **SetCollapseState** kann diese Daten verwenden, um den Zustand wiederherzustellen. 
    
3. **SetCollapseState** gibt als Ausgabeparameter eine Textmarke zurück, die dieselbe Zeile identifiziert wie die Instanztaste, die als Eingabe an **GetCollapseState übergeben wird.**
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie sind für die Überprüfung verantwortlich, ob die Sortierreihenfolge und die Einschränkungen exakt mit der zum Zeitpunkt des **GetCollapseState-Aufrufs identisch** sind. Wenn eine Änderung vorgenommen wurde, **sollte SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar sein können. Dies kann passieren, wenn ein Client z. B. **GetCollapseState** aufruft und **anschließend SortTable** zum Ändern des Sortierschlüssels vor dem Aufrufen von **SetCollapseState .** Um sicher zu sein, überprüfen Sie, ob die gespeicherten Daten noch gültig sind, bevor Sie mit der Wiederherstellung fortfahren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Aufrufen **von SetCollapseState** müssen Sie zuvor **GetCollapseState aufgerufen haben.** Die Sortierreihenfolge zum Festlegen der Kategorien sollte für beide Methoden identisch sein. Wenn sich die Sortierreihenfolgen unterscheiden, sind die Ergebnisse des **SetCollapseState-Vorgangs** unvorhersehbar. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

