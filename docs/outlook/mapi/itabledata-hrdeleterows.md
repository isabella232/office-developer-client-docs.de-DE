---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416454"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht mehrere Tabellenzeilen.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Löschvorgang steuert. Das folgende Flag kann festgelegt werden:
    
TAD_ALL_ROWS 
  
> Löscht alle Zeilen aus der Tabelle und allen entsprechenden Ansichten und sendet eine TABLE_RELOAD Benachrichtigung.
    
 _lprowsetToDelete_
  
> [in] Ein Zeiger auf einen Zeilensatz, der die zu löschende Zeile beschreibt. Der  _lprowsetToDelete-Parameter_ kann NULL sein, wenn TAD_ALL_ROWS im  _ulFlags-Parameter festgelegt_ ist. 
    
 _cRowsDeleted_
  
> [out] Die Anzahl der gelöschten Zeilen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabellenzeilen wurden erfolgreich gelöscht.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrDeleteRows-Methode** sucht und entfernt die Tabellenzeilen, die die Spalten enthalten, die mit der Eigenschaft übereinstimmen, auf die das **lpProps-Mitglied** jedes **aRow-Eintrags** im Zeilensatz verweist. Zum Identifizieren jeder Zeile wird eine Indexspalte verwendet. Diese Spalte muss das gleiche Eigenschaftstag wie das Eigenschaftstag haben, das im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion übergeben](createtable.md) wird. 
  
Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in _cRowsDeleted zurückgegeben._ Es wird kein Fehler zurückgegeben, wenn eine oder mehrere Zeilen nicht gefunden wurden. 
  
Nachdem die Zeilen gelöscht wurden, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Durch das Löschen von Zeilen werden die Spalten, die vorhandenen Tabellenansichten oder anschließend geöffneten Tabellenansichten zur Verfügung stehen, nicht reduziert, auch wenn die gelöschten Zeilen die letzten sind, die Werte für eine bestimmte Spalte enthalten.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

