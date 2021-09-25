---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48810ea68394fa21ad666dfc8464bbf12b2c8359
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584227"
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
  
> [in] Eine Bitmaske mit Flags, die den Löschvorgang steuert. Das folgende Kennzeichen kann festgelegt werden:
    
TAD_ALL_ROWS 
  
> Löscht alle Zeilen aus der Tabelle und alle entsprechenden Ansichten und sendet eine einzelne TABLE_RELOAD Benachrichtigung.
    
 _lprowsetToDelete_
  
> [in] Ein Zeiger auf einen Zeilensatz, der die zu löschenden Zeilen beschreibt. Der  _LprowsetToDelete-Parameter_ kann NULL sein, wenn das flag TAD_ALL_ROWS im  _UlFlags-Parameter_ festgelegt ist. 
    
 _cRowsDeleted_
  
> [out] Die Anzahl der gelöschten Zeilen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabellenzeilen wurden erfolgreich gelöscht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrDeleteRows-Methode** sucht und entfernt die Tabellenzeilen, die die Spalten enthalten, die der Eigenschaft entsprechen, auf die der **lpProps-Member** jedes **aRow-Eintrags** im Zeilensatz verweist. Eine Indexspalte wird verwendet, um jede Zeile zu identifizieren. Diese Spalte muss das gleiche Eigenschaftstag wie das Eigenschaftstag aufweisen, das im  _ulPropTagIndexColumn-Parameter_ beim Aufruf der [CreateTable-Funktion](createtable.md) übergeben wird. 
  
Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in  _cRowsDeleted_ zurückgegeben. Wenn eine oder mehrere Zeilen nicht gefunden werden konnten, wird kein Fehler zurückgegeben. 
  
Nachdem die Zeilen gelöscht wurden, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die eine Ansicht der Tabelle haben und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Das Löschen von Zeilen reduziert nicht die Spalten, die für vorhandene Tabellenansichten oder anschließend geöffnete Tabellenansichten verfügbar sind, selbst wenn die gelöschten Zeilen die letzten sind, die Werte für eine bestimmte Spalte haben.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

