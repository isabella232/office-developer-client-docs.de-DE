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
  
Fügt mehrere Tabellenzeilen ein, die möglicherweise vorhandene Zeilen ersetzen.
  
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
  
> in Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den Satz von Zeilen enthält, der hinzugefügt werden soll, und ggf. vorhandene Zeilen ersetzen. Eine der Eigenschaftswert Strukturen, auf die durch das **lpProps** -Element jeder [SRow](srow.md) -Struktur im Zeilensatz verwiesen wird, sollte die Indexspalte enthalten, den gleichen Wert, der im _ulPropTagIndexColumn_ -Parameter im Aufruf der [ Createable](createtable.md) -Funktion. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine der übergebenen Zeilen verfügt über keine Indexspalte. Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrModifyRows** -Methode fügt die von der [SRowSet](srowset.md) -Struktur beschriebenen Zeilen ein, auf die durch den _lpSRowSet_ -Parameter verwiesen wird. Wenn der Index Spaltenwert einer Zeile im Zeilensatz mit dem Wert einer vorhandenen Zeile in der Tabelle übereinstimmt, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die mit der in der **SRowSet** -Struktur übereinstimmt, fügt **HrModifyRows** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden so geändert, dass Sie die Zeilen einbeziehen, auf die von _lpSRowSet_verwiesen wird. Wenn in einer Ansicht jedoch eine Einschränkung vorhanden ist, die eine Zeile ausschließt, ist Sie möglicherweise für den Benutzer nicht sichtbar. 
  
Die Spalten in den Zeilen, auf die von _lpSRowSet_ verwiesen wird, müssen sich nicht in derselben Reihenfolge wie die Spalten in der Tabelle befinden. Der Aufrufer kann auch als Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden. Bei vorhandenen Ansichten stellt **HrModifyRows** diese neuen Spalten zur Verfügung, diese werden jedoch nicht in den aktuellen Spaltensatz aufgenommen. Für zukünftige Ansichten enthält **HrModifyRows** die neuen Spalten in den Spaltensatz. 
  
Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. MAPI sendet TABLE_ROW_ADDED-oder TABLE_ROW_MODIFIED-Benachrichtigungen für jede Zeile, bis zu acht Zeilen. Wenn der **HrModifyRows** -Aufruf mehr als acht Zeilen betrifft, sendet MAPI stattdessen eine einzelne TABLE_CHANGED-Benachrichtigung. 
  
## <a name="see-also"></a>Siehe auch



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

