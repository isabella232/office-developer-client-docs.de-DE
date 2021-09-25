---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 693569c5b7ce6915bc30857445dca5b7e55c63c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613765"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt mehrere Tabellenzeilen ein, wobei möglicherweise vorhandene Zeilen ersetzt werden.
  
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
  
> [in] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die den hinzuzufügenden Zeilensatz enthält, wobei vorhandene Zeilen bei Bedarf ersetzt werden. Eine der Eigenschaftswertstrukturen, auf die vom **lpProps-Element** jeder [SRow-Struktur](srow.md) im Zeilensatz verwiesen wird, sollte die Indexspalte enthalten, denselben Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Mindestens eine der übergebenen Zeilen verfügt nicht über eine Indexspalte. Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData::HrModifyRows-Methode** fügt die Zeilen ein, die durch die [SRowSet-Struktur](srowset.md) beschrieben werden, auf die der  _lpSRowSet-Parameter_ verweist. Wenn der Indexspaltenwert einer Zeile in der Zeilengruppe mit dem Wert für eine vorhandene Zeile in der Tabelle übereinstimmt, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden ist, die der in der **SRowSet-Struktur** enthaltenen Zeile entspricht, fügt **HrModifyRows** die Zeile am Ende der Tabelle hinzu. 
  
Alle Ansichten der Tabelle werden geändert, um die Zeilen einzuschließen, auf die mit  _lpSRowSet_ verwiesen wird. Wenn jedoch eine Ansicht eine Einschränkung enthält, die eine Zeile ausschließt, ist sie möglicherweise nicht für den Benutzer sichtbar. 
  
Die Spalten in den Zeilen, auf die von  _lpSRowSet_ verwiesen wird, müssen nicht in der gleichen Reihenfolge wie die Spalten in der Tabelle sein. Der Aufrufer kann auch Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden. Für vorhandene Ansichten stellt **HrModifyRows** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein. Für zukünftige Ansichten schließt **HrModifyRows** die neuen Spalten in den Spaltensatz ein. 
  
Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die eine Ansicht der Tabelle haben und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. MAPI sendet TABLE_ROW_ADDED oder TABLE_ROW_MODIFIED Benachrichtigungen für jede Zeile, bis zu acht Zeilen. Wenn mehr als acht Zeilen vom **HrModifyRows-Aufruf** betroffen sind, sendet MAPI stattdessen eine einzelne TABLE_CHANGED Benachrichtigung. 
  
## <a name="see-also"></a>Siehe auch



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

