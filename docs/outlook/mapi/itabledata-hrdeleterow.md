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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278859"
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
  
> in Ein Zeiger auf eine Eigenschaftswert Struktur, die die Indexspalte für die zu löschende Zeile beschreibt. Das **ulPropTag** -Element der Eigenschaftswert Struktur sollte das gleiche Property-Tag wie der _ulPropTagIndexColumn_ -Parameter aus dem Aufruf der [createable](createtable.md) -Funktion enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Zeile wurde erfolgreich gelöscht.
    
MAPI_E_NOT_FOUND 
  
> Die Eigenschaft, auf die durch den _lpSPropValue_ -Parameter verwiesen wird, identifiziert keine Zeile in der Tabelle. 
    
## <a name="remarks"></a>Bemerkungen

Die **ITableData:: HrDeleteRow** -Methode entfernt die Tabellenzeile, die die Spalte enthält, die mit der Eigenschaft übereinstimmt, auf die durch den _lpSPropValue_ -Parameter verwiesen wird. Die Daten für die Zeile werden gelöscht, und die Zeile wird aus allen geöffneten Ansichten entfernt. 
  
Nachdem die Zeile gelöscht wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren. 
  
Durch das Löschen einer Zeile wird der Spaltensatz, der für vorhandene oder nachträglich geöffnete Ansichten verfügbar ist, nicht reduziert, auch wenn es sich bei der gelöschten Zeile um die letzte Zeile handelt, die einen Wert für eine bestimmte Spalte aufweist.
  
## <a name="see-also"></a>Siehe auch



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

