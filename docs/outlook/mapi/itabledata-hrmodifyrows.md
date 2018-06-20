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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15d98183548d4b73c35368d690ef63d5c3dfd9af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792856"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Betrifft**: Outlook 
  
Mehrere Tabellenzeilen, möglicherweise Ersetzen der vorhandene Zeilen eingefügt.
  
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
  
> [in] Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur enthält, die den Satz von Zeilen hinzugefügt werden soll, Ersetzen von vorhandenen Zeilen bei Bedarf. Eine der Eigenschaft Wert Strukturen zum Festlegen anhand der **LpProps** Member jeder [SRow](srow.md) Struktur in der Zeile gezeigt sollte die Indexspalte den gleichen Wert enthalten, die in der _UlPropTagIndexColumn_ -Parameter im Aufruf der [angegeben wurde CreateTable](createtable.md) Funktion. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeilen wurden erfolgreich eingefügt oder geändert.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine oder mehrere Zeilen übergebenen verfügt nicht über eine Indexspalte. Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrModifyRows** -Methode fügt die Zeilen, die durch die [SRowSet](srowset.md) -Struktur, die auf das durch den Parameter _LpSRowSet_ beschrieben. Wenn der Wert von Column Index einer Zeile in der Zeile Set der Wert für eine vorhandene Zeile in der Tabelle entspricht, wird die vorhandene Zeile ersetzt. Wenn keine Zeile vorhanden, die in der Struktur **SRowSet** enthaltene übereinstimmt ist, fügt **HrModifyRows** die Zeile an das Ende der Tabelle an. 
  
Alle Ansichten für die Tabelle werden geändert, um die Zeilen, die auf den _LpSRowSet_enthalten. Jedoch, wenn eine Ansicht eine Einschränkung eingerichtet, die eine Zeile ausschließt hat, es für den Benutzer sichtbar möglicherweise nicht. 
  
Die Spalten in den Zeilen auf den _LpSRowSet_ müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle werden. Der Aufrufer kann auch als Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind. Für vorhandene Ansichten **HrModifyRows** diesen neuen Spalten zur Verfügung umfasst aber nicht sie in der aktuellen Spalte Gruppe. Für zukünftige Ansichten enthält **HrModifyRows** die neuen Spalten in der Spalte festlegen. 
  
Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet. MAPI sendet TABLE_ROW_ADDED oder TABLE_ROW_MODIFIED Benachrichtigungen für jede Zeile, bis zu acht Zeilen. Wenn mehr als acht Zeilen betroffen sind durch den Aufruf von **HrModifyRows** sendet MAPI eine einzelne TABLE_CHANGED Benachrichtigung stattdessen. 
  
## <a name="see-also"></a>Siehe auch



[' Srowset '](srowset.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

