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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328833"
---
# <a name="imapitablesetcollapsestate"></a>IMAPITable::SetCollapseState

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt den aktuellen erweiterten oder reduzierten Status einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) -Methode gespeichert wurden. 
  
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
  
> Reserviert muss NULL sein.
    
 _cbCollapseState_
  
> in Die Anzahl der Bytes in der Struktur, auf die durch den _pbCollapseState_ -Parameter verwiesen wird. 
    
 _pbCollapseState_
  
> in Zeiger auf die Strukturen, die die zum Neuaufbau der Tabellenansicht erforderlichen Daten enthalten.
    
 _lpbkLocation_
  
> Out Zeiger auf eine Textmarke, die die Zeile in der Tabelle identifiziert, bei der der reduzierte oder erweiterte Zustand neu erstellt werden soll. Diese Textmarke und der Instanzschlüssel, die im _lpbInstanceKey_ -Parameter im Aufruf von [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) übergeben werden, identifizieren dieselbe Zeile. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Status der kategorisierten Tabelle wurde erfolgreich neu erstellt.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Die Tabelle konnte das erneute Erstellen der reduzierten oder erweiterten Ansicht nicht abschließen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: SetCollapseState** -Methode stellt den erweiterten oder reduzierten Status der Tabellenansicht wieder her. **SetCollapseState** und **GetCollapseState** arbeiten wie folgt zusammen: 
  
1. Wenn der Status einer kategorisierten Tabelle gerade geändert wird, wird [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten zu speichern, die sich auf den Status vor der Änderung beziehen. 
    
2. **SetCollapseState** wird aufgerufen, um die Ansicht der Tabelle auf den gespeicherten Zustand zurückzusetzen. Die von **GetCollapseState** gespeicherten Daten werden an **SetCollapseState**übergeben. **SetCollapseState** kann diese Daten verwenden, um den Status wiederherzustellen. 
    
3. **SetCollapseState** gibt als Ausgabeparameter eine Textmarke zurück, die dieselbe Zeile identifiziert wie der Instanzschlüssel, der als Eingabe an **GetCollapseState**übergeben wird.
    
Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Sie sind dafür verantwortlich, zu überprüfen, ob die Sortierreihenfolge und die Einschränkungen identisch sind, wie Sie zum Zeitpunkt des **GetCollapseState** -Aufrufs waren. Wenn eine Änderung vorgenommen wurde, sollte **SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar sein können. Dies kann passieren, wenn beispielsweise ein Client **GetCollapseState** aufruft und dann **sortable** , um den Sortierschlüssel zu ändern, bevor **SetCollapseState**aufgerufen wird. Vergewissern Sie sich, dass die gespeicherten Daten noch gültig sind, bevor Sie mit der Wiederherstellung fortfahren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Aufrufen von **SetCollapseState**müssen Sie zuvor **GetCollapseState**aufgerufen haben. Die Sortierreihenfolge für die Kategorien sollte für beide Methoden identisch sein. Wenn die Sortierreihenfolgen unterschiedlich sind, sind die Ergebnisse der **SetCollapseState** -Operation unvorhersehbar. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

