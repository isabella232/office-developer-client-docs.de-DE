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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278947"
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
  
> in Eine Bitmaske von Flags, die den Löschvorgang steuert. Das folgende Flag kann festgelegt werden:
    
TAD_ALL_ROWS 
  
> Löscht alle Zeilen aus der Tabelle und alle entsprechenden Ansichten und sendet eine einzelne TABLE_RELOAD-Benachrichtigung.
    
 _lprowsetToDelete_
  
> in Ein Zeiger auf einen Zeilensatz, der die zu löschenden Zeilen beschreibt. Der _lprowsetToDelete_ -Parameter kann NULL sein, wenn das TAD_ALL_ROWS-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _cRowsDeleted_
  
> Out Die Anzahl der gelöschten Zeilen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Tabellenzeilen wurden erfolgreich gelöscht.
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrDeleteRows** -Methode sucht und entfernt die Tabellenzeilen, die die Spalten enthalten, die mit der Eigenschaft übereinstimmen, auf die durch das **lpProps** -Element jedes **aRow** -Eintrags im Zeilensatz verwiesen wird. Eine Indexspalte wird verwendet, um jede Zeile zu identifizieren. Diese Spalte muss dasselbe Property-Tag aufweisen wie das Property-Tag, das im _ulPropTagIndexColumn_ -Parameter im Aufruf der [createable](createtable.md) -Funktion übergeben wird. 
  
Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in _cRowsDeleted_zurückgegeben. Wenn eine oder mehrere Zeilen nicht gefunden wurden, wird kein Fehler zurückgegeben. 
  
Nachdem die Zeilen gelöscht wurden, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Durch das Löschen von Zeilen werden die verfügbaren Spalten für vorhandene Tabellen Ansichten oder anschließend geöffnete Tabellen Ansichten nicht reduziert, auch wenn die gelöschten Zeilen die letzten sind, die Werte für eine bestimmte Spalte aufweisen.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

