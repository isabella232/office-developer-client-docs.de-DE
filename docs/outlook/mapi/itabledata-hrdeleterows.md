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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792835"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Eine Bitmaske aus Flags, die den Löschvorgang steuert. Das folgende Flag kann festgelegt werden:
    
TAD_ALL_ROWS 
  
> Löscht alle Zeilen aus der Tabelle und alle zugehörigen Ansichten eine einzelne TABLE_RELOAD-Benachrichtigung senden.
    
 _lprowsetToDelete_
  
> [in] Ein Zeiger auf ein Rowset fest, die die zu löschenden Zeilen beschreibt. Der Parameter _LprowsetToDelete_ kann NULL sein, wenn das Flag TAD_ALL_ROWS im _UlFlags_ -Parameter festgelegt ist. 
    
 _cRowsDeleted_
  
> [out] Die Anzahl der gelöschten Zeilen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Zeilen der Tabelle gelöscht wurden.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrDeleteRows** -Methode sucht und entfernt die Zeilen der Tabelle, die die Spalten enthalten, die die-Eigenschaft zum Festlegen anhand der **LpProps** Member der einzelnen **aRow** Einträge in der Zeile gezeigt entsprechen. Eine Indexspalte wird verwendet, um jede Zeile zu identifizieren. Diese Spalte muss das gleiche Eigenschafts-Tag als das Eigenschafts-Tag im _UlPropTagIndexColumn_ -Parameter im Aufruf der [CreateTable](createtable.md) -Funktion übergeben haben. 
  
Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in _cRowsDeleted_zurückgegeben. Es wird kein Fehler zurückgegeben, wenn eine oder mehrere Zeilen nicht gefunden werden konnte. 
  
Nachdem die Zeilen gelöscht werden, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet. 
  
Löschen von Zeilen, verringert sich nicht auf die Spalten der vorhandenen Tabelle Ansichten oder Tabellenansichten anschließend geöffnet werden, selbst wenn gelöschten Zeilen der letzten, die Werte für eine bestimmte Spalte enthalten sind.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[' Srowset '](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

