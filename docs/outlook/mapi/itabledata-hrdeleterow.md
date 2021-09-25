---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc516d8792fe87e6b9caf282146ad8ef996715c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587846"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löscht eine Tabellenzeile.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameter

 _lpSPropValue_
  
> [in] Ein Zeiger auf eine Eigenschaftswertstruktur, die die Indexspalte für die zu löschende Zeile beschreibt. Der **ulPropTag-Member** der Eigenschaftswertstruktur sollte dasselbe Eigenschaftstag wie der  _ulPropTagIndexColumn-Parameter_ aus dem Aufruf der [CreateTable-Funktion](createtable.md) enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die Eigenschaft, auf die der  _parameter lpSPropValue_ verweist, identifiziert keine Zeile in der Tabelle. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **ITableData::HrDeleteRow-Methode** entfernt die Tabellenzeile, die die Spalte enthält, die mit der Eigenschaft übereinstimmt, auf die der  _parameter lpSPropValue_ verweist. Die Daten für die Zeile werden gelöscht, und die Zeile wird aus allen geöffneten Ansichten entfernt. 
  
Nachdem die Zeile gelöscht wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die eine Ansicht der Tabelle haben und die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Durch das Löschen einer Zeile wird der Spaltensatz, der für vorhandene Ansichten oder anschließend geöffnete Ansichten verfügbar ist, nicht reduziert, auch wenn die gelöschte Zeile die letzte Zeile ist, die einen Wert für eine bestimmte Spalte aufweist.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

