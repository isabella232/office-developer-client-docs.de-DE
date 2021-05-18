---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421676"
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
  
> [in] Ein Zeiger auf eine Eigenschaftswertstruktur, die die Indexspalte für die zu löschende Zeile beschreibt. Das **ulPropTag-Element** der Eigenschaftswertstruktur sollte das gleiche Eigenschaftstag wie der  _ulPropTagIndexColumn-Parameter_ aus dem Aufruf der [CreateTable-Funktion](createtable.md) enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die Eigenschaft, auf die der  _lpSPropValue-Parameter_ verweist, identifiziert keine Zeile in der Tabelle. 
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrDeleteRow-Methode** entfernt die Tabellenzeile, die die Spalte enthält, die der Eigenschaft entspricht, auf die der  _lpSPropValue-Parameter_ verweist. Die Daten für die Zeile werden gelöscht, und die Zeile wird aus allen geöffneten Ansichten entfernt. 
  
Nachdem die Zeile gelöscht wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Durch das Löschen einer Zeile wird der Spaltensatz, der vorhandenen oder anschließend geöffneten Ansichten zur Verfügung steht, nicht reduziert, auch wenn die gelöschte Zeile die letzte Zeile mit einem Wert für eine bestimmte Spalte ist.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

