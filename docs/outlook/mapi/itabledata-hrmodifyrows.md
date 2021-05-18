---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405359"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt mehrere Tabellenzeilen ein und ersetzt möglicherweise vorhandene Zeilen.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpSRowSet_
  
> [in] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die zu hinzufügende Gruppe von Zeilen enthält und bei Bedarf vorhandene Zeilen ersetzt. Eine der Eigenschaftenwertstrukturen, auf die das **lpProps-Element** jeder [SRow-Struktur](srow.md) im Zeilensatz verweist, sollte die Indexspalte enthalten, denselben Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine der übergebenen Zeilen verfügt nicht über eine Indexspalte. Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrModifyRows-Methode** fügt die Zeilen ein, die von der [SRowSet-Struktur](srowset.md) beschrieben werden, auf die der  _lpSRowSet-Parameter_ verweist. Wenn der Indexspaltenwert einer Zeile im Zeilensatz dem Wert für eine vorhandene Zeile in der Tabelle entspricht, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die der in der **SRowSet-Struktur** enthaltenen Zeile entspricht, fügt **HrModifyRows** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden so geändert, dass sie die Zeilen enthalten, auf die _von lpSRowSet verwiesen wird._ Wenn eine Ansicht jedoch eine Einschränkung hat, die eine Zeile ausschließt, ist sie möglicherweise nicht für den Benutzer sichtbar. 
  
Die Spalten in den Zeilen, auf die  _von lpSRowSet_ verwiesen wird, müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein. Der Aufrufer kann auch Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind. Für vorhandene Ansichten **stellt HrModifyRows** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein. Für zukünftige Ansichten **enthält HrModifyRows** die neuen Spalten im Spaltensatz. 
  
Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. MAPI sendet TABLE_ROW_ADDED oder TABLE_ROW_MODIFIED Benachrichtigungen für jede Zeile, bis zu acht Zeilen. Wenn mehr als acht Zeilen vom **HrModifyRows-Aufruf** betroffen sind, sendet MAPI stattdessen eine TABLE_CHANGED Benachrichtigung. 
  
## <a name="see-also"></a>Siehe auch



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

